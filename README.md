<h3>In Just 5 Step to install Mac OS X in windows and linux </h3>(**VMWARE**/**Virtual Box** Both (Workstaiton/Player))(**No Need to close The WSL or Hyper-V**)<br>
Raise a issue if found with log file and *.vmw 

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


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Inside The VMWARE-unlocker folder/dir (Run as Administration):  **win-install.cmd**  <br>

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Run (Linux):

                   				./lnx-install.sh
 - Step 1:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/image.png?raw=true)<br>
 - Step 2:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20041554.png?raw=true)<br>
 - Step 3:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20041657.png?raw=true)<br>
 - Step 4:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20041739.png?raw=true)<br>
 - Step 5:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20041902.png?raw=true)<br>
 - Step 6:<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20042017.png?raw=true)<br>
 - Step 7:<br>
Change the Cpu cores  as per your requiements<br>
 - Step 8:**SEE THE IMAGE CAREFULLY Under the directory you will found the *.vmx**<br>
![image description](https://github.com/AnjaniGourisaria/MacOS-in-windows-vm/blob/main/MacOS%20Installation/Screenshot%202022-02-23%20042254.png?raw=true)<br>
3: (**Optional** Run the Mac if not working follows steps below)Change the double Quotation mark("") **FIle is given in step 8 red line Please Insert This End of FIle(Inside The *.vmx)**

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

3:- Run The Machine <br>
4:- After Successful Installtion of Machine install the vm-tool for the MacOS Machine(Optional) <br>



WHY?: VMWARE-unlocker  
The patch code carries out the following modifications dependent on the product being patched:

-   Fix vmware-vmx and derivatives to allow macOS to boot
-   Fix vmwarebase .dll or .so to allow Apple to be selected during VM creation
-   Download a copy of the latest VMware Tools for macOS

REF: 

    https://computerverge.com/the-cpu-has-been-disabled-by-the-guest-operating-system-explained-and-fixed/
	
Raise a issue if found with log file and *.vmw 

