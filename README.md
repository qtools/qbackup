# qbackup
This project aims to create a standalone, unix-style executable for running a backup of hard disks on windows machines.

There is already a product that can do this, Disk2VHD, but it has quite limited capabilities and doesn't run well in scripts.

wbAdmin is also available from Microsoft, but I find it too inflexible in how the backup gets sent to the location and it'll also replace any existing backup from the same machine.

## Goals
First and foremost, I want a clean, strict naming convention for the commands that the application handles.

This will run on older environments, so I will be targeting older versions of .NET. Probably no earlier than 3.0.

This application will also be dependant on backup capabilities already found in the OS, and not implementing them internally.

I hope to make this cross platform as well in the future, which may require changing what language its written in.

## Commands
These are just an overview of how I think it will operate for now. I'll implement this, and if it's working well I'll keep the syntax as-is.

```
qbackup --type disk --target C --output \\SERVER\Share\Backup-17062015.vhdx
qbackup --type baremetal --output \\SERVER\Share\Backup-17062015.vhdx
```
