# TFTP Ansible Role
A TFTP server (Trivial File Transport Protocol) is commonly used in PXE boot setups, where the NIC fetches a boot file and a 'next-server' IP address for a TFTP server from a DHCP server.
In our case this TFTP server then delivers a pxe-script file, which tells the server where to get the Kernel, initramfs and slx-config via HTTP.

## This Role
Installs `tftp-server` package, creates and enables a systemd service for it.
## Variable
Only one: the directory where the `pxe-script-file` lives
~~~
tftpboot_path: "/mnt/tftpboot"
~~~

## License
MIT
