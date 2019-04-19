# ubuntu-bash-for-windows

Combined a vbs script that installs the fonts that are present in the current directory in Windows 10 with a PowerShell script that modifies the apperance of the 'Ubuntu on Windows' bash to look like its counterpart in the original Ubuntu. Settings for this found on https://medium.com/@jgarijogarde/make-bash-on-ubuntu-on-windows-10-look-like-the-ubuntu-terminal-f7566008c5c2 and fonts are from http://font.ubuntu.com/ .

The vbs changes or adds setting options only when the [HKCU/Console/*ubuntu*] item exists. Users can open regedit.exe and navigate to [HKCU/Console] to check whether the *ubuntu* subitem exists or not. When the subitem does not exist, open ubuntu.exe and customize the properties. Customizing ubuntu.exe will generate a *ubuntu* subitem. The user can then run the vbs script for automatically customization.

If the vbs script does not work, use the wsl_ubuntu.reg file. First open regedit.exe and navigate to [HKCU/Console] in which find the subitem which match *ubuntu* and copy the item name, e.g. *C:_Program Files_WindowsApps_CanonicalGroupLimited.UbuntuonWindows_1804.2018.817.0_x64__79rhkp1fndgsc_ubuntu.exe* . Open the reg file with whatever the text editor you like and edit to replace the *ubuntu* with the subitem name. Then save and import the edited reg file into reg database.
