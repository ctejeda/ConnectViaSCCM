Remote machine access is a crucial aspect of IT administration and support. In this tech article, we will explore how to leverage the PowerShell module on Windows to connect to a Windows machine via SCCM (System Center Configuration Manager). By utilizing the provided script, we can easily connect to a user’s primary device, choose from a list of primary devices, call the SCCM executable from the command-line interface (CLI), send wake packets to wake up sleeping machines, and log events for future reference. We will also guide you on obtaining the script from a GitHub repository. Let’s explore the benefits and procedures.

Benefits of Using PowerShell and SCCM:

Connecting to a User’s Primary Device:
One significant benefit of the PowerShell script is the ability to connect to a user’s primary device. This ensures that you are connecting to the correct machine for support or administrative tasks, leading to more efficient troubleshooting and user assistance.
Choosing from a List of Primary Devices:
In scenarios where a user has multiple primary devices, the script allows you to select from a list of available devices. This flexibility empowers you to connect to the desired device and avoid any confusion or potential mistakes caused by connecting to the wrong machine.
Calling the SCCM Executable from CLI:
The script seamlessly integrates with SCCM by calling the SCCM executable from the command-line interface. This eliminates the need for manual navigation through the SCCM user interface and enables a quicker and more streamlined connection process.
Sending Wake Packets to Wake Sleeping Machines:
When a target machine is in sleep mode, establishing a remote connection can be challenging. The PowerShell script includes functionality to send wake packets, which wake up sleeping machines remotely. This capability ensures uninterrupted access, even when the target machine is in a low-power state.
Logging Events for Future Reference:
The script incorporates event logging, allowing you to keep a record of important events during the remote connection process. Logging events provides a valuable reference for troubleshooting, auditing actions performed on the machines, and analyzing usage patterns.
Step-by-Step Guide:

Obtaining the Script:
To obtain the PowerShell script, follow these steps:
Visit the GitHub repository: https://github.com/ctejeda/ConnectViaSCCM.git
Download the script from the repository.
Save the script file to a directory of your choice, such as C:\Scripts\ConnectViaSCCM.ps1.
Adjusting Execution Policy:
Before running the script, ensure that the PowerShell execution policy allows script execution. Follow these steps:
Open a PowerShell console with administrative privileges.
Set the execution policy by running the following command:
powershell Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Navigating to the Script Directory:
In the PowerShell console, navigate to the directory where the script is saved. For example:
   cd C:\Scripts
Example Usage: Connecting to a User’s Primary Device:
To connect to a user’s primary device, execute the following command:
   .\ConnectViaSCCM.ps1 -user "Username" -showPrimaryDeviceOnly
Replace “Username” with the appropriate username. This command retrieves the primary device for the specified user and displays a list of available primary devices to choose from. Select the desired device from the list.

Example Usage: Connecting to a Specific Computer:
To connect to a specific computer via SCCM, execute the following command:
   .\ConnectViaSCCM.ps1 -computer "ComputerName"
Replace “ComputerName” with the name of the target computer. This command initiates a connection to the specified computer using SCCM.

Example Usage: Sending Wake Packets to a Sleeping Machine:
To send wake packets and wake up a sleeping machine before establishing a remote connection, use the following command:
   .\ConnectViaSCCM.ps1 -computer "ComputerName" -SendWakePacket
Replace “ComputerName” with the name of the target computer. This command sends wake packets to wake up the sleeping machine and then connects to it using SCCM.

Enjoy Remote Machine Access:
After executing the script with the desired parameters, you will establish a remote connection to the specified computer via SCCM. This remote access enables you to perform various administrative tasks, troubleshooting, or user support.
