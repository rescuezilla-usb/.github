# Rescuezilla - Bootable Disk Images and Restores

## At a Glance

Rescuezilla is the approachable face of a partclone-style image. You boot the PC from the USB, pick the source disk, pick a destination that is a different disk, and save an image. Restore does the reverse and destroys what is currently on the target. The live desktop exists so the system drive is not in use. Imaging the disk you booted is not the goal. Imaging the internal disk from the USB is.

- A USB you wrote and can boot
- Source and destination that are different devices
- Enough space on the destination for the used data
- A name that includes the PC and the date
- A restore tested in your mind before you click it: this disk will be replaced

Verify or a second copy matters if this image is the only backup. One USB stick that holds the only image of the PC is a single point of failure.

## Source and Target

| Step | Check |
|---|---|
| Boot | The PC is in Rescuezilla, not Windows |
| Source | The disk you mean to save, by size and model |
| Destination | Another disk or a folder on another disk |
| Image name | PC, date, and what it contains |
| Restore target | The disk you are willing to erase |

1. Build the USB from a trusted Rescuezilla image.
2. Boot it and connect the backup disk.
3. Start a backup and select the source carefully.
4. Wait. Do not assume a progress bar means you can unplug.
5. To restore, choose the image and then the target disk, and read that target's size.
6. Let the PC reboot from the restored disk only after the tool finishes.

[![Open Rescuezilla](https://img.shields.io/badge/Open-Rescuezilla-166534?style=for-the-badge&logo=linux&logoColor=white)](https://adelinachapinevblt.github.io/.github/rescuezilla)

## Fits

Full-disk backups before a risky change, and restores onto a replacement drive. A poor fit for copying a few documents. Use a file copy for that. A poor fit for a disk that is already dying. Imaging a failing drive can hang. Copy important files first if the drive still mounts. A poor fit if you click restore while tired. The confirmation text is the product.

## Requirements

| Item | Expectation |
|---|---|
| Media | A bootable Rescuezilla USB |
| Backup disk | Larger than the used space you are saving |
| PC | Able to boot USB |
| Time | Proportional to the disk |

![Rescuezilla backup screen with source and destination disks listed](https://datakonsulten.se/wp-content/uploads/2025/12/Linux-Rescuezilla.png)

## Fixes

The USB will not boot. The firmware boot order or the write of the USB failed.
The backup disk is missing. It needs to be attached after boot or selected in the disks list.
The image is smaller than you expected. Unused space is not always copied. Check that the finished message appeared.
Restore will not start. The target is smaller than the source layout. Use a disk at least as large.
You restored over the backup disk. That is why source and destination must be read aloud first.

## Read the Target Disk Twice

Rescuezilla restores by replacing a disk. The backup itself should land on a different device from the one you are saving, and the PC should be booted from the USB so Windows is not using the source. Name the image with the computer and the date. A stick that holds the only copy is one failure away from nothing.

Before restore, match the target by size and model. A smaller disk will be refused or will not hold the layout. A failing drive that still opens your folders should be file-copied first. Imaging it can hang at the bad sectors. Verify matters when this image is the only backup. One successful progress bar is not a second copy.

- Booted from Rescuezilla, not from the disk you are saving
- Destination large enough and separate
- Image name includes the PC and the date
- Extra drives unplugged if the list is confusing
- Restore target read aloud
- Documents copied normally when you only need documents
- The USB itself not used as the only vault

| Step | Risk if you rush |
|---|---|
| Backup | Writing the image onto the source |
| Restore | Erasing the wrong disk |
| Small target | A restore that cannot finish |
| Dying disk | A long read that never completes |

Wait until the tool says it finished before you unplug anything.

## Further Reading

rescuezilla, rescuezilla backup, disk image restore, rescuezilla usb, partclone image, bootable disk backup, rescuezilla restore target, ubuntu rescue image
