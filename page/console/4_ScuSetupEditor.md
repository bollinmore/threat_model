## SCU(Setup) Editor

### -gs
<span style="color:#404040">Argument "\-gs" : Generate </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> to a file</span>

* <span style="color:#262626">Type command "H2OUVE \-gs \<file>"  </span>
  * <span style="color:#262626">The settings of setup menu will be listed in the output file\.</span>
* <span style="color:#262626">Type command "H2OUVE \-gs \<file> \-all"</span>
  * <span style="color:#262626">It will dump all settings of setup menu\, include suppressed items\.</span>
  * <span style="color:#FF0000"> __\-all for read\-only dump\, not support import via the file which dump by \-all parameter\.__ </span>

![](img/H2OUVE_User_Guide11.png)

![](img/H2OUVE_User_Guide12.png)

<span style="color:#404040">Argument "\-gs" : Generate </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> to a file</span>

* <span style="color:#262626">Append "\-\-v" behind \-gs to show parent form name\.</span>

![](img/H2OUVE_User_Guide13.png)

<span style="color:#404040">Argument "\-gs" : Generate </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> to a file</span>

<span style="color:#262626">Item with grayout true will display without \[\] means this item could not be modify</span>

![](img/H2OUVE_User_Guide14.png)

Content of output file about SCU

* <span style="color:#262626">Put the "\*" between "\[" and "\]" to change the setting </span>
  * <span style="color:#262626">This is for "Oneof" Question in VFR</span>
* <span style="color:#262626">Update the number between "\[" and "\]" to change the setting\. The value must be in between maximum and minimum\. </span>
  * <span style="color:#262626">This is for "Numeric " Question in VFR</span>

![](img/H2OUVE_User_Guide15.png)

![](img/H2OUVE_User_Guide16.png)

Content of output file about SCU

* <span style="color:#262626">About "Text" Question</span>
  * <span style="color:#262626">User Only CAN modify the content of brackets\[ \] to assign data\.</span>

![](img/H2OUVE_User_Guide17.png)

![](img/H2OUVE_User_Guide18.png)

![](img/H2OUVE_User_Guide19.png)

![](img/H2OUVE_User_Guide20.png)

Content of output file about SCU

* <span style="color:#262626">Modify Boot Device Type Order</span>
  * <span style="color:#262626">Modify the number of brackets\[ \] to change the order\.</span>
  * <span style="color:#262626">Do NOT Modify the numbers of BootTypeOrderSize and BootTypeOrderOffset\.</span>

Content of output file about SCU

* <span style="color:#262626">Modify Boot Order</span>
  * <span style="color:#262626">Modify the number of brackets\[ \] to change the order\.</span>
  * <span style="color:#262626">Legacy and EFI are two group\, and there is "\<Legacy>" or "\<EFI>" before the device name\.   </span>
  * <span style="color:#262626">User only can swap the number of device which in the same group\.</span>
  * <span style="color:#262626">If the boot device is not exist just like EFI DVD/CDROM or EFI Network \, and they will keep at the end of list\.</span>

![](img/H2OUVE_User_Guide21.png)

![](img/H2OUVE_User_Guide22.png)

Content of output file about SCU

* <span style="color:#262626">Add Password</span>
  * <span style="color:#262626">Keep the brackets\[ \] of Current Password clear\.</span>
  * <span style="color:#262626">Modify the content of brackets\[ \] of New Password and Repeat Password to set the password\.</span>
* <span style="color:#262626">Modify Password</span>
  * <span style="color:#262626">Modify the content of brackets\[ \] of Passwords to modify the password\.</span>

![](img/H2OUVE_User_Guide23.png)

![](img/H2OUVE_User_Guide24.png)

![](img/H2OUVE_User_Guide25.png)

![](img/H2OUVE_User_Guide26.png)

Content of output file about SCU

* <span style="color:#262626">Clear Password</span>
  * <span style="color:#262626">Fill the content of brackets\[ \] of Current Password\.</span>
  * <span style="color:#262626">Keep the brackets\[ \] of New Password and Repeat Password clear\.</span>

![](img/H2OUVE_User_Guide27.png)

![](img/H2OUVE_User_Guide28.png)

### -ss
<span style="color:#404040">Argument "\-ss" : Modify </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> with the data in the \(input\) file</span>

<span style="color:#262626">Type command "H2OUVE \-ss \<file>"  </span>

![](img/H2OUVE_User_Guide29.png)

![](img/H2OUVE_User_Guide30.png)

<span style="color:#404040">Argument "\-ss" : Modify </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> with the data in the \(input\) file</span>

