# ExitService

The following configurations and scripts are used to power our Tor exit servers.

Included in this README.md is a basic guide on how to setup and exit node if you so chose to. This is also 
the settings and configurations used for all of our servers. Listed below are the operating systems that 
are used by Cypherpunk Labs to deliver the Tor exit relays.


# Risks in running an exit

There are a few inherit risks when dealing with exit nodes. You need to be sure to allow your contact ISP, you should
also evaluate what types of traffic you will allow. There is some critical pieces to this, including but not limited to the 
fact the host may be used for abuse purposes. This is a side effect of the anonymity with the Tor network. Ransomware and 
scammers use the same pipelines that journalists and the oppressed use. 


# Fedora

First and foremost let's install Tor:

```
sudo yum install tor -y

```

Set policy for SELinux, similar to the following should cover it: 

```
touch tor-selinux-workaround.cil

```

Add the following to the aforeementioned file:
 
```
typeattributeset cil_gen_require tor_t)
(allow tor_t self (capability (dac_override dac_read_search)))

```

Now run the following command:

```
sudo semodule -i tor-selinux-workaround.cil

```

Now you will need to modify your /etc/tor/torrc file with the following changes:


```
DirPort 80

DirPort $PATHtoHTMLExitFile

```

Uncommenty the following entries;

```
ExitRelay 1

```

You should consider adding an extended exit policy, those are covered in this repository as well.

Next we will need to create a DNS entry for the relay using our DNS provider, map to IP address. Make it descriptive.

Now we will install unbound and configure it to handle DNS locally to prevent upstream filtering:


Install the unbound package:

```
yum install unbound

```

in /etc/unbound/unbound.conf replace the line

```
qname-minimisation: no

```

with:

```
qname-minimisation: yes

```

enable and start unbound:

```
systemctl enable unbound
systemctl start unbound

```

Tell the system to use the local unbound server:

```
cp /etc/resolv.conf /etc/resolv.conf.backup
```

```
echo nameserver 127.0.0.1 > /etc/resolv.conf
```

To avoid that the configuration gets changed (for example by the DHCP client):

```
chattr +i /etc/resolv.conf
```

Once this is all completed run the following command:

```
sudo systemctl start tor.service
```

To enable as system daemon: 

```
sudo systemctl enable tor.service
```

We also setup fail2ban and disable unnecessary services running on the machine for the basis of our template that is deployed with each request. 


