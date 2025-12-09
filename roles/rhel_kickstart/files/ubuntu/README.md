dnsmasq port 53 conflict with systemd-resolve.

Edit /etc/dnsmasq.conf and uncomment #bind-interfaces. Restart service daemon dnsmasq

or 

create /etc/dnsmasq.d/pxe.conf with a line bind-interfaces

Optional:

You might consider of editing /etc/systemd/resolv.conf and put in 

DNSStubListener=no

This has to be done before installing dnsmasq.