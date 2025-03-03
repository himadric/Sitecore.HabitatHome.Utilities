## Installation helpers for Sitecore Experience Commerce (XC)

> These steps assume you have all of the prerequisites installed or have followed the instructions at [Prerequisites README.md](../../Prerequisits/README.md) and [XP Installation README.md](..\..\XP\install\README.md)

Still in an elevated PowerShell session

- Browse to the XC installation folder
  
    ```powershell
    Set-Location ..\..\XC\install
    ```

- Set some predefined defaults
  
    ```powershell
    .\set-installation-defaults.ps1
    ```

- Create a copy of the overrides file

    ```powershell
    copy set-installation-overrides.ps1.example set-installation-overrides.ps1
    ```

- Edit **`set-installation-overrides.ps1`** to set the SQL instance name and sa password

- Apply overrides

    ```powershell
    .\set-installation-overrides.ps1
    ```

> **KNOWN ISSUE:** Automatic download of assets is current not working as expected.
> 
> **WORKAROUND:** Download the following assets and place them in the indicated folders:
> - [Sitecore.Commerce.2019.04-3.0.163.zip](https://dev.sitecore.net/~/media/EF8EE376257142B4BDFAFF7EB1E1CA3E.ashx) - `xc/install/assets/downloads`
> - [Habitat Home Product Images.zip](https://sitecore.box.com/shared/static/bjvge68eqge87su5vg258366rve6bg5d.zip) - `xc/install/assets/Commerce`

Once the above files have been downloaded, these are **_2 options_** to install the Sitecore Experience Commerce

- If you plan on installing the Habitat Home Demo (**Sitecore.HabitatHome.Commerce**), execute the script without parameter

    ```powershell
    .\install-xc0.ps1
    ```
- If you simply want a fresh instance of Sitecore Experience Commerce without the pre-loaded demo assets, simply append `-SkipHabitatHomeInstall` as below
  
    ```powershell
    .\install-xc0.ps1 -SkipHabitatHomeInstall
    ```

## Troubleshooting

#### Resuming Installation

If a part of the installation fails, you can resume from the last failed step by removing the relevant tasks in the `Commerce_SingleServer.json` file.

The file is located in `XC\install\assets\Resources`.

Make sure you make a backup copy of the file.