<span style="color:#262626">Item with </span>  <span style="color:#FF0000">grayout true</span>  <span style="color:#262626"> will display without \[\]\. This kind of item will ignore during \-ss process</span>

![](img/H2OUVE_User_Guide31.png)

### -gbd
<span style="color:#404040">Argument "\-gbd" : Dump </span>  <span style="color:#FF0000">Current Boot device</span>  <span style="color:#404040"> to file</span>

<span style="color:#262626">Type command "H2OUVE \-gbd \<file>"  </span>

![](img/H2OUVE_User_Guide32.png)

![](img/H2OUVE_User_Guide33.png)

![](img/H2OUVE_User_Guide34.png)

![](img/H2OUVE_User_Guide35.png)

### -sbd
<span style="color:#404040">Argument "\-sbd" : Save </span>  <span style="color:#FF0000">Current Boot device</span>  <span style="color:#404040"> by input file</span>

<span style="color:#262626">Type command "H2OUVE \-sbd \<file>"  </span>

![](img/H2OUVE_User_Guide36.png)

![](img/H2OUVE_User_Guide37.png)

![](img/H2OUVE_User_Guide38.png)

### -gbt
<span style="color:#404040">Argument "\-gbt" : Dump </span>  <span style="color:#FF0000">Current Boot Device Type</span>  <span style="color:#404040"> to file</span>

<span style="color:#262626">Type command "H2OUVE \-gbt \<file>"  </span>

![](img/H2OUVE_User_Guide39.png)

![](img/H2OUVE_User_Guide40.png)

<span style="color:#404040">Argument "\-gbt" : Dump </span>  <span style="color:#FF0000">Current Boot Device Type</span>  <span style="color:#404040"> to file</span>

* <span style="color:#262626">With newer BIOS file would be like following two type</span>
  * <span style="color:#262626">Legacy and UEFI using same data</span>
  * <span style="color:#262626">Legacy and UEFI using different data\.</span>

![](img/H2OUVE_User_Guide41.png)

![](img/H2OUVE_User_Guide42.png)

![](img/H2OUVE_User_Guide43.png)

![](img/H2OUVE_User_Guide44.png)

### -sbt
<span style="color:#404040">Argument "\-sbt" : Save </span>  <span style="color:#FF0000">Current Boot Device Type</span>  <span style="color:#404040"> by input file</span>

<span style="color:#262626">Type command "H2OUVE \-sbt \<file>"  </span>

![](img/H2OUVE_User_Guide45.png)

<span style="color:#404040">Argument "\-sbt" : Save </span>  <span style="color:#FF0000">Current Boot Device Type</span>  <span style="color:#404040"> by input file</span>

* <span style="color:#262626">With newer BIOS Boot Device Type Order also could be able to modify device status\.</span>
  * <span style="color:#262626">The following word in red square is reserved word for tool\. Do not modify it\.</span>

![](img/H2OUVE_User_Guide46.png)

![](img/H2OUVE_User_Guide47.png)

![](img/H2OUVE_User_Guide48.png)

![](img/H2OUVE_User_Guide49.png)

### -ms
<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Type command "H2OUVE \-ms \-fi \<Item Name> \[\-op \<Option> \-idx \<index>\]" </span>
  * <span style="color:#262626"> Item Name is case\-sensitive\.</span>
* <span style="color:#262626">If there is nothing change\, it will show this message</span>
* Without -op Will be read mode.

![](img/H2OUVE_User_Guide50.png)

![](img/H2OUVE_User_Guide51.png)

