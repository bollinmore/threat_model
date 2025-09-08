## Arguments

| Arguments | Description |
| --------------- | ----------------------------------------------- |
| -? or -h  | Display Help information |
| -fea | Report BIOS supported functionalities. |
| -uvebf \<Enabled\|Disabled\> | Enable/Disable H2OUVE functions in BIOS for subsequent boot. |
| -r \<File\> | Dump the BIOS ROM regions (e.g. Variables, Settings, Strings, etc.) to raw file. |
| -a | Auto Reboot. |
| -l | Load default/original settings for BIOS setup utility. i.e. delete setup and associated variables in BIOS (data section). Same as "Load Default" option under BIOS Setup Utility. |
| -c | Load custom settings for BIOS setup utility. i.e. restore setup variables in BIOS (data section). Same as "Load Custom" option under BIOS Setup Utility. |
| -sc | Save custom settings for BIOS setup utility.\<br /\>i.e. save custom variables in BIOS (data section).\<br /\>Same as "Save Customize default" option under BIOS setup utility. |
| -gs \<File\> \[-all\] | Generate setup utility setting to file. (-all for read-only dump, not support import via the file which dump by -all parameter) |
| -ss \<File\> | Modify setup utility settings from a configuration file. |
| -gd \<File\> | Generate setup utility default setting to file. |
| -sd \<File\> -i \<ImageFile\> | Read saved default configuration file and update setup utility default settings in specified Bios File. |
| -cdi \[File\] \[-n \<Name\>\] \[-i \<ImageFile\>\] | Report duplicate items and their locations in BIOS                         Setup Utility. |
| -gstr \<File\> -s\|-b -i \<ImageFile\> | Modify setup configuration or setup browser strings from specified string-formatted file to Bios Image File. |
| -sstr \<File\> -s\|-b -i \<ImageFile\> | Modify setup configuration or setup browser strings from specified string-formatted file to Bios Image File. |
| -dpw -admin \<Password\> \[-user \<Password\>|-skuid \<SkuId\>\] -i \<BiosImage\> | Add default password to bios image. |
| -gbd \<File\> \[-i \<BiosImageFile\] | Dump current boot device setting to boot-device file. |
| -sbd \<File\> \[-i \<BiosImageFile\] | Modify current boot device from specified boot-device file. |
| -gbt \<File\> \[-i \<BiosImageFile\] | Dump current Boot Device Type Order setting to Boot Device Type Order file. |
| -sbt \<File\> \[-i \<BiosImageFile\] | Modify current Boot Device Type Order from specified Boot Device Type Order file. |
| -bfirst \<name\> \[-t\] | Make device to first boot. |
| -gv \<File\> | Dump variable information to a variable record file. |
| -sv \<File\> | Update variables from specified variable record file. |
| -rd \[-vn "\<VarName\>"\] \[-vg \<GUID\>\] | Read a variable by name or GUID. |
| -wt \[-vn "\<VarName\>"\] \[-vg \<GUID\>\] \[-attr \<Attribute\>\] \<-by\|-wd\|-dw\|-qw\|-blk\|-astr\|-ustr\> "\<VarData\>" | Write a variable by name or GUID.(If the attribute is not specified, then the default will be 0x7(NV|BS|RT)) \<br /\>by: byte, wd: word, dw: dword, qw: qword, blk: block data(01h 02h ...), astr: ascii string, ustr: unicode string |
| -re \[-vn \<VarName\>\] \[-vg \<GUID\>\] | Remove a variable by name or GUID. |
| -cvl \<File \| -vn \<Name\> -vg \<GUID\>\> | Check variables are locked by input a variable name-guid file or by input a specified name-guid. |
| -dbos | Display Boot Order Sequence. |
| -cnvs | Clear NV Spare data. |
| -cvhc | Check Variable Header Continuity. |
| -vorv \[-count\] | Variable store Out of Region Verification. |
| -cvur \[-count\] | Check Variable Usage situation by Reboot. |
| -cvus \[-count\] | Check Variable Usage situation by Shutdown. |
| -cvrd \[-count\] | Check Variable Reclamation on Dxe. |
| -cvrs \[-count\] | Check Variable Reclamation on Smm. |
| -cvsf \[-count\] \[-bc\] | Check Variable fill Setting (fill 0xFF). |
| -cvs0 \[-count\] \[-bc\] | Check Variable fill Setting (fill 0x00). |
| -cgnv | Check GetNextVariablename on RT. |
| -cssr | Check Synchronization between Smm and RT SetVariable. |
| -cvsd | Check Variable is existing while changing variable State to Deleteed_transition in Smm variable services. |
| -sipi | Send IPI. |
| -count \<number\> | Specify the count number. |
| -bc \<number\> | Partial erase - Number * block size (0x1000) |

<div style="page-break-after: always;"></div>
