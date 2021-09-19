# FlashPlayerExt
A flash player extension for firefox to run swf files.

## How To Install
1. Run the setup file to install the flash player
2. Open Firefox, Click on the ham-menu and then Add-ons and themes
3. Click on the gear icon, Select "Install Add-on From File"

Now go to any website that has swf files in it and it will show a "Run This Flash" button.

## Source Code:
you can get the source code of the extension by renaming the file to .zip and extracting it.
The setup file will install the adobe flash player and some registry keys.
the following keys will be installed under HKEY_CLASSES_ROOT:
```
runSWF\
  (default) = runSWF
  URL Protocol = 
  DefaultIcon\
    (default) = %localappdata%\FlashPlayer\flashplayer.exe,1
  shell\
    (default) = open
    open\
      (default) = 
      command\
        (default) = cmd /V /C "set file=%1&&start %localappdata%\FlashPlayer\flashplayer.exe !file:runswf:=!"
```
If you don't trust the setup file you can download the Adobe Flash Player or any other player, add the keys above to the registry,
modify the value of the default key under "command" and set the path to the player on your machine.