![](img/H2OUVE_User_Guide52.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Modify Boot Device Type Order</span>
  * <span style="color:#262626">According the name strings to modify</span>
  * <span style="color:#262626">    the Boot Device Type Order\.</span>
  * <span style="color:#FF0000">MUST </span> use "\," to separate the name
  * strings  <span style="color:#FF0000">WITHOUT</span>  redundant space\.

![](img/H2OUVE_User_Guide53.png)

![](img/H2OUVE_User_Guide54.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Modify Boot Device Type Order</span>
  * <span style="color:#262626">If user entered an invalid input\, then utility shows the current setting\.</span>

![](img/H2OUVE_User_Guide55.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Modify Boot Device Type Order</span>
  * <span style="color:#262626">The following message means you need to set Boot Device Type by \-sbt</span>

![](img/H2OUVE_User_Guide56.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Modify Boot Order</span>
  * <span style="color:#262626">According the number in the </span>
  * <span style="color:#262626">   brackets\( \) to modify the Boot </span>
  * <span style="color:#262626">   Order\. </span>
  * <span style="color:#262626">The rule for modify Boot Order has been explained at here\.</span>

![](img/H2OUVE_User_Guide57.png)

![](img/H2OUVE_User_Guide58.png)

![](img/H2OUVE_User_Guide59.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Modify Boot Order</span>
  * <span style="color:#262626">If user entered an invalid input\, and utility will show the current setting\.</span>

![](img/H2OUVE_User_Guide60.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">Add Password</span>
  * <span style="color:#262626">Command format after "\-op" :  ""  "Password"</span>
* <span style="color:#262626">Change Password</span>
  * <span style="color:#262626">Command format after "\-op" :  "Old Password"  "New Password"</span>
* <span style="color:#262626">Clear Password</span>
  * <span style="color:#262626">Command format after "\-op" :  "Old Password"  ""</span>

![](img/H2OUVE_User_Guide61.png)

![](img/H2OUVE_User_Guide62.png)

![](img/H2OUVE_User_Guide63.png)

<span style="color:#404040">Argument "\-ms" : Modify specific item of </span>  <span style="color:#FF0000">Current Setup Setting</span>  <span style="color:#404040"> </span>

* <span style="color:#262626">\-ms command will modify first item which match field name\.</span>
* <span style="color:#FF0000">\-idx</span>  is used to update a specific item where multiple items\(the name is the same\) exist\.
  * <span style="color:#262626">Optional parameter\, the default is zero</span>
  * You may need to count the number in the output file generated by " <span style="color:#FF0000">\-gs</span> " command
* <span style="color:#262626">Example</span>
  * There are two " <span style="color:#FF0000">DevSleep0 Port Number</span> " items in the file below
  * <span style="color:#262626">their index is "idx 0" and "idx 1" separately\.</span>
  * <span style="color:#262626">If item with </span>  <span style="color:#FF0000">index</span>  <span style="color:#262626"> is not found\, it will show error</span>

![](img/H2OUVE_User_Guide64.png)

![](img/H2OUVE_User_Guide65.png)

### -cdi
<span style="color:#404040">Argument "\-cdi" : Report duplicate items and their locations in BIOS Setup Utility</span>

* <span style="color:#262626">Type command "H2OUVE \-cdi"</span>
  * <span style="color:#262626">List all duplicate items in setup settings on screen</span>
* <span style="color:#262626">Type command "H2OUVE \-cdi \[File\]"</span>
  * <span style="color:#262626">Dump all duplicate items in setup setting to specified file</span>

![](img/H2OUVE_User_Guide66.png)

![](img/H2OUVE_User_Guide67.png)

<span style="color:#404040">Argument "\-cdi" : Report duplicate items and their locations in BIOS Setup Utility</span>

* <span style="color:#262626">Type command "H2OUVE \-cdi \-n \<Name>"</span>
  * <span style="color:#262626">List locations if any item in setup setting has same name</span>
* <span style="color:#262626">Type command "H2OUVE \-cdi -i \<ImageFile>"</span>
  * <span style="color:#262626">List all duplicate items in setup setting of Bios Image File</span>

![](img/H2OUVE_User_Guide68.png)

![](img/H2OUVE_User_Guide69.png)

![](img/H2OUVE_User_Guide70.png)

<span style="color:#404040">Argument "\-cdi" : Report duplicate items and their locations in BIOS Setup Utility</span>

* <span style="color:#262626">Type command "H2OUVE \-cdi \[\-n \<Name>\] \[\-i \<ImageFile>\]"</span>
  * <span style="color:#262626">List locations if any item in setup setting of bios image file has same name</span>
  * <span style="color:#262626">List all duplicate items</span>
  * <span style="color:#262626">List all duplicate items in image file</span>

![](img/H2OUVE_User_Guide71.png)

![](img/H2OUVE_User_Guide72.png)

![](img/H2OUVE_User_Guide73.png)

![](img/H2OUVE_User_Guide74.png)

### -bfirst
<span style="color:#404040">Argument "\-bfirst" : Make device to first boot\.</span>

* <span style="color:#262626">Type command "H2OUVE \-bfirst \<name>"</span>
  * <span style="color:#262626">Set input name of boot device to be first boot device</span>

![](img/H2OUVE_User_Guide75.png)

### -uvebf
<span style="color:#404040">Argument "\-uvebf" : Enable/Disable H2OUVE functions in BIOS for subsequent boot</span>

* <span style="color:#262626">Type command "H2OUVE \-uvebf \<Enabled|Disabled>"</span>
  * <span style="color:#262626">Enable H2OUVE functionalities</span>
  * <span style="color:#262626">Disable H2OUVE functionalities</span>

![](img/H2OUVE_User_Guide76.png)

![](img/H2OUVE_User_Guide77.png)

<div style="page-break-after: always;"></div>
