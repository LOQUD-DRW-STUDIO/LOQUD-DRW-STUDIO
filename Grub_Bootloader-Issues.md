Solution-1:
If your in Windows then:

Type : bcdedit /set {bootmgr} displaybootmemu yes
Type : bcdedit /set {bootmgr} \EFI\ubuntu\grubx64.efi
Start : DiskGeniush (Or annother to have acces to linux storage)
Go to : etc\default
Delete File : grub

By this GRUB must be reseted to default settings and be showed and fixed.

If yout in linux then:

Delete : grub (from etc\default)

Solution-2:
If in Windows then:

Open: EasyBCD
Add entry "Linux" and select disk linux.

If in linux then:
Install Grub-Customizer

Go to terminal
Type: sudo apt update
Type: sudo apt install grub-customizer

If not work then:

Type: sudo apt update
Type: sudo apt --fix-broken install
Type: sudo apt install libqt5core5a libqt5gui5 qt5-default
Type: sudo add-apt-repository ppa:danielrichter2007/grub-customizer
Type: sudo apt update
Type: sudo apt install grub-customizer

Using grub-customizer you can fix or add the grub bootloader and hange theme.

Solution-3:
If linux & Windows then: (if windows then use app like in the solution 1)

Go to: etc\default\
Edit: (in windows just edit) (in linux open terminal) sudo nano grub
Type:
GRUB_DEFAULT=saved GRUB_TIMEOUT=10 GRUB_TIMEOUT STYLE=menu GRUB_DISTRIBUTOR="Manjaro" |GRUB_CMDLINE_LINUX_DEFAULT="quiet apparmor=1 security=apparmor udev.log_priority=3"
GRUB CMDLINE LINUX=""
Restart Computer.

Solution-4:
Reinstall both systems using bootable usb media.
