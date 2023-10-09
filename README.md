# Android Binaries Loader
a Magisk module that provides a simplified command-line packager to load various binaries/scripts/executables into Android system

## What is this
This is a command-line utilities for Android devices. It provides a packager(bpkg), which enables us to load various
useful utils with a simple package. With this, we are not needed to write a new Magisk module for a single script.

## Installation
Step 1 - Download the latest flashable zip from Release page of this repo;<br />
Step 2 - Put the zip into the sdcard, and flash it via Magisk app;<br />
Step 3 - Launch terminal emulator app, and type 'binloader', it will be initilized;<br />
Step 4 - Reboot and enjoy.<br />

## Usage
bpkg + [Options] + [Parameters]<br />
Options:<br />
&emsp;install [path] - install a new package"<br />
&emsp;remove [path] - remove a installed package"<br />
&emsp;ls - list all installed packages"<br />
&emsp;ver - show blcore version information"<br />
&emsp;help - show this help screen"<br />
Type 'bpkg help' at terminal emulator(Termux is recommended) to get more usage information.

## Make a Package
### Package Structure
[Root]
-/pkginfo-[
-/programs
