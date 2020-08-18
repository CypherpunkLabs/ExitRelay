# IoT, HighTraffic, Streaming Services policy

This Policy is designed for using IOT streaming services or big data applications via Tor.

```
ExitPolicy accept *:20-21 	# FTP
ExitPolicy accept *:43 		# WHOIS
ExitPolicy accept *:53 		# DNS
ExitPolicy accept *:79 		# finger
ExitPolicy accept *:80-81 	# HTTP, HTTP alt.
ExitPolicy accept *:83 		# MIT ML Device
ExitPolicy accept *:85 		# MIT ML Device
ExitPolicy accept *:86 		# BroadCam Video Streaming Server
ExitPolicy accept *:88 		# kerberos
ExitPolicy accept *:90 		# dnsix Securit Attribute Token Map / Pointcast
ExitPolicy accept *:110 	# POP3
ExitPolicy accept *:143 	# IMAP
ExitPolicy accept *:220 	# IMAP3
ExitPolicy accept *:389 	# LDAP
ExitPolicy accept *:443 	# HTTPS
ExitPolicy accept *:464		# kpasswd
ExitPolicy accept *:531 	# IRC/AIM
ExitPolicy accept *:543-544 	# Kerberos
ExitPolicy accept *:554 	# RTSP
ExitPolicy accept *:636 	# LDAP
ExitPolicy accept *:706 	# SILC
ExitPolicy accept *:749 	# kerberos
ExitPolicy accept *:873 	# rsync
ExitPolicy accept *:902-904 	# VMware
ExitPolicy accept *:981 	# Remote HTTPS management for firewall
ExitPolicy accept *:989-990 	# FTP over TLS/SSL
ExitPolicy accept *:991 	# Netnews Administration System
ExitPolicy accept *:992 	# Telnet protocol over TLS/SSL
ExitPolicy accept *:993 	# IMAP over SSL (N.B. potential abuse - brute-force attacks - tornull.org)
ExitPolicy accept *:995 	# POP3 over SSL
ExitPolicy accept *:1043 	# BOINC Client Control
ExitPolicy accept *:1103 	# Adobe Server 2
ExitPolicy accept *:1113 	# Licklider Transmission Protocol (IANA official) [RFC 5326]
ExitPolicy accept *:1194 	# OpenVPN
ExitPolicy accept *:1220 	# QT Server Admin
ExitPolicy accept *:1293 	# PKT-KRB-IPSec
ExitPolicy accept *:1500 	# VLSI License Manager
ExitPolicy accept *:1533 	# Sametime
ExitPolicy accept *:1677 	# GroupWise
ExitPolicy accept *:1723 	# PPTP
ExitPolicy accept *:1755 	# RTSP
ExitPolicy accept *:1863 	# MSNP
ExitPolicy accept *:1883 	# Message Queuing Telemetry (IANA official)
ExitPolicy accept *:2082 	# Infowave Mobility Server and CPanel default
ExitPolicy accept *:2083 	# Secure Radius Service (radsec) and CPanel default SSL
ExitPolicy accept *:2086-2087 	# GNUnet, ELI
ExitPolicy accept *:2095-2096 	# NBX
ExitPolicy accept *:2102-2104 	# Zephyr
ExitPolicy accept *:3690 	# SVN
ExitPolicy accept *:4321 	# RWHOIS
ExitPolicy accept *:4643 	# Virtuozzo
ExitPolicy accept *:4070 	# Trivial IP Encryption (TrIPE)
ExitPolicy accept *:5004 	# RTP media data [RFC 3551, RFC 4571]
ExitPolicy accept *:5050 	# MMCC
ExitPolicy accept *:5190 	# ICQ and AOL Instant Messenger
ExitPolicy accept *:5222-5223 	# XMPP, XMPP over SSL
ExitPolicy accept *:5228 	# Android Market
ExitPolicy accept *:5287 	# IP Camera viewer apps
ExitPolicy accept *:5675 	# V5UA application port (IANA official) [RFC 3807]
ExitPolicy accept *:6880 	# Dwyco Video Conferencing
ExitPolicy accept *:8008 	# HTTP alternate
ExitPolicy accept *:8074 	# Gadu-Gadu
ExitPolicy accept *:8082 	# HTTPS Electrum Bitcoin port
ExitPolicy accept *:8087-8088 	# Simplify Media SPP Protocol, Radan HTTP - Control Panel
ExitPolicy accept *:8232-8233 	# Zcash
ExitPolicy accept *:8332-8333 	# Bitcoin
ExitPolicy accept *:8443 	# PCsync HTTPS - Plesk Control Panel, Apache Tomcat SSL
ExitPolicy accept *:8502 	# FTN Message Transfer Protocol (IANA official)
ExitPolicy accept *:8601 	# Wavestore CCTV protocol
ExitPolicy accept *:8602	# XBConnect, Wavestore Notification protocol
ExitPolicy accept *:8888 	# HTTP Proxies, NewsEDGE, HUSH coin
ExitPolicy accept *:9418 	# git - Git pack transfer service
ExitPolicy accept *:11371 	# OpenPGP hkp
ExitPolicy accept *:19294 	# Google Voice
ExitPolicy accept *:19638 	# Ensim control panel
ExitPolicy accept *:50002 	# Electrum Bitcoin SSL
ExitPolicy accept *:64738 	# Mumble - voice over IP
ExitPolicy reject *:*
```

