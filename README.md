# Simplest local DNS resolver (sldns)

The tiny domain name resolving utility using system call `gethostbyname()` (i.e. with possible DoH/DoT/DNSCrypt/etc
features supported by your OS).

One of the main purposes of it is to check if your ISP is replacing unencrypted DNS requests: find a host with a
different MX record between some DNS server and your ISP, make a classic host/dig/nslookup request (i.e. without
encryption), and compare it with the result of this program. If the IP is the same, I have bad news for you...

## Usage

```bash
./sldns domain.name
```

## TODO

Provide test service for checking possible DNS hijacking.
