# Selftests
Things I would watch for in logfiles

* systemctl status at startup
  * systemctl status qubes-vm@sys-usb.service
  * journalctl -xeu qubes-vm@sys-usb.service
* sys-usb startup fail
* other qube startup fail
* qrexec timeout
  * has devices?
  * no devices?
  * recent changes?
* shutdown error
* pool error?
* clockvm error
* netvm or sys-fw
* 



