# Sitecore.HabitatHome.Utilities

## Typical Installation Procedure

1. [Installing Prerequisites](prerequisites/readme.md)
2. [Installing Sitecore Experience Platform (XP)](xp/readme.md)
3. [Installing Modules](xp/installing-modules.md)
4. [Installing Experience Commerce (XC)](xc/readme.md)

## Additional Operations

- [Warming Up a Sitecore Instance](warmup/readme.md)

## General Folder Descriptions

### Azure

The Azure folder contains a set of scripts for managing Azure IaaS VMs. In particular:

- Taking a snapshot of an existing VM
- Creating a "master" VHD from the snapshot for use in replicating the "master"
- Create VM from a stored VHD, complete with firewall configuration and auto-shutdown

### Prerequisites

The Prerequisites folder contains helper scripts to get a Windows environment ready for the installation of Sitecore (XP and/or XC).

See the [readme.md](prerequisites/readme.md) in the `prerequisites` doc folder for a detailed description and instructions.

### SecurityHardening

The SecurityHardening folder contains _sample_ scripts to harden a Sitecore instance based on information available on doc.sitecore.com. They are used for illustration purposes only and users should validate these scripts against their own needs and environment prior to using them.

### Shared

The Shared folder contains modules and SIF configurations to support functionality that is common across other HabitatHome Utilities folders.

### Warmup

The Warmup folder contains a script to warmup a set of pages.

See the [readme.md](warmup/readme.md) in the `warmup` doc folder for a detailed description and instructions.

### XC (Experience Commerce)

The XC folder contains a set of scripts for installing Sitecore Experience Commerce 9 with all the required modules.

See the [readme.md](xc/readme.md) in the `xc` doc folder for a detailed description and instructions.

### XP (Experience Platform)

The XP folder contains a set of scripts for installing Sitecore Experience Platform 9 with all the required modules and certificates.

See the [readme.md](xp/readme.md) in the `xp` doc folder for a detailed description and instructions.
