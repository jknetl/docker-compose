# Netboot PXE server

This image serves as PXE server which can be used to install custom OS locally.

## How to use this image

### Configure DHCP

To boot from PXE your DHCP server must instruct client to the location of PXE server. Most of SOHO routers can't do that. For that case there is the dhcp service bundled in here. If your router supports dhcp "next-boot" option then you can configure it instead. If not, then follow next part:

#### Steps to configure dhcp service

1. copy `dnsmasq/dnsmasq.conf.example` to `dnsmasq/dnsmasq.conf`.
2. edit `dnsmasq/dnsmasq.conf` top section (marked with "IMPORTANT" comment) to use proper ip address which your network uses normally
3. disable DHCP on your SOHO router
4. Make sure nothing is using port 53 and 69

### Change path of config files and assets for netboot

## Useful links

- http://localhost:3000
    - management of PXE menus of running instance
- https://blog.linuxserver.io/2019/12/16/netboot-xyz-docker-network-boot-server-pxe/
    - about Netboot and how to customize boot menus
- https://docs.linuxserver.io/images/docker-netbootxyz
    - netboot docs

### Booting windows

1. take ISO and extract it into `assets/win10/x64` subfolder
2. When booted into netboot.xyz select "Windows installation"
3. Enter url to windows `http://YOUR-IP:8080/win10`
    - The ending slash must not be present
4. Select boot from url
    - the installer should boot few files from network 
    - it will show their path so check the URL if they cannot be obtained

https://discourse.linuxserver.io/t/running-windows-setup-in-netboot-xyz/1379

https://forums.unraid.net/topic/84722-support-linuxserverio-netbootxyz/
