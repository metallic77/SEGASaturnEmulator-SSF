Required environment
  Android devices
    CPU is ARM with 4 or more cores and NEON
    OS: Android 6.0 or later
    OpenGL ES 3.1 support
      No problem with recent devices
  Gamepad
    Any pad that returns standard key codes should work.
    Android keycode button B is confirm, keycode button A is cancel



* Recommended environment
  The latest high-end devices
    CPU with 8 or more cores



〇CD image
  Supports CUE+BinaryImage and CHD



Batch files
  The following batch file can only be used if you enable developer options and turn on USB debugging.
    install_apk.bat
    uninstall_apk.bat
    install_image.bat
    delete_data.bat
    delete_ini.bat
    get_ini.bat
    push_ini.bat



Installation
  If you are using Android 8.0 or below, go to Settings -> Security -> Turn on Unknown Sources
  Install the app with install_apk.bat
  Give the app permission to access storage
  Copy the CD image file to the data folder.
  Transfer the files in the data folder to the device using install_image.bat
  If you cannot use the batch file, follow the steps below:
    Connect the PC and device with a USB cable (if the device recognizes it, it's OK)
      If you cannot view the contents of the storage in Explorer, change the device's USB settings to file transfer.
    There is a folder called Download on your device, so copy the apk file there.
    Launch a file manager on your device, navigate to the apk file folder, select it, and install it.
    Give the app permission to access storage
    Run it once (it will create folders etc. that the app uses)
    Unplug and plug in the USB cable (if you do not unplug it, the changes may not be reflected)
    The /Android/data/com.xrea.g2.aaaaaaaa.ssf/files folder will be created on your device (the files folder will be where the images are stored).
      If the folder is not created, create it manually.
        If creation fails, or the folder does not appear even after creation, access restrictions may be set on the device.
        In that case, use a batch file
    Copy the CD image file to the files folder
  External SD cards are not supported.



*Uninstall
  Delete all data with delete_data.bat
  Delete all configuration files with delete_ini.bat
  Delete all apps and data with uninstall_apk.bat
  If the batch file cannot be used, please delete it from the app management on your device.
    You may need to manually delete the /Android/data/com.xrea.g2.aaaaaaaa.ssf folder.



〇 Execution
  First, an image list will be displayed, so select
  Shader initialization begins (this may take some time)
  Start the game♪



〇Options
  After the game starts, touch the center of the screen to display the options menu.
  The settings are basically the same as the Windows version.
    There are many options in the configuration file itself, but only the ones shown are functional.
  Use up and down to select an item, and left and right to change the value
  Items marked with * require a restart
    Save is done when you exit the options menu, so please restart after exiting the menu.
  You can assign buttons with Controller Remap
    For buttons that do not need to be assigned, touch the screen.
  To exit the menu, press the cancel button or touch the screen.
  Options can also be opened on the game selection screen
    In this case, the settings are stored in SSF.ini.
    SSF.ini is the default value
  Android-specific options:
    ・CS Group Thread Y
      Specifies the number of group threads for the compute shader
      The higher the number, the faster the processing, but some devices may not work with a large number of threads.



〇Other
  adb.exe, AdbWinApi.dll, AdbWinUsbApi.dll are the same files included in the Android SDK.
  Does not sleep while running
    Since there is almost no touch operation, the program prohibits sleep.
  The BIOS is not used by default.
    You can use it by rewriting the configuration file and transferring the BIOS.
  It's quite unstable
    If it moves, consider yourself lucky.



