SECURE PERSO INSTALLATION AND USAGE GUIDE
Contents
1.	Prerequisites

1.1	Operating System Requirements

1.2	.NET Framework Requirement

1.3	SafeNet HSM Software Interface Requirement
2.	Software Installation
2.1	Installing the .NET Framework 3.5
2.2	Installing the SafeNet HSM Software Interface with PTK-C
3.	Secure Perso Profile Creation
4.	Secure Perso Data Processing Steps
5.	Maintenance
6.	Data flow diagram
7.	System and Network architecture
 



SOFTWARE INSTALLATION
 
1.0	Prerequisites
Before installing Secure Perso, ensure your system meets the following requirements:
•	Operating System: Windows 11(Current OS version)
•	.NET Framework: Version 3.5 enabled within Windows Features
•	SafeNet HSM Software Interface: Installed and configured for use with PTK-C
•	Workstation : For data management
1.1	Operating System Requirements
The Windows operating system provides the fundamental platform for your computer, managing hardware and software resources to ensure efficient operation. Secure Perso is designed to function optimally on Windows 11 or a later version.
1.2	.NET Framework Requirement
The .NET Framework 3.5, developed by Microsoft, offers a comprehensive set of pre-built code libraries and a runtime environment necessary for running various applications.
Secure Perso relies on these components for its functionality.
1.3	SafeNet HSM Software Interface Requirement 
The SafeNet Hardware Security Module (HSM) Software Interface with PTK-C provides a secure method for managing cryptographic keys and performing cryptographic operations. This interface is crucial for protecting sensitive data and meeting security compliance standards within Secure Perso.
 
2.0	Installing the .NET Framework 3.5
The .Net Framework 3.5 can be enabled through the Windows graphical user interface (GUI). Follow these steps:
2.0.1	Open Control Panel: Search for "Control Panel" in the Start menu and open it.
2.0.2	Access Programs and Features: Within the Control Panel, click on "Programs" or "Programs and Features."
2.0.3	Turn Windows Features On or Off: On the left-hand side of the "Programs and Features" window, select "Turn Windows features on or off."
2.0.4	Enable .NET Framework 3.5: In the "Windows Features" dialog box, find the entry ".NET Framework 3.5 (includes .NET 2.0 and 3.0)" and check the box next to it.
2.0.5	Initiate Installation: Click "OK" to begin the installation. Windows may need to download additional files from Windows Update.
2.0.6	Complete Installation: Follow any on-screen prompts to finish the installation. Restart your computer if requested.
 
Integrating the SafeNet HSM Software Interface with PTK-C is essential for secure operations. Follow these steps:
2.0.7	Obtain Installation Materials:
2.0.7.1	Download the SafeNet HSM Software Interface with PTK-C installation package from the official SafeNet website or your designated software provider.
2.0.7.2	Ensure you have access to all necessary documentation, including installation guides and release notes.
2.0.8	System Requirements Check:
2.0.8.1	Carefully review the system requirements outlined in the SafeNet documentation forthe HSMSoftware Interface with PTK-C. Verifythat your system meets all specified hardware and software prerequisites.
2.0.9	Prepare Environment:
2.0.9.1	Before starting the installation, ensure your system is correctly configured according to any network or security requirements detailed in the SafeNet documentation.
2.0.9.2	Confirm that you have administrator privileges on the target system to install software.
2.0.10	Run Installer:
2.0.10.1	Locatethe SafeNet HSMSoftware Interface installer file and double-click it to launch the installation process.
2.0.10.2	Follow the on-screen prompts provided by the installer.
2.0.11	Accept License Agreement:
2.0.11.1	Carefullyreadandacceptthelicenseagreement presented during the installation.
2.0.12	Choose Installation Options:
2.0.12.1	Select the specific components or features you wish to install. This might include the core software interface, drivers, utility programs, and
documentation.
2.0.13	Specify Installation Directory:
 
