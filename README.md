# Daedalus restore wallet process

> A small guide (written as of may 2018) to help you restore a [Daedalus wallet](https://daedaluswallet.io) (Version 1.1.5813) for windows 10 users. (On new macOS APFS full 64 bits it should be natively fast enough)

:bulb: The test was done on a win10 macbook12 bootcamp partition

Requirements:

- Having already synced the whole blockchain once
- Install git bash from [official website](https://git-scm.com/downloads)
- During the installation (of git) be sure to check **git bash & linux like commands**

### Deactivate all virus & threat protections

> A strong interaction between Daedalus and Antimalware Service Executable - Windows Defender Antivirus Service on a freshly installed / fully updated instance of Windows 10 Pro x64 was observed.

You **MUST** turn **OFF** all the options in the section "VIRUS & THREAT PROTECTION SETTINGS"

![VIRUSTHREATPROTECTIONSETTINGS](win-settings.PNG)

:bulb: After a windows update the protection might be reactivated again!

### Make a back-up of the whole blockchain to your desktop

>Rigth click anywhere to open a new git bash and enter the following command:

`mv ~/AppData/Roaming/Daedalus/DB-1.0  ~/Desktop/DB-1.0`

### Uninstall Daedalus properly

- Uninstall Deadalus from control panel
- Remove remaining roaming files: `rm -rf ~/AppData/Roaming/Daedalus/`

### Reinstall Daedalus properly

- Install Daedalus
- Launch Daedalus and expect to see the first blocks syncing (anything > 0%)
- Quit Daedalus
- Remove DB-1.0 folder from Roaming: `rm -rf ~/AppData/Roaming/Daedalus/DB-1.0/`
- And replace with the whole previous blockchain datas from desktop with:

`mv ~/Desktop/DB-1.0 ~/AppData/Roaming/Daedalus/DB-1.0`

### Restoring an old wallet

- Restart Daedalus again
- Create a new temporary wallet
- Restore the old wallet with your seeds phrase

:trophy: From the moment I clicked on the button "restore wallet" it took me ~2h to restore (with a network interruption in between...)

___

If it helped you the smallest donation is welcome:

ETH: 0x390a745cc529e2fefc2c2a320f91243148dbed34
ADA: DdzFFzCqrhsyMRDCwmyn1KWXkvDXenTYapsPU3FG4fy2j2QK8Kn52J2gaNtogv3B5L7tiwZNWchBi6BVVhDF9ynMR2jYuqiGrvZUkUTK
