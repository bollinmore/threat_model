## Variable Editor

### -gv
<span style="color:#404040">Argument "\-gv" : Generate </span>  <span style="color:#FF0000">all the UEFI Variable </span>  <span style="color:#404040">to a file</span>

* <span style="color:#262626">Type command "H2OUVE \-gv \<file> \[ \-i \<ImageFile> \]"</span>
  * <span style="color:#262626">Runtime</span>
  * <span style="color:#262626">Image </span>

![](img/H2OUVE_User_Guide110.png)

![](img/H2OUVE_User_Guide111.png)

![](img/H2OUVE_User_Guide112.png)

![](img/H2OUVE_User_Guide113.png)

#### Image
* Requirement
  * Bios must be Boot t least once and dump from machine, otherwise it will not work.
* Limitation
  * Only support modify existed data image.
  * You can not add/delete variable. Increase variable data size.

__Content of output file with "\-gv" argument __

<span style="color:#262626">
```
File format:
[Index] Variable Name
          GUID:XXXXXXXX\-XXXX\-XXXX\-XXXX\-XXXXXXXXXXXX
          Attributes: 0xXX
          DataSize: 0xXX
          Data:
                00000000: XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX
                00000010: XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX
                ..............   ...............
```
</span>

<span style="color:#262626">Index must start from 001 and be in order\. The number of data bytes must be equal to DataSize\. \(Except data size = 0\)</span>

<span style="color:#262626">"X" represent a hex number\.</span>

<span style="color:#262626">It only supports for modifying the data region of variable on image\.</span>

![](img/H2OUVE_User_Guide114.png)

__Content of output file with "\-gv" argument __

* <span style="color:#262626">Modify Variable data value:</span>
* <span style="color:#262626">Delete Variable: \(Runtime Only\)</span>
  * <span style="color:#262626">Modify </span>  <span style="color:#FF0000">DataSize</span>  <span style="color:#262626"> or </span>  <span style="color:#FF0000">Attributes</span>  <span style="color:#262626"> value to zero\.</span>

![](img/H2OUVE_User_Guide115.png)

![](img/H2OUVE_User_Guide116.png)

![](img/H2OUVE_User_Guide117.png)

![](img/H2OUVE_User_Guide118.png)

__Content of output file with "\-gv" argument __

* <span style="color:#262626">Create/Add some Variables : \(Runtime Only\)</span>
  * <span style="color:#262626">Follow the format to add the description and ensure index number must be in order\.</span>

![](img/H2OUVE_User_Guide119.png)

### -sv
<span style="color:#404040">Argument "\-sv" : Modify </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> with the data in the file</span>

* <span style="color:#262626">Type command "H2OUVE \-sv \<file> \[ \-i \<ImageFile> \]" </span>
  * <span style="color:#262626">Runtime</span>
  * <span style="color:#262626">Image</span>

![](img/H2OUVE_User_Guide120.png)

![](img/H2OUVE_User_Guide121.png)

![](img/H2OUVE_User_Guide122.png)

![](img/H2OUVE_User_Guide123.png)

### -rd
<span style="color:#404040">Argument "\-rd" : Read specific </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> by Name or GUID</span>

<span style="color:#262626">Type command "H2OUVE \-rd -vn \<VarName> \-vg \<GUID>" </span>

![](img/H2OUVE_User_Guide124.png)

### -wt
<span style="color:#404040">Argument "\-wt" : Write specific </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> by Name or GUID with data</span>

<span style="color:#262626">Type command "H2OUVE \-wt \[\-vn "\<VarName>"\] \[\-vg \<GUID>\] \[\-attr \<Attribute>\] <\-by|\-wd|\-dw|\-qw|\-blk|\-astr|\-ustr> "\<VarData>"" </span>

<span style="color:#262626">Then verifiy data with -rd:</span>

![](img/H2OUVE_User_Guide125.png)

![](img/H2OUVE_User_Guide126.png)

### -re
<span style="color:#404040">Argument "\-re" : Delete specific </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> by Name or GUID</span>

<span style="color:#262626">Type command "H2OUVE \-re -vn \<VarName> \-vg \<GUID>" </span>

![](img/H2OUVE_User_Guide127.png)

![](img/H2OUVE_User_Guide128.png)

<span style="color:#404040">Argument "\-re" : Delete specific </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> by Name or GUID</span>

If only type command as "H2OUVE \-re -vn \<VarName>" or "H2OUVE \-re -vg \<GUID>"\, the tool will list all matched Variables one by one and delete it by asking user\.

![](img/H2OUVE_User_Guide129.png)

![](img/H2OUVE_User_Guide130.png)

![](img/H2OUVE_User_Guide131.png)

![](img/H2OUVE_User_Guide132.png)

### -cvl
<span style="color:#404040">Argument "\-cvl" : Check if </span>  <span style="color:#FF0000">Variable</span>  <span style="color:#404040"> is locked</span>

* <span style="color:#262626">Type command "H2OUVE -cvl \[\<File> | -vn \<Name> \-vg \<GUID>\]"</span>
  * Check if variables are locked which list in INI file\. Each variable is described by name and GUID
  * <span style="color:#262626">Check if a specific variable is locked or not</span>

![](img/H2OUVE_User_Guide133.png)

![](img/H2OUVE_User_Guide134.png)

![](img/H2OUVE_User_Guide135.png)

![](img/H2OUVE_User_Guide136.png)

![](img/H2OUVE_User_Guide137.png)

![](img/H2OUVE_User_Guide138.png)

<div style="page-break-after: always;"></div>
