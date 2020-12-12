# DNSMASQ as a DHCP server

This docker-compose file starts a dnsmasq server configured as a dhcp server with support for PXE/TFTP boot.

Before you use this image replace copy `dnsmasq.conf.example` to `dnsmasq.conf` and edit the top section (marked with "IMPORTANT" comment).