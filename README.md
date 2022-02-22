<h3>In Just 5 Step to install Mac OS X in windows and linux </h3>(VMWARE Both (Workstaiton/Player))(**No Need to close The WSL or Hyper-V**)

1:- Download  Mac OS image (macOS Big Sur 11.0.1 (20B29)) and Vmware Player or Workstation :- 

**Tested**: MacOS Big Sur:	

		https://bit.ly/3h7OBfK
**Tested**: MacOS Mojave:

		https://bit.ly/3Hdl52H
**Not Tested**: MacOS Catalina:

		https://bit.ly/3v9QAbm


2: Install The Unlocker (**Warning:Make Sure to close all services of VMWARE using task manger and turn off antivirus** )

**Note: Unlocker 3 is designed for VMware Workstation 11-16 and Player 7-16.**
 
		git clone https://github.com/AnjaniGourisaria/VMWARE-unlocker 

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1:After Git clone and install Python 2.7 or later:<br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Run (Windows):<br>


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Inside The VMWARE-unlocker folder/dir (Run as Administration):  win-install.cmd  <br>

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Run (Linux):

                               				./lnx-install.sh
3: Change the double Quotation mark("") Please Insert This End of FIle

		smc.version = 0
		cpuid.0.eax = "0000:0000:0000:0000:0000:0000:0000:1011"
		cpuid.0.ebx = "0111:0101:0110:1110:0110:0101:0100:0111"
		cpuid.0.ecx = "0110:1100:0110:0101:0111:0100:0110:1110"
		cpuid.0.edx = "0100:1001:0110:0101:0110:1110:0110:1001"
		cpuid.1.eax = "0000:0000:0000:0001:0000:0110:0111:0001"
		cpuid.1.ebx = "0000:0010:0000:0001:0000:1000:0000:0000"
		cpuid.1.ecx = "1000:0010:1001:1000:0010:0010:0000:0011"
		cpuid.1.edx = "0000:1111:1010:1011:1111:1011:1111:1111"
		featureCompat.enable = "FALSE"
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
If you are facing the same error message after saving the changes, then change  **‘featureCompat.enable =’**  entry to  **“TRUE**.**”**  After that, remove the  **‘cpuid.ss’**  and  **‘wcpuid.ds’**  entries from the enabled features. Plus, change the value of  **‘cpuid.1.edx’**  line to  **‘**  **“0000:0111:1000:1011:1111:1011:1111:1111”**  .**’**



WHY?: VMWARE-unlocker  
The patch code carries out the following modifications dependent on the product being patched:

-   Fix vmware-vmx and derivatives to allow macOS to boot
-   Fix vmwarebase .dll or .so to allow Apple to be selected during VM creation
-   Download a copy of the latest VMware Tools for macOS


