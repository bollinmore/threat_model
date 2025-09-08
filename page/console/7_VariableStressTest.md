## Variable Stress Test

### -dbos
<span style="color:#404040">Argument "\-dbos" : </span>  <span style="color:#FF0000">Display Boot Order </span>  <span style="color:#FF0000">Sequence</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-dbos"</span>

<span style="color:#262626">Display the Boot Order sequence</span>

![](img/H2OUVE_User_Guide139.png)

![](img/H2OUVE_User_Guide140.png)

### -cnvs
<span style="color:#404040">Argument "\-cnvs" : </span>  <span style="color:#FF0000">Clear NV Spare data</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cnvs"</span>

<span style="color:#262626">Clear NV Spare with fill in 0xFF\.</span>

<span style="color:#262626">This function is not supported in secure flash mode\.</span>

![](img/H2OUVE_User_Guide141.png)

![](img/H2OUVE_User_Guide142.png)

### -cvhc
<span style="color:#404040">Argument "\-cvhc" : </span>  <span style="color:#FF0000">Check Variable Header Continuity</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvhc"</span>

<span style="color:#262626">Auto detect the platform is Secure Boot or not\, then check variable header continuity\.</span>

<span style="color:#262626">If the variable header has checksum or variable sequence is non\-contiguous\, show the error message\.</span>

![](img/H2OUVE_User_Guide143.png)

![](img/H2OUVE_User_Guide144.png)

### -vorv
<span style="color:#404040">Argument "\-vorv" : </span>  <span style="color:#FF0000">Variable store Out of Region Verification</span>  <span style="color:#404040">\.</span>

* <span style="color:#262626">Type command "H2OUVE \-</span>  <span style="color:#262626">vorv</span>  <span style="color:#262626"> \[\-count\]"</span>
* The argument \-count specify number of times <span style="color:#262626">\.</span>
* <span style="color:#262626">This function is not supported in </span> Secure Flash  <span style="color:#262626">mode\.</span>
* <span style="color:#262626">There are 2 cases to testing:</span>
  * <span style="color:#262626">The data size of last one variable is out of variable storage region\.</span>
  * <span style="color:#262626">The last variable has only </span> 8\-bytes header <span style="color:#262626">\.</span>  <span style="color:#262626">\(</span>  <span style="color:#262626">StartID</span>  <span style="color:#262626">\, State\, and Attributes\)</span>
  * <span style="color:#262626">The system should reclaim and remove those incomplete variables\.</span>

<span style="color:#404040">Argument "\-vorv" : </span>  <span style="color:#FF0000">Variable store Out of Region Verification</span>  <span style="color:#404040">\.</span>

![](img/H2OUVE_User_Guide145.png)

![](img/H2OUVE_User_Guide146.png)

![](img/H2OUVE_User_Guide147.png)

### -cvur
<span style="color:#404040">Argument "\-cvur" : </span>  <span style="color:#FF0000">Check Variable Usage situation by Reboot</span>  <span style="color:#404040">\.</span>

* <span style="color:#262626">Type command "H2OUVE \-cvur \[\-count\]"</span>
* <span style="color:#262626">The argument \-count used to specified the number of times\.</span>
* <span style="color:#262626">To detect that BIOS updates the variables during the POST time\.</span>
* <span style="color:#262626">There are 3 situations:</span>
  * <span style="color:#262626">Variables are added or modified : list those variables</span>
  * <span style="color:#262626">System do reclaim : show system do reclaim message</span>
  * <span style="color:#262626">No change : pass the test</span>

<span style="color:#404040">Argument "\-cvur" : </span>  <span style="color:#FF0000">Check Variable Usage situation by Reboot</span>  <span style="color:#404040">\.</span>

![](img/H2OUVE_User_Guide148.png)

![](img/H2OUVE_User_Guide149.png)

![](img/H2OUVE_User_Guide150.png)

### -cvus
<span style="color:#404040">Argument "\-cvus" : </span>  <span style="color:#FF0000">Check Variable Usage situation by Shutdown</span>  <span style="color:#404040">\.</span>

* <span style="color:#262626">Type command "H2OUVE \-cvus \[\-count\]"</span>
* <span style="color:#262626">The argument \-count used to specified the number of times\.</span>
* <span style="color:#262626">To detect that BIOS updates the variables during the POST time\.</span>
* <span style="color:#262626">There are 3 situations:</span>
  * <span style="color:#262626">Variables are added or modified : list those variables</span>
  * <span style="color:#262626">System do reclaim : show system do reclaim message</span>
  * <span style="color:#262626">No change : pass the test</span>

<span style="color:#404040">Argument "\-cvus" : </span>  <span style="color:#FF0000">Check Variable Usage situation by Shutdown</span>  <span style="color:#404040">\.</span>

![](img/H2OUVE_User_Guide151.png)

![](img/H2OUVE_User_Guide152.png)

![](img/H2OUVE_User_Guide153.png)

### -cvrd
<span style="color:#404040">Argument "\-cvrd" : </span>  <span style="color:#FF0000">Check Variable Reclamation on Dxe</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvrd \[\-count\]"</span>

<span style="color:#262626">The argument \-count used to specified the number of times\.</span>

<span style="color:#262626">This function is not supported in secure flash mode\.</span>

