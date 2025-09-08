# Features

* <span style="color:#262626">To provide 4 kinds of UEFI Variable Editors</span>
  * <span style="color:#262626"> _SCU\(Setup\) Editor _ </span>  <span style="color:#262626">: Edit "runtime/current setup setting" of platform</span>
  * <span style="color:#262626"> _Image SCU Editor _ </span>  <span style="color:#262626">: Edit "default setup setting" of BIOS image</span>
  * <span style="color:#262626"> _Variable Editor _ </span>  <span style="color:#262626">: Edit "runtime variable data" or "variable data in BIOS image"</span>
  * <span style="color:#262626"> _Variable Stress Test_ </span>  <span style="color:#262626">: Support stress testing UEFI variables at runtime or in the BIOS image\.</span>

## Supported OS environment
* <span style="color:#404040">UEFI SHELL</span>
* <span style="color:#404040">WINDOWS</span>
* <span style="color:#404040">LINUX</span>

## Limitation
* The  __SCU editor and Image SCU editor __ depend on  __InsydeH2oUvePkg\.__  Please make sure that your BIOS was built with that\.
* __Saving and loading custom deault __ depends on the PCD  _gInsydeTokenSpaceGuid\.PcdH2OCustomDefaultSupported_  being  __True__\.
  * To support full copy and restore for custom default\, the minimun version of  __BIOS version is 5\.31\.19__  and  __H2OUVE version is 200\.02\.00\.04__\.
* If __Boot Guard__ is enabled in BIOS, BIOS image modified by H2OUVE will __not__ able to __boot__\.
* If __PcdH2OIhisiVatsWriteLockEnabled__ is enabled in BIOS, H2OUVE will __not__ able to __modify__ runtime setup variable\.
* If __SecureBoot__ is __on__ when __PcdH2OIhisiVatsWriteLockEnabled__ is disabled, H2OUVE will __not__ able to __modify__ runtime setup variable\.

<div style="page-break-after: always;"></div>

## Command Status

<span style="color:#006600"> __O__ </span> <span style="color:#008000"> __- Support__ </span>  <span style="color:#FF0000"> __X  - Not Support__ </span> <span style="color:#FF0000"> __! \- Depend on BIOS__ </span>

| BIOS Kernel |  | 3.5 | 3.5 | 3.7 | 3.7 | 5.0 | 5.x |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
|  |  | CRB | OEM | CRB | OEM | CRB | CRB |
| Common Arguments  |  -r  | x | x | O | O | O | O |
|  |  -a | O | O | O | O | O | O |
|  |  -l | x | x | O | O | O | O |
|  | -c | x | x | O | O | O | ! |
|  | -sc | x | x | O | O | O | ! |
| Setup Editor<br />Arguments |  -gs  | x | x | O | O | O | O |
|  |  -ss  | x | x | O | O | O | O |
|  |  -ms  | x | x | O | O | O | O |
| Image Setup Editor<br />Arguments |  -gd  | x | x | O | O | O | O |
|  |  -sd  | x | x | O | O | O | O |
|  | -gstr | x | x | O | O | O | O |
|  | -sstr | x | x | O | O | O | O |
| Image Setup Editor<br />Arguments |  -dpw | x | x | O | O | O | O |
|  | -comp | x | x | x | x | O | O |
| Setup Editor<br />Name-Value Paired Arguments | -gst | X | X | O | O | O | O |
|  | -sst | X | X | O | O | O | O |
|  | -cdi | X | X | O | O | O | O |
| Variable Editor<br />Arguments |  -gv  | O | O | O | O | O | O |
|  |  -sv | O | O | O | O | O | O |
|  | -wt | - | - | - | - | O | O |
|  | -rd | - | - | - | - | O | O |
|  |  -re  | O | O | O | O | O | O |
|  | -cvl | X | X | O | O | O | O |
| Variable Stress Test <br />Arguments | -dbos | O | O | O | O | O | O |
|  | -cnvs | O | O | O | O | O | O |
|  | -cvhc | O | O | O | O | O | O |
|  | -vorv | O | O | O | O | O | O |
|  | -cvur | O | O | O | O | O | O |
|  | -cvus | O | O | O | O | O | O |
|  | -cvrd | O | O | O | O | O | O |
|  | -cvrs | O | O | O | O | O | O |
|  | -cvsf | O | O | O | O | O | O |
|  | -cvs0 | O | O | O | O | O | O |
|  | -cgnv | O | O | O | O | O | O |
|  | -cssr | O | O | O | O | O | O |
|  | -cvsd | O | O | O | O | O | O |
|  | -sipi | O | O | O | O | O | O |

<div style="page-break-after: always;"></div>
