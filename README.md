# Neptune Software Suite
## Introduction
This is a long-term research project that I started a long time ago. It began as an experiment for creating a boot loader in Visual Studio and has since been expanded. Please run at your own risk.

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
