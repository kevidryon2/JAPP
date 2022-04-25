# JAPP
A program for patching executables or other files.

## Use cases
For example, JAPP is useful when you want to distribute a mod without distributing the entire game, especially if that game is paid.

## How to use
### Patching
To patch the original game/program/anything else, first you have to put all the files of the software inside a ZIP file.

Then, you apply the patch to the ZIP file and the mask, using the JAPP CLI `japp-patch`.

### Creating a patch and mask
All you need is a ZIP archive of the original program and a ZIP archive of the modified version. Then, you can create a patch (`.jp`) and a mask (`.jm`) using the JAPP CLI `japp-unpatch`

## How it works
### Patching
`japp-patch` sets every byte in the file to be patched to the corresponding byte in the patch file, but only if the corresponding bit in the mask file is set.

### Creating a patch and mask
`japp-unpatch` compares the differences between the original file and the modified file, and stores those differences in the patch and mask files.
