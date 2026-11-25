# Linux Installation

## Objective

Replace Windows 7 with a lightweight Linux operating system to establish a dedicated home lab environment.

## Operating System Selection

- Distribution: Debian 13.8.0 (Trixie)
- Architecture: AMD64 (64-bit)
- Installation image: Network installer (netinst)
- Reason for selection: Low resource requirements, stability, and suitability for server administration.

## Bootable USB Creation

### Tools Used

- Windows 11 computer
- USB flash drive
- Rufus 4.16
- debian-13.8.0-amd64-netinst.iso

### Rufus Configuration

| Setting | Value |
|---|---|
| Partition Scheme | MBR |
| Target System | BIOS or UEFI |
| File System | FAT32 |
| Cluster Size | 16 KB |
| Persistence | None |
| Write Mode | ISO Image Mode |

MBR was selected for compatibility with the Dell Inspiron 531's legacy BIOS.

### Procedure

1. Downloaded the Debian ISO from the official Debian website.
2. Downloaded and launched Rufus.
3. Connected the USB flash drive.
4. Selected the Debian ISO and configured the boot settings.
5. Downloaded the required Syslinux bootloader files.
6. Created the bootable installation media.

## Operating System Installation

Pending.