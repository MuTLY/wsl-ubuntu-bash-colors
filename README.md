# WSL Ubuntu bash console colors

## Easy mode

The easiest mode to have Ubuntu colors on the WSL Ubuntu bash is to use the new Windows Terminal app (you can find it on the Windows Store), add the color scheme inside the `windows-terminal-color-scheme.json` file to the custom colors of the Windows Terminal settings and set it as the default for the Ubuntu profile.

## Hard mode

This Powershell script writes new colors to the Windows registry, modifying the Windows Subsystem for Linux (WSL) Ubuntu bash to resemble the colors of the native Ubuntu bash.

1. Install WSL, then reboot;

2. Install Ubuntu from the Microsoft Store;

3. Run Ubuntu bash for the first time, so the Registry keys are created;

4. Install the Ubuntu fonts provided in the `/fonts` folder:
    * Select all the fonts <kbd>Ctrl</kbd> + <kbd>A</kbd>;
    * Right-click on one of the fonts and select `Install for all users`;
    * Click `Yes` if prompted;
    
5. Run the Windows Powershell script as administrator:
    * Type `Powershell` on the Windows search field at the task bar;
    * Right-click the Windows Powershell app icon and choose `Run as administrator`;
    * Click `Yes` if prompted;
    
The script will loop through the **Ubuntu** folders on the `\Computer\HKEY_CURRENT_USER\Console\` folder and set the colors for them (depending on Ubuntu version installed from the Store - it's possible to have several different folders for each Ubuntu installation).

There's a caveat: whenever you install a new WSL Ubuntu version, you'll have to run its bash - so Registry keys are created - and this Powershell script again.

### More information

For more information, refer to these links:

1. https://docs.microsoft.com/en-us/windows/wsl/install-win10
2. https://docs.microsoft.com/en-us/windows/wsl/install-win10#windows-10-fall-creators-update-and-later-install-from-the-microsoft-store
3. https://medium.com/@jgarijogarde/make-bash-on-ubuntu-on-windows-10-look-like-the-ubuntu-terminal-f7566008c5c2
4. https://design.ubuntu.com/font/
5. https://docs.microsoft.com/en-us/windows/terminal/customize-settings/color-schemes
6. https://atomcorp.github.io/themes/
