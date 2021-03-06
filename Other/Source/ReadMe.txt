
;= NOTES
;= ################
1. Do not associate through 7-Zip.
   Doing so will cause trash in the registry.
   Enable associations via 7-ZipPortable.ini (read ASSOCiATiONS below)
   Refer to 7-ZipPortable\App\AppInfo\Launcher\7-ZipPortable.ini

2. Do not enable Context Menu through 7-Zip.
   ie. Tools > Options > 7-Zip Tab > Integrate 7-Zip to shell context menu
   Doing so will cause trash in the registry.
   Enable by setting ShellExtension= to true.
   ie. 7-ZipPortable\7-ZipPortable.ini

The Launcher has been designed w/out Administrative Privilege dependency.

Features which require elevated privileges have been made optional.

You must specify to the Launcher, so it knows to cleanup after these features.

;= OFFLINE INSTALL
;= ################
This method will bypass online downloading.

For instance: 
- if you would like to install with a specific version..
- if your Internet connection is incompatible..
- if the Installer is not working correctly..
- or if you're a tech. who plans to install on multiple machines.

1. Download desired variant from: http://www.7-zip.org/
2. x32: rename to 7zip.exe or 7zip.msi depending on filetype
   x64: rename to 7zip64.exe or 7zip64.msi depending on filetype
3. Place renamed file next to 7-ZipPortable_16.04_Multilingual.paf.exe
4. Install as normal

OPTIONALLY: pass -x or /x for extraction only.

;= ASSOCIATIONS
;= ################
It is super easy to add associations.

1. Navigate to: 7-ZipPortable\App\AppInfo\Launcher
2. Open 7-ZipPortable.ini with Notepad or any text editor
3. Scroll down to: [Associations]
4. Simply add desired assocation underneath in numerical sequential order.

ie.
	[Associations]
	1=7z
	2=001
	3=rar
	4=zip
	5=iso
	6=bzip
	7=tar
	8=cab

Supported filetypes:
001, 7z, arj, bz2, bzip2, cab, cpio, deb, dmg, fat, gz, gzip, hfs, iso, lha,
lzh, lzma, ntfs, rar, rpm, squashfs, swm, tar, taz, tbz, tbz2, tgz, tpz, txz,
vhd, wim, xar, xz, z, zip.

NOTES:
• Adding too many can impact launch time.
• Windows XP cache icons which are visible even after exiting 7-Zip.
• Windows 8.0 is problematic and may require unlocking for some filetypes:
  - Double-click file > select 7-Zip from list
  this is due to Win8.0's implementation of a hash id for associations
• Do not associate through 7-Zip!, which will leave trash in the registry.
• In addition, SendTo is available for un-associated but supported filetypes.

;= PRESERVE
;= ################
http://portableapps.com/manuals/PortableApps.comLauncher/ref/paf/installer.html

If there are any directories or files you'd like to preserve during upgrades or reinstalls:
- enter it in ..\App\AppInfo\installer.ini

Files example:
	[FilesToPreserve]
	PreserveFile1=App\file

Directories example:
	[DirectoriesToPreserve]
	PreserveDirectory1=App\directory

In addition, [DirectoriesToPreserve] & [FilesToPreserve] configurations are preserved.