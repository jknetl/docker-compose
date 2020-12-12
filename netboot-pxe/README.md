# Netboot PXE server

This image serves as PXE server which can be used to install custom OS locally.

## How to use this image

### Configure DHCP

To boot from PXE your DHCP server must instruct client to the location of PXE server. Most of SOHO routers can't do that. For that case there is the dhcp service bundled in here. If your router supports dhcp "next-boot" option then you can configure it instead. If not, then follow next part:

#### Steps to configure dhcp service

1. copy `dnsmasq/dnsmasq.conf.example` to `dnsmasq/dnsmasq.conf`.
2. edit `dnsmasq/dnsmasq.conf` top section (marked with "IMPORTANT" comment) to use proper ip address which your network uses normally
3. disable DHCP on your SOHO router

### Change path of config files and assets for netboot

## Useful links

- http://localhost:3000
    - management of PXE menus of running instance
- https://blog.linuxserver.io/2019/12/16/netboot-xyz-docker-network-boot-server-pxe/
    - about Netboot and how to customize boot menus
- https://docs.linuxserver.io/images/docker-netbootxyz
    - netboot docs

### Booting windows

https://discourse.linuxserver.io/t/running-windows-setup-in-netboot-xyz/1379

https://forums.unraid.net/topic/84722-support-linuxserverio-netbootxyz/
