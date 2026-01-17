\# RHEL 8 – Reset Root Password



\## Steps



1\. Reboot VM and stop at GRUB

2\. Press `e` and append `rd.break`

3\. Boot with Ctrl+X

4\. Remount and chroot:

&nbsp;  ```bash

&nbsp;  mount -o remount,rw /sysroot

&nbsp;  chroot /sysroot

Reset password

passwd root

touch /.autorelabel



