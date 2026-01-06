# Neptune Software Suite
## Introduction
The Neptune Software Suite is a research project I started along time ago. This is still hosted on BitBucket, moving to GitHub so all projects are in one location. This includes NCC1 which is a rewrite and most up-to-date codebase of NCC. NCC was part of the Neptune OS codebase however has since been moved to its own repository due to its complexity. The Neptune OS, NCC, and related SDK's and other tools are a Work In Progress (WIP), run at your own risk.

## nboot
The Neptune Boot Loader for the Neptune operating system. It is primarily written in C and some assembly. The core application nboot and related libraries runs in 32 bit protected mode. The system includes drivers to support UEFI and Legacy BIOS firmware.
### Legacy BIOS
To target Legacy BIOS, link nboot with the BIOS firmware driver. Prepend nstart.bin to nboot.exe to create nboot. Install one of the boot sectors compatible with the file system and boot device, and copy nboot to the root directory of the file system.
### UEFI
To target UEFI, link nboot to the UEFI firmware driver. Then build nboot as an UEFI application - nboot.efi.
## nexec
The Neptune Executive is a microkernel. It runs in 32 bit protected mode and runs as a higher half kernel.
## nsdk
The Neptune SDK implements nasm, nmake, nbuild, and other utilities. ncc has been moved to a separate repository.
