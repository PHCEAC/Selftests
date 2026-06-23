# Selftests
Things I would watch for in logfiles

* systemctl status at startup
  * systemctl status qubes-vm@sys-usb.service
  * journalctl -xeu qubes-vm@sys-usb.service
* sys-usb startup fail
  * useful msg: add “qubes.skip_autostart” to grub AND  remove rd.qubes_hide_all_usb from grub.
* other qube startup fail
* qrexec timeout
  * has devices?
  * no devices?
  * recent changes?
*  /var/log/xen/console/guest-sys-usb.log etc
*  

* shutdown error
* pool error?
* clockvm error
* netvm or sys-fw
* minimal tpl
* missing qubes services?
* dispvm cannot start
* no iommu
* secureboot
* slots on luks? safety one?




* A start job for unit qubes-vm@sys-usb.service has begun execution.
Jun 20 16:57:22 dom0 qvm-start[3868]: Error: * Cannot connect to qrexec agent for 60 seconds, see /var/log/xen/console/guest-sys-usb.log for details
Jun 20 16:57:22 dom0 systemd[1]: qubes-vm@sys-usb.service: Main process exited, code=exited, status=1/FAILURE
░░ An ExecStart= process belonging to unit qubes-vm@sys-usb.service has exited.
░░ The process' exit code is 'exited' and its exit status is 1.
Jun 20 16:57:22 dom0 systemd[1]: qubes-vm@sys-usb.service: Failed with result 'exit-code'.



