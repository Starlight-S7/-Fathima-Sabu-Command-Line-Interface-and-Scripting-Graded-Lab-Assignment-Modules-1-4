<h2>Question 4</h2>
You must perform all operations without making any configuration changes to the system.
These tasks should be executed within your own user account. Since uptime, processes, memory usage, disk usage, and background jobs vary across systems and users, each student’s output will be unique.

1. System Uptime Verification: 
Display the time elapsed since the system was last booted.

**Answer 1:** To display the time elapsed since the last boot, I used the **top** command, which displays *real-time* information about system activity.

The **uptime** command in Linux systems shows how long the system has been running, the current time, the number of logged-in users, and the system's load average (average processes waiting for CPU) over the last 1, 5, and 15 minutes.
<img width="1920" height="805" alt="Screenshot (667)" src="https://github.com/user-attachments/assets/74b2b288-1e61-427a-a414-9f969f41ed68" />
<img width="1088" height="403" alt="Screenshot (668)" src="https://github.com/user-attachments/assets/e411b4d8-60bb-409b-abde-cee3388deb78" />

2. User Process Listing: 
List all processes currently running under your user account.

**Answer 2:** The **ps** command is used to display only a basic snapshot of processes running in the current shell session

To list all the comprehensive, user-oriented list of all running processes on the system, including background daemons, I used **ps aux**, which provides details like the Process ID (PID), CPU usage, and the user associated with the process.
<img width="1040" height="578" alt="Screenshot (669)" src="https://github.com/user-attachments/assets/2d64dc1f-11a1-4103-a191-93ebc784a83f" />
<img width="1110" height="806" alt="Screenshot (670)" src="https://github.com/user-attachments/assets/6d7ec5d7-b952-49ae-8807-056c5a508567" />

3. CPU Usage Analysis: 
Identify the process that is consuming the highest CPU usage among your running processes.

**Answer 3:** To identify the process consuming the highest CPU, I used the top command. This tool provides a real-time, dynamic view of the system, automatically sorting processes by their resource consumption, including CPU and memory usage.

The output is a continuously updating list. The process at the very top of the list under the COMMAND column is consuming the most CPU resources at that moment. In this screenshot, it can be seen that the python command was consuming the highest CPU usage.
<img width="1141" height="798" alt="Screenshot (671)" src="https://github.com/user-attachments/assets/ba41e34e-6ef0-4bc5-b5bd-f0e92a10ff30" />

4. Background Process Execution: 
Start a command in the background and verify that it is running.

**Answer 4:** In Linux, background processing allows a task to run independently of the active terminal. To execute a command in the background, append an ampersand (&) to the end of the command (e.g., sleep 100 &). I verified it is running by using the ps command.

I also used the ps aux command with the help of grep to pinpoint the exam process running, as ps aux would usually give a long list of processes. So, using grep to specify which command we wanna check is a time efficient way.
<img width="1174" height="363" alt="Screenshot (673)" src="https://github.com/user-attachments/assets/6a930edd-a3ff-4ccb-ba32-ce81a2dd84dc" />

5. Process Priority Management: 
Change the priority (niceness) of one of your running processes and display the updated priority.

**Answer 5:** To change a running process's priority (niceness), I used the renice command with the new value and Process ID (PID), and then verified it with ps -l.

I first used the command ps to check and select which process's priority I want to change. I chose the python/home command, of which the PID is 349. I changed its priority to 5 from 0 (lowered its priority). If I want to make the priority higher, it would require the sudo command, which is not working in the Coursera labs. Using the **ps -l -p 349** command, I was able to verify that the priority has been successfully changed.
<img width="1045" height="586" alt="Screenshot (675)" src="https://github.com/user-attachments/assets/004e1147-5ce4-440c-8a48-40c5947e4e29" />

6. Memory Usage Monitoring: 
Display memory usage information in a human-readable format.

**Answer 6:** I used the free command with the -h option to turn it into a human-readable format.
- Total: It represents the total RAM of the system.

- Used: It represents the current memory that is currently in use.

- Free: It represents free memory.

- Shared: It represents shared memory among processes.

- Available: It represents the estimated amount of memory available.
<img width="1045" height="584" alt="Screenshot (677)" src="https://github.com/user-attachments/assets/9ccd2392-bceb-4463-9d65-9ef8f14c0442" />

7. Disk Space Inspection: 
Display the disk space usage of the filesystem where your home directory resides.

**Answer 7:** To check the filesystem where the home directory resides, I used the df -h command. The df (disk free) command displays used and available space on all mounted filesystems, and the -h option ensures the output is in a human-readable format.
<img width="1043" height="648" alt="Screenshot (678)" src="https://github.com/user-attachments/assets/f5cfdf63-fa1b-4ec8-9c73-f5d8bd79ce85" />

8. Shell Identification: 
Display the name of the shell currently in use.

**Answer 8:** The command **echo $0** displays the name of the process currently running, which is typically the shell's name. The shell that I'm currently using is bash.
<img width="1042" height="656" alt="Screenshot (681)" src="https://github.com/user-attachments/assets/d1badefd-10d5-432d-967f-446bb23a6558" />

9. Output Redirection: 
Redirect the output of a system information command of your choice into a file named system_report.txt.

**Answer 9:** I added all the system information from the commands hostname, ps, uptime, and df -h into the system_report.txt file and used the cat command to check if they all have been successfully included in the file. The redirection of the first output only used one output redirection operator (>) as it was adding to an empty file, but if I had used only one (>) for the next commands, then it would have over-written the file input and would've given only the latest addition. Therefore, I used the double output redirection operator (>>) to add to the next lines and not over-write the existing info.
<img width="1828" height="573" alt="Screenshot (683)" src="https://github.com/user-attachments/assets/1fe2e92b-8682-4a21-ba41-1e742ac53333" />

10. Disk Usage Visualization: 
Demonstrate the usage of the ncdu tool using appropriate options and briefly explain what it shows.

**Answer 10:** ncdu (NCurses Disk Usage) is an interactive, visual version of du. It provides an easy-to-navigate interface to see which folders are taking up the most space.

ncdu was not installed or available in the Coursera labs system, and due to not having permission to use sudo in the Coursera labs, I am using my Kali OS to demonstrate the command.

I had to first install the ncdu tool.
<img width="1920" height="1080" alt="Screenshot (684)" src="https://github.com/user-attachments/assets/6db050f0-2946-469f-85be-f3be5de53903" />
Once the tool was installed and running, I was able to spot that BurpSuite was taking up the most space.
<img width="1920" height="1080" alt="Screenshot (685)" src="https://github.com/user-attachments/assets/ba431559-1eaa-43ce-ab44-a405e951b4cf" />
After navigating through the list, I pressed the right arrow key at the Downloads folder (or one could use the enter key instead) and was able to get further details on the files present in the folder.
<img width="1920" height="1080" alt="Screenshot (686)" src="https://github.com/user-attachments/assets/07430c6d-2563-45b8-a4e0-339dc0120e14" />
