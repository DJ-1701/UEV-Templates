# UEV-Templates

## UEV Basics

In this section is information on UE-V (User Experience Virtualisation) setup based conversations and guidance by EduGeek's awesome Arcolite (Thanks again!)

Requirements

- Updated Windows 10 ADMX policy templates on SYSVOL.

- To enable UEV on a Windows 10 machine, you need to run the following PowerShell script on said machine:
"C:\ProgramData\Microsoft\UEV\Scripts\RegisterInboxTemplates.ps1"

Computer Policy Settings

Policies/Administrative Templates/Windows Components/Microsoft User Experience Virtualization
Set Enable UEV - Enabled, and tick Auto-register inbox templates.

If you have some custom settings templates you can also set the 'Settings template catalogue path'.

User Policy Settings

Policies/Administrative Templates/Windows Components/Microsoft User Experience Virtualization

Update 'Synchronize Windows settings' to set if you require Desktop settings, Ease of access, Themes, Roaming Credentials and/or Network Printers data shared between machines.

By default, UEV data is stored in %homeshare% under a folder called SettingsPackages. You can edit 'Settings storage path' to specify a location where this folder gets created instead if required. Please note that it would be wise to include the %username% in the path you wish to use. Also note that the SettingsPackages folder is visible by default.

Policies/Administrative Templates/Windows Components/Microsoft User Experience Virtualization/Applications

In here you can disable or force enable applications to share information between PCs.

## UEV Templates for Google Chrome and Microsoft Edge (aka Edgium)

The templates for Google Chrome and Microsoft Edge for UEV are set to remember basic information such as the Preferences (including Window Size and if you have the Bookmark bar showing), Bookmarks, Favicon images for the Bookmarks and Cookies to remember previously typed usernames for websites (i.e. Office 365).

These are not set to remember history, cache or passwords.
