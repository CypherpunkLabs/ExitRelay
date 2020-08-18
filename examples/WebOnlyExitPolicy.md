# Web Only Exit Policy

Say you want to run just a simple exit node for web services to help out the Tor bundle users(browser), then you could simply run the following
in your relay's exit policy:

```
ExitPolicy accept *:53        # DNS
ExitPolicy accept *:80        # HTTP
ExitPolicy accept *:443       # HTTPS
ExitPolicy reject *:*
```