2.0.13.1	Choose the location where you want to install the SafeNet HSM Software Interface. Youcaneither use the default installation path or specify a custom directory.
2.0.14	Configure HSM Connectivity:
2.0.14.1	Duringtheinstallation, youmay be prompted to configure the connection to your SafeNet Hardware Security Module (HSM). Provide the required information, such as the HSM's IP address, port number, and any necessary authentication credentials.
2.0.15	Complete Installation:
2.0.15.1	Follow the on-screen instructions to finalize the installation process. Allow the installer to complete the installation of all selected components.
2.0.16	Verify Installation:
2.0.16.1	Once the installation is finished, verify that the SafeNet HSM Software Interface has been installed successfully.
2.0.16.2	Test the connection to your HSM to ensure that your software applications can communicate correctly using the PTK-C interface.
2.0.17	Post-Installation Tasks:
2.0.17.1	After installation, you mayneed to perform additional configuration or setup tasks depending on your specific environment and requirements.
2.0.17.2	Refer to the SafeNet installation guide and documentation for any necessary post-installation configuration steps or best practices.








2.0.18	Documentation and Support:
2.0.18.1	Take time to familiarize yourself with the documentation provided with the SafeNet HSM Software Interface. It contains valuable information on configuration, troubleshooting, and best practices.
By following these steps, you should be able to successfully install the SafeNet HSM Software Interface with PTK-C and integrate it with your software environment. If you encounter any issues, consult the official SafeNet documentation or contact SafeNet
 
technical support for assistance.
3.0 Secure Perso Profile Creation 
This section describes how to create profiles within Secure Perso for different customers and card products. This function is typically performed by the EMV Implementation team.
Profiles are created using a configuration adaptor file. A copy of an existing, related profile is made and then renamed according to the Customer, card type, and chip type






















(Figure 1 - Note: Ensure Figure 1 is appropriately referenced and included in the manual).
 

























(Figure 2 showing card profiles for In house personalization)
 





















(Figure 3 showing the content of the card profiles in fig 1 - Ensure Figure 3 is appropriately referenced and included)
Step 1: Define Product Name and Select Profiles
•	In the profile creation interface, specify the Product Name.
•	Selecttheappropriate Customer, Card Profile, and Key Profile fromtheprovided dropdown lists.
Step 2: Define Customer Bank BINs
•	Define the Bank Identification Numbers (BINs) associated with the customer and the profile being created.
•	The BIN(the first 6 digits of the Primary Account Number - PAN) is declared within the
‘Declaration: Validate_PAN’ section


(Figure 2 - Note: Ensure Figure 2 is correctly referenced here).
•	If multiple BINs are associated with the same product andcustomer, list each BIN
separated by a ‘+’ sign.
 
Step 3: Define the Key Profile
•	Identify the required HSM keys for the in-house personalization process.
•	Copy the exact names of these keys from the HSM view.
•	Insert the copied key references into the Header section of the adapter file






























1showing the creation of profiles by injecting specific details



4.0 Secure Perso Data Processing Steps
This section outlines the steps involved in processing data for card personalization within Secure Perso. This process is typically carried out by Card Operations personnel.
To process data:
 
1.	Browse for File: Click the Browse button to locate and select the data file you wish to process.


 





2 Browsing a file



2.	Automatic Loading: Once selected, the file will automatically load into the system, and the total number of records within the file will be displayed.

  


3Figure demonstrating the selection of created profiles from a drop-down list in the processor adapter



  



4Figure showing a successfully loaded file for processing



The Profile tab displays a list of existing scripts used for file processing.
1.	Select Profile: Choose the appropriate profile from the list to process thedata.
2.	Initiate Processing: Once a profile is selected, click the Process button to begin the data processing.
3.	Cancel Processing (Optional): If you do not want to proceed, click the Cancel
button.
4.	Locate Output File: After processing is complete, checkthe designated Output folder
for the generated machine file.

4.0	Logging of processed file

Upon successful file processed, the log of the processed file can be located in the log.txt folder on the adaptor. It contains the following:
•	The file processed

•	The number of records processed

•	Time stamp and date it was processed
 
5.0	Maintenance General Overview
As the solution is developed in modules for different functionalities, any new feature addition or bug fixing only that module needs to be amended and released with a new version. It is not necessary to update the whole solution.
Every new release should go through an approval process. It is important to verify the test scenarios and its outcome before any new release approval.
Reporting & Management

Any issues or feature additions can be reported by the end users, and it should go through the below process.

 
6.0	DATA FLOW DIAGRAM DIAGRAMS
Data Flow Diagram

 
7.0	Systems and Network Architecture



