
## Image Setup Editor

### -gd
<span style="color:#404040">Argument "\-gd" : Generate </span>  <span style="color:#FF0000">Setup Default Setting</span>  <span style="color:#404040"> to a file</span>

* <span style="color:#262626">Type command "H2OUVE \-gd \<file> \[ \-i \<ImageFile> \]"  </span>
  * <span style="color:#262626">All the default settings of setup menu will be listed in the output file\, And the contents format of file is the same with SCU Editor\.  </span>
    * <span style="color:#262626">Runtime</span>
    * <span style="color:#262626">Image file</span>

![](img/H2OUVE_User_Guide78.png)

![](img/H2OUVE_User_Guide79.png)

![](img/H2OUVE_User_Guide80.png)

![](img/H2OUVE_User_Guide81.png)

<span style="color:#404040">Argument "\-gd" : Generate </span>  <span style="color:#FF0000">Setup Default Setting</span>  <span style="color:#404040"> to a file</span>

* In ApolloLake and GemiLake\, we need to add " <span style="color:#FF0000">\-fba</span> " to make sure command will work\.
  * This due to when we search region by FDM\, we need to know where is the base address
  * FDM only provide offset\, not actual address
  * In those platform\, we need to assign base address to FDM address due to BIOS architecture

<span style="color:#404040">Argument "\-sd" : Modify Setup Default Setting with the data in the file</span>

* <span style="color:#262626">Type command "H2OUVE \-sd \<file> \-i \<ImageFile> \-out \<NewImageFile>" </span>
  * <span style="color:#262626">Argument "\-out" is optional to save as the other new image name\. </span>

![](img/H2OUVE_User_Guide82.png)

![](img/H2OUVE_User_Guide83.png)

### -sd
<span style="color:#404040">Argument "\-sd" : Modify </span>  <span style="color:#FF0000">Setup Default Setting</span>  <span style="color:#404040"> with the data in the file</span>

* In ApolloLake and GemiLake\, we need to add " <span style="color:#FF0000">\-fba</span> " to make sure command will work\.
  * This due to when we search region by FDM\, we need to know where is the base address
  * FDM only provide offset\, not actual address
  * In those platform\, We need to assign Base Address to FDM Address due to BIOS architecture

<div style="page-break-after: always;"></div>

### -gstr
<span style="color:#404040">Argument "\-gstr" : </span>  <span style="color:#FF0000">Generate strings</span>  <span style="color:#404040"> which in Setup page to a file\.</span>

* <span style="color:#262626">Strings with two type in setup page\.</span>
  * <span style="color:#262626">Setup utility</span>
    * <span style="color:#262626">> H2OUVE -gstr \<ImageFile> \<file> \-s</span>
  * <span style="color:#262626">Setup browser</span>
    * <span style="color:#262626">> H2OUVE -gstr \<ImageFile> \<file> -b</span>

![](img/H2OUVE_User_Guide84.png)

![](img/H2OUVE_User_Guide85.png)

![](img/H2OUVE_User_Guide86.png)

![](img/H2OUVE_User_Guide87.png)

Content of output file with "\-gstr" argument

<span style="color:#262626">Modify the string in the " "\, and then "\-sstr" can apply the string base on this file\.</span>

<span style="color:#262626">It has word limit at the top of whole strings</span>

<span style="color:#262626">The first number in brackets means which package it belong to \(For string of setup utility\)\.</span>

The remaining  character that can be added\.

Strings for setup utility

![](img/H2OUVE_User_Guide88.png)

![](img/H2OUVE_User_Guide89.png)

Strings for setup browser

![](img/H2OUVE_User_Guide90.png)

![](img/H2OUVE_User_Guide91.png)

### -sstr
<span style="color:#404040">Argument "\-sstr" : </span>  <span style="color:#FF0000">Save strings</span>  <span style="color:#404040"> to Setup page with the data in the file\.</span>

* <span style="color:#262626">Argument "\-out" is supported for this argument\. \(optional\)</span>
  * <span style="color:#262626">Setup utility</span>
    * <span style="color:#262626">> H2OUVE -sstr \<file> \<ImageFile> \-s </span>
  * <span style="color:#262626">Setup browser</span>
    * <span style="color:#262626">> H2OUVE -sstr \<file> \<ImageFile> \-b</span>

![](img/H2OUVE_User_Guide92.png)

![](img/H2OUVE_User_Guide93.png)

![](img/H2OUVE_User_Guide94.png)

![](img/H2OUVE_User_Guide95.png)

<span style="color:#404040">Example for Argument "\-sstr"\. </span>

* <span style="color:#262626">1\. Modify content of output file with "\-gstr" argument\.</span>
  * <span style="color:#262626">This example is for setup utility type\(\-s\)</span>
* <span style="color:#262626">2\. Save string to setup page in image file\.</span>
  * <span style="color:#262626">>H2OUVE -sstr \<file> \<ImageFile> \-s</span>
* <span style="color:#262626">3\. Use the image file to update BIOS\.</span>
* <span style="color:#262626">4\. The string has changed\. </span>

![](img/H2OUVE_User_Guide96.png)

![](img/H2OUVE_User_Guide97.png)

![](img/H2OUVE_User_Guide98.png)

![](img/H2OUVE_User_Guide99.png)

<span style="color:#404040">Example for Argument "\-sstr"\. </span>

* <span style="color:#262626">1\. Modify content of output file with "\-gstr" argument\.</span>
  * <span style="color:#262626">This example is for setup utility type\(\-s\)</span>
* <span style="color:#262626">2\. Save string to setup page in image file\.</span>
  * <span style="color:#262626">>H2OUVE -sstr \<file> \<ImageFile> \-s</span>
* <span style="color:#262626">3\. Use the image file to update BIOS\.</span>
* <span style="color:#262626">4\. The string has changed\. </span>

![](img/H2OUVE_User_Guide100.png)

![](img/H2OUVE_User_Guide101.png)

![](img/H2OUVE_User_Guide102.png)

![](img/H2OUVE_User_Guide103.png)

### -dpw
<span style="color:#404040">Argument "\-dpw" : </span> Set a default password in bios image <span style="color:#404040">\.</span>

* <span style="color:#262626">Argument "\-out" is supported for this argument\. \(optional\)</span>
  * <span style="color:#262626">Admin password</span>
    * <span style="color:#262626">> H2OUVE -dpw \-admin "12345" \-i \<ImageFile></span>
  * <span style="color:#262626">User password</span>
    * <span style="color:#262626">> H2OUVE -dpw \-admin "12345" \-user "12345" \-i \<ImageFile></span>

![](img/H2OUVE_User_Guide104.png)

![](img/H2OUVE_User_Guide105.png)

### -comp
<span style="color:#404040">Argument "\-comp" : Compare two Setup setting files</span>

* <span style="color:#262626">Type command "H2OUVE \-comp \<Savefile> \<Setting1\.txt> \<Setting2\.txt>"</span>
  * <span style="color:#262626">Sample Output</span>
  * <span style="color:#262626">Different item example</span>

![](img/H2OUVE_User_Guide106.png)

![](img/H2OUVE_User_Guide107.png)

<span style="color:#404040">Argument "\-comp" : Compare two Setup setting files</span>

* <span style="color:#262626">Type command "H2OUVE \-comp \<Savefile> \<Setting1\.txt> \<Setting2\.txt>"</span>
  * <span style="color:#262626">Missing item example</span>
  * <span style="color:#262626">Add item example</span>

![](img/H2OUVE_User_Guide108.png)

![](img/H2OUVE_User_Guide109.png)

<div style="page-break-after: always;"></div>
