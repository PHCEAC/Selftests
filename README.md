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
* 



