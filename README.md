# How to use an Exit specifically

If you have been kind enough to support us in paying for an exit or you just want to use them specifically there is a configuration
change that you need to make to your Tor browser bundle. To do this it is slightly different locations for the particular host
operating system you are using the Tor browser on. 

You may also add changes to your torsocks configuration to use an exit specifically.

Our exit list can be found in the feed of the CypherpunkLabs Twitter account or you can use the tor metrics page with the following url:


https://metrics.torproject.org/rs.html#search/contact:cypherpunklabs@protonmail.com

All of our exits, guards, and bridges unless private bridge will have our email as support contact.



# Configuration

If you installed Tor Browser on Windows or Linux, the torrc file is in the data directory, which is Browser/TorBrowser/Data/Tor inside your Tor Browser directory.

If you are using macOS the torrc will be found in the following location: ~/Library/Application Support/TorBrowser-Data/Tor/torrc


Open up your torrc with your favorite editor and add the following lines:


```
ExitNodes $IP(Or you can use the exit's fingerprint)

```

You can also define country specific exits if you choose with the following:

```
ExitNodes {$countrycode} StrictNodes 1

```

