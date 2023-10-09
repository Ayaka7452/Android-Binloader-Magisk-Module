# Android Binaries Loader
a Magisk module that provides a simplified command-line packager to load various binaries/scripts/executables into Android system

## What is this
This is a command-line utility for Android devices. It provides a packager(bpkg), which enables us to load various
useful utils with a simple package. With this, we are not needed to write a new Magisk module for a single script.

## Installation
Step 1 - Download the latest flashable zip from Release page of this repo;<br />
Step 2 - Put the zip into the sdcard, and flash it via Magisk app;<br />
Step 3 - Launch terminal emulator app, and type 'binloader', it will be initilized;<br />
Step 4 - Reboot and enjoy.<br />

## Usage
bpkg + [Options] + [Parameters]<br />
Options:<br />
>install [path] - install a new package"<br />
    remove [path] - remove a installed package"<br />
    ls - list all installed packages"<br />
    ver - show blcore version information"<br />
    help - show this help screen"<br />

## Make a Package
### Package Structure
─ util_1.0 [folder]<br />
----programs [folder] ---- custom_applet.sh<br />
----pkginfo [file]<br />
### pkginfo File Content
Total 4 tags of this metadata file, they are:<br />
pkgname=[YOUR_APPLET]<br />
version=[APPLET_VERSION]<br />
execpath=[custom_applet.sh]<br />
execname=[NAME_OF_EXEC]<br />
* execname is the spell of the command which you access this applet in terminal to.
### Try Packing a Script
For example we have script 'custom_applet.sh', following these simple steps:<br />
Step 1 - create a folder named 'programs';<br />
Step 2 - copy the 'custom_applet.sh' to 'programs' folder;<br />
Step 3 - write pkginfo file according to the format above;<br />
Step 4 - pack the folder and pkginfo with tar format;<br />
Step 5 - install the tar file using 'bpkg install [file_path]' command and reboot.<br />
After this, you can access your brand new applet via terminal.<br />

## About This Program
This is a command-line utility which is working at Magisk environment, it has been tested working
fine with Magisk v26.3 and Android 13. But still, this utility does NOT responsible for any losses
by using this program, please use it at your own risk.







