# Selftests
Things I would watch for in logfiles and in testing...

* systemctl status at startup
  * systemctl status qubes-vm@sys-usb.service
  * journalctl -xeu qubes-vm@sys-usb.service
* sys-usb startup fail
  * useful msg: add “qubes.skip_autostart” to grub AND  remove rd.qubes_hide_all_usb from grub.
* other qube startup fail
* every qube startup fail
* multiple qubes with same device assignment(s)
  * and autostart?
  * are startup failures due to non-availability avoidable? 
* qubes with assigned PCI devs that are missing.
* qubes with no strict reset on devices.
* qrexec timeout
  * has devices?
  * no devices?
  * recent changes?
*  /var/log/xen/console/guest-sys-usb.log etc
*  var/log/xen/console/guest-sys-net.log
   *  maybe also this one: /var/log/xen/console/guest-sys-net-dm.log
* ? /var/log/xen/console/hypervisor.log
*  policy: lint
*  segfaults
*  panics
*  BUGs
*  qubes with non-accept firewall rules but upstream netvm has no qvm-firewall daemon running. Drop rules are not implemented. https://forum.qubes-os.org/t/serious-qvm-firewall-bypass-possibly-if-you-do-not-understand-qvm-firewall-and-qubes-firewall-service/39429/22 and rest of that thread.

* shutdown error
* pool error?
* clockvm error
* netvm or sys-fw
* minimal tpl
* missing qubes services?
* dispvm cannot start
* no iommu
* no vt-d etc
* xen smt?
* acpi errors - benign
* 
* secureboot
* slots on luks? safety one?

*  missing service(s)
*  ask policies
*  denials
*  time since last backup?
*  qube types?
   * audiovm
   * guivm
   * video/qva
   * ???
* shutdown-idle service enabled ?
* other services?
* 

* ? sys-usb - > sys-usb: denied: loopback qrexec connection not supported


* A start job for unit qubes-vm@sys-usb.service has begun execution.
Jun 20 16:57:22 dom0 qvm-start[3868]: Error: * Cannot connect to qrexec agent for 60 seconds, see /var/log/xen/console/guest-sys-usb.log for details
Jun 20 16:57:22 dom0 systemd[1]: qubes-vm@sys-usb.service: Main process exited, code=exited, status=1/FAILURE
░░ An ExecStart= process belonging to unit qubes-vm@sys-usb.service has exited.
░░ The process' exit code is 'exited' and its exit status is 1.
Jun 20 16:57:22 dom0 systemd[1]: qubes-vm@sys-usb.service: Failed with result 'exit-code'.


what was:
“qrexec-policy-graph –include-ask”?


