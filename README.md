# PowerShell and SCCM for Remote Machine Access

This repository provides a PowerShell script for efficient and streamlined remote access to Windows machines via SCCM (System Center Configuration Manager). The script allows for quick connection to a user's primary device, facilitates choosing from a list of primary devices, enables calling the SCCM executable from the command-line interface (CLI), supports sending wake packets to wake up sleeping machines, and logs events for future reference. 

## Benefits of Using PowerShell and SCCM:

* **Connecting to a User’s Primary Device**: The PowerShell script allows for easy connection to a user's primary device, enhancing troubleshooting and user assistance efficiency.

* **Choosing from a List of Primary Devices**: If a user has multiple primary devices, the script offers the flexibility to select the required device, preventing confusion and potential errors from connecting to the incorrect device.

* **Calling the SCCM Executable from CLI**: The script allows for SCCM executable calling from the CLI, eliminating manual navigation through the SCCM user interface and promoting a quicker and more streamlined connection process.

* **Sending Wake Packets to Wake Sleeping Machines**: The script supports the sending of wake packets to wake up sleeping machines remotely, ensuring uninterrupted access even when the target machine is in a low-power state.

* **Logging Events for Future Reference**: Event logging is incorporated into the script, providing valuable reference for troubleshooting, auditing machine actions, and analyzing usage patterns.

## How to Use:

### Step 1: Obtaining the Script

1. Visit the GitHub repository: https://github.com/ctejeda/ConnectViaSCCM.git
2. Download the script from the repository.
3. Save the script file to a directory of your choice, e.g., C:\Scripts\ConnectViaSCCM.ps1.

### Step 2: Adjusting Execution Policy

Before running the script, you need to ensure that the PowerShell execution policy permits script execution. Follow these steps:

1. Open a PowerShell console with administrative privileges.
2. Set the execution policy by running the following command: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

### Step 3: Navigating to the Script Directory

In the PowerShell console, navigate to the directory where the script is saved. For example: `cd C:\Scripts`

### Example Usage

* **Connecting to a User’s Primary Device**: To connect to a user’s primary device, execute the following command: `.\ConnectViaSCCM.ps1 -user "Username" -showPrimaryDeviceOnly`. Replace “Username” with the appropriate username. This command retrieves the primary device for the specified user and displays a list of available primary devices to choose from.

* **Connecting to a Specific Computer**: To connect to a specific computer via SCCM, execute the following command: `.\ConnectViaSCCM.ps1 -computer "ComputerName"`. Replace “ComputerName” with the name of the target computer.

* **Sending Wake Packets to a Sleeping Machine**: To send wake packets and wake up a sleeping machine before establishing a remote connection, use the following command: `.\ConnectViaSCCM.ps1 -computer "ComputerName" -SendWakePacket`. Replace “ComputerName” with the name of the target computer.

After executing the script with the desired parameters, a remote connection will be established with the specified computer via SCCM. Enjoy your efficient remote machine access!

Note: Always replace "Username" and "ComputerName" with the actual user's username and the name of the target computer respectively.