<span style="color:#262626">Write a 'dirty\-byte' to the variable storage remaining area\.</span>

<span style="color:#262626">BIOS will do reclaim while detect there have any byte in remaining area is 'dirty\-byte' \(not 0xFF\) during POST time\.</span>

![](img/H2OUVE_User_Guide154.png)

![](img/H2OUVE_User_Guide155.png)

### -cvrs
<span style="color:#404040">Argument "\-cvrs" : </span>  <span style="color:#FF0000">Check Variable Reclamation on Smm</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvrs \[\-count\]"</span>

<span style="color:#262626">The argument \-count used to specified the number of times\.</span>

<span style="color:#262626">This function is not supported in secure flash mode\.</span>

<span style="color:#262626">Create variables until remaining size reaches the reclaim threshold and trigger reclamation event\.</span>

![](img/H2OUVE_User_Guide156.png)

![](img/H2OUVE_User_Guide157.png)

### -cvsf
<span style="color:#404040">Argument "\-cvsf" : </span>  <span style="color:#FF0000">Check Variable fill Setting \(fill 0xFF\)</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvsf \[\-count\] \[\-bc\]"</span>

<span style="color:#262626">The argument \-count used to specified the number of times\.</span>

<span style="color:#262626">The argument \-bc used to specified the Partial Erase Size Base on Block Size = 0x1000\. \(Number \* BlockSize\)</span>

<span style="color:#262626">Fill 0xFF to NV Variable Area and reboot\, the system should rebuild the NV Variable Area after reboot\.</span>

<span style="color:#262626">This function is not supported in secure flash mode\.</span>

![](img/H2OUVE_User_Guide158.png)

![](img/H2OUVE_User_Guide159.png)

### -cvs0
<span style="color:#404040">Argument "\-cvs0" : Check Variable fill Setting \(fill 0x00\)</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvs0 \[\-count\] \[\-bc\]"</span>

<span style="color:#262626">The argument \-count used to specified the number of times\.</span>

<span style="color:#262626">The argument \-bc used to specified the Partial Erase Size Base on Block Size = 0x1000\. \(Number \* BlockSize\)</span>

<span style="color:#262626">Fill 0x00 to NV Variable Area and reboot\, the system should rebuild the NV Variable Area after reboot\.</span>

<span style="color:#262626">This function is not supported in secure flash mode\.</span>

![](img/H2OUVE_User_Guide160.png)

![](img/H2OUVE_User_Guide161.png)

### -cgnv
<span style="color:#404040">Argument "\-cgnv" : </span>  <span style="color:#FF0000">Check GetNextVariablename on RT</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cgnv"</span>

<span style="color:#262626">Verify Runtime GetNextVariableName function\.</span>

<span style="color:#262626">Compare the variable between parsed from BIOS ROM and Runtime GetNextVariableName\.</span>

![](img/H2OUVE_User_Guide162.png)

![](img/H2OUVE_User_Guide163.png)

### -cssr
<span style="color:#404040">Argument "\-cssr" : </span>  <span style="color:#FF0000">Check Synchronization between SMM and RT SetVariable</span>  <span style="color:#404040">\.</span>

* <span style="color:#262626">Type command "H2OUVE \-cssr"</span>
* <span style="color:#262626">Verify synchronization between SMM and RT SetVariable\.</span>
* <span style="color:#262626">Behavior</span>
  * <span style="color:#262626">Write new variable in the sequence: SMM\, RT\, SMM\, RT\.</span>
  * <span style="color:#262626">Then read variable data in the sequence: SMM\, RT\, SMM\, RT and check if variable corrupted\.</span>

![](img/H2OUVE_User_Guide164.png)

![](img/H2OUVE_User_Guide165.png)

### -cvsd
<span style="color:#404040">Argument "\-cvsd" : </span>  <span style="color:#FF0000">Check Variable is existing while changing variable State to Deleteed\_transition in Smm variable services</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvsd"</span>

<span style="color:#262626">Create a variable with state Added and change the variable state from Added to Deleted\_Transition\, then read the variable to ensure the variable is valid\.</span>

![](img/H2OUVE_User_Guide166.png)

![](img/H2OUVE_User_Guide167.png)

### -sipi
<span style="color:#404040">Argument "\-sipi" : </span>  <span style="color:#FF0000">Send IPI</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-sipi"</span>

<span style="color:#262626">Send IPI interrupt message to CPU and all except self processors\.</span>

<span style="color:#262626">If processors cannot resume normally\, the system may crush\.</span>

![](img/H2OUVE_User_Guide168.png)

![](img/H2OUVE_User_Guide169.png)

### -cvax
<span style="color:#404040">Argument "\-cvax" : </span>  <span style="color:#FF0000">A group test</span>  <span style="color:#404040">\.</span>

<span style="color:#262626">Type command "H2OUVE \-cvax</span>  <span style="color:#262626">"</span>

<span style="color:#262626">This test is a group test to test -cvhc\, \-cnvs\, \-dvfi\, \-vorv\, \-cvur\, \-cvus\, \-cvsf\, \-cvs0 one by one</span>

<span style="color:#262626">Before run this test\, make sure system can be login automatically and run H2OUVE with administrator permission without input password</span>

![](img/H2OUVE_User_Guide170.png)

<div style="page-break-after: always;"></div>
