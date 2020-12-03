# IOXIDResolver (Python3 updated)
IOXIDResolver.py from AirBus Security

I couldn't find an official repository for this code so I am posting it here. It's great research and super useful.

- The source from this blog post: https://airbus-cyber-security.com/the-oxid-resolver-part-1-remote-enumeration-of-network-interfaces-without-any-authentication/
- Part 2 of that blog post: https://airbus-cyber-security.com/the-oxid-resolver-part-2-accessing-a-remote-object-inside-dcom/

## Example Run

```
user@host:~/IOXIDResolver$ python3 IOXIDResolver.py -t 10.10.11.3
[*] Retrieving network interface of 10.10.11.3
Address: HYPERV1
Address: 192.168.57.1
Address: 192.168.2.1
Address: 192.168.77.201
Address: 10.10.11.3
```
This is super useful because it helps you to identify hosts that have additional active interfaces, which usually means, virtual machines, VPNs, connected wireless, docker, etc. Basically "interesting".


## Impacket toubleshooting

If you have problems with impacket modules, please consider to install it in a virtualenv.

https://github.com/SecureAuthCorp/impacket

Installation info from Impacket repo:
In order to install the source execute the following command from the directory where the Impacket's distribution has been unpacked: pip3 install . (pip install . for Python 2.x). This will install the classes into the default Python modules path; note that you might need special permissions to write there.
