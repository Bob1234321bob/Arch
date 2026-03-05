# Here is my guide on how I installed a very basic Arch Linux Setup:

## Creating a boot stick

  ### Windows
  If you have a Windows PC, you can create a Bootstick very easily
  
  1. Download Rufus:
  ```
  https://rufus.ie/
  ```
  2. Download an Arch Linux ISO:
  ```
  https://archlinux.org/download/
  ```
  3. Install Rufus and start it.
  4. Choose your Arch ISO File and the USB Stick and click on start.
  5. When it's finished, you can close Rufus and Restart your PC. Click the Fkey that bringst you to the BIOS/UEFI (F2, F8 or F10).
  6. Depending on the BIOS/UEFI, you have to turn off "Secure Boot" and you have to change your Boot Order, so your PC boots in to your Bootstick.
  7. After saving your changes, your PC will restart and you can start with your Arch installation.

## Arch Installation

### Change your Keyboard
1. The default keyboard layout is US_English. To change it, look what layouts are available:
```
localectl list-keymaps
```
2. If you found your layout, use loadkeys (I use a german keyboard, for example):
```
loadkeys de-latin1
```

### Boot mode
1. Very important to check what boot mode you use!!! This is the command:
```
cat /sys/firmware/efi/fw_platform_size
```
If you get a `64`: You use a 64-bit UEFI Boot-Mode.\
If you get a `32`: You use a 32-bit UEFI Boot-Mode.\
If you dont get anything: You use a BIOS Boot-Mode.\
Depending on your Boot-Mode, you have to install Arch differently!

### Internet
If you have 




