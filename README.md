mkinitcpio-syslinux
===================

A hook to have mkinitcpio automagically update the syslinux bootloader
image on Arch Linux. This hook will automatically install itself the
existing `linux.preset` to ensure syslinux is always run when a new
initramfs is built.
