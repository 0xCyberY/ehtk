# Clearing Logs

## Steps to clear logs using Clear_Event_Viewer_Logs.bat utility are as follows
1. Download the Clear_Event_Viewer_Logs.bat utility from https://www.tenforums.com.
2. Unblock the .bat file. 3. Right-click or press and hold on the .bat file and click/tap on Run as administrator. 4. If prompted by UAC, click/tap on Yes.
5. A command prompt will now open to clear the event logs. The command prompt will automatically close when finished.

## Steps to clear logs using Meterpreter shell are as follows.
If the system is exploited with Metasploit, the attacker uses a Meterpreter shell to wipe out all the logs from a Windows system: 
1. Launch the meterpretershell prompt from the Metasploit Framework.
2. Type `clearev` command in the Meterpreter shell prompt and press Enter. The logs of the target system will start being wiped out.

## Steps to clear PowerShell logs using Clear-EventLog command are as follows. 
Using the `Clear-EventLog` command, the attacker can clear all the PowerShell event logs from local or remote computers: 
1. Launch Windows PowerShell with administrator privileges. 
2. Use the following command to clear the entries from the PowerShell event log on the local or remote system: 
>`Clear-EventLog "Windows PowerShell"`
3. Use the following command to clear specific multiple log types from local or remote systems: 
> `Clear-EventLog-LogName ODiag, OSession -ComputerName localhost, Server02`
(This command clears all the log entries in Microsoft Office Diagnostics (ODiag) and Microsoft Office Sessions (OSession) on the local computer and Server02 remote computer.)
4. Use the following command to clear all the logs on the specified systems, and then display the event log list: 
>`Clear-EventLog -LogName application, system -confirm`
Note: The parameters used in the `Clear-EventLog` command are as follows: 
o `-ComputerName`: Specifies a remote computer; the default is the local computer 
o `-Confirm`: Prompts you for confirmation before running cmdlet 
o `-LogName`: Specifies the event logs o -WhatIf: Shows what will happen if the cmdlet runs

## Steps to clear event logs using wevtutil utility are as follows. 
1. Launch command prompt with administrator privileges. 
2. Use the following command to display a list of event logs: >`wevtutil el`
3. Use the following command to clear the event logs: >`wevtutil cl` <log_name> 
	`log_name`: name of the log to clear, ex: system, application, security. As shown in the screenshot, the attacker can view the list of event logs using the wevtutil utility and clear the system, application, and security event logs.

# Manually Clearing Event Logs 
## For Windows 
- Navigate to Start -> Control Panel -> System and Security -> Administrative Tools -> double-click Event Viewer
- Delete the all the log entries logged while compromising the system

## For Linux 
- Navigate to the `/var/log` directory on the Linux system 
- Open the plaintext file containing log messages with text editor `/var/log/messages` 
- Delete all the log entries logged while compromising the system