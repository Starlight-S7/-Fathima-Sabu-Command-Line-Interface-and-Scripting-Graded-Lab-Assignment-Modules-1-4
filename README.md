# -Fathima-Sabu-Command-Line-Interface-and-Scripting-Graded-Lab-Assignment-Modules-1-4
This repository contains the completed assignment of the Command Line Interface and Scripting Graded Lab Assignment done by Fathima Sabu.

**Coursera Labs** was used to complete this assignment.

<h2>Question 1</h2>
You have just joined IxD Systems as a junior systems engineer. On your first day, the Linux administrator asks you to perform a basic environment verification on the lab machine using your own login account.

1. User Identity Verification: 
Display your currently logged-in username and all groups your user account belongs to.
Your name or login ID must appear in the output.

**Answer 1:** I used the command whoami to display my current logged-in username. To see all groups that my user account belongs to, along with my unique user ID (UID), I used the id command.

Command: **whoami** and **id**
<img width="1790" height="895" alt="Screenshot (625)" src="https://github.com/user-attachments/assets/db7cd89c-e845-4157-b50b-cfefdf140696" />
I used the **clear** command after each question's commands to keep it looking tidy and easy to spot.

2. Workspace Validation: 
Display the current working directory and list all files and directories in that location using long format listing.

**Answer 2:** To display my current working directory, I used the **pwd** (print working directory) command.
And to list all files and directories in that location in a detailed format, I used **ls -l**, which provides the long format listing including permissions, owner, and size.

Command: **pwd** and **ls -l**
<img width="1122" height="716" alt="Screenshot (626)" src="https://github.com/user-attachments/assets/537de018-6f1f-4936-8071-f31a0713a7db" />
<img width="1079" height="683" alt="Screenshot (627)" src="https://github.com/user-attachments/assets/6e50f3bc-b071-4d4a-88ba-d48fd42a6408" />

3. Environment Confirmation File: 
Create a file named user_info.txt and write the line:
"Linux user environment verified"

**Answer 3:** To create the file and write the specific string to it, I used the echo command combined with output redirection (>). The > symbol redirects the text into the specified file, creating it if it does not exist. This was the easier way. The longer way would've been to first use the **touch** command to create the file and then use the **echo** command to write the line into the file.
Then I used the **cat** command to check if it worked. The proper command used was **cat user_info.txt**. This showed that the line was written successfully, as shown in the screenshot.

Command: **echo "Linux user environment verified" > user_info.txt**
<img width="1088" height="686" alt="Screenshot (629)" src="https://github.com/user-attachments/assets/236f1633-e79b-4927-804a-72974d446e22" />

4. File Integrity Check: 
Display the number of characters present in user_info.txt.

**Answer 4:** I used the Linux command **wc -m user_info.txt** to display the number of characters present in the user_info.txt file.
It was observed that there were 32 characters in the user_info.txt file.

Command: **wc -m user_info.txt**
<img width="1065" height="677" alt="Screenshot (640)" src="https://github.com/user-attachments/assets/9d2b1500-8d26-42b5-a3b9-1079ea628c3c" />

5. Learning the Tools: 
Access the manual page of the mkdir command. Identify one useful option and briefly explain what it does.

**Answer 5:** To access the manual page for the mkdir command, I used **man mkdir**.
I used my Kali Linux OS to use this command as the terminal in coursera labs kept showing the message "No manual entry for mkdir" as shown in the first screenshot. You can see the result of the command I ran in my Kali in the next screenshot
<img width="1083" height="675" alt="Screenshot (630)" src="https://github.com/user-attachments/assets/7223b908-941b-4e8c-bb70-8cb81bec0919" />
<img width="1920" height="936" alt="Screenshot_2025-12-25_11_28_22" src="https://github.com/user-attachments/assets/482bc896-9922-45a2-b04a-96c2dc5dc5f7" />
Useful Option: The -p option is highly useful as it allows us to create parent directories automatically if they do not already exist.
I used the command **mkdir -p /home/coder/parent/child** to create the directory **child** along with its parent directory **parent**.
Using the command **ls**, I saw that the **parent** directory was created. I used **cd parent** and then used **ls** again, to check if the **child** directory has been created. The commands were executed successfully and both the directories were present.

Command: **man mkdir** & **mkdir -p /home/coder/parent/child**
<img width="1051" height="678" alt="Screenshot (641)" src="https://github.com/user-attachments/assets/57a8c5cf-99dc-4321-8dc4-45bb29a365e4" />

6. Home Directory Inspection: 
List the contents of your home directory sorted alphabetically.

**Answer 6:** The home directory is represented by the tilde (~) symbol. To list its contents, I used the **ls ~** command. By default, ls lists entries alphabetically.

Command: **ls ~**
<img width="1064" height="683" alt="Screenshot (642)" src="https://github.com/user-attachments/assets/b5366364-fcc9-48f2-8bc3-d36b24b3c95b" />

7. Log Investigation: 
Search for the word "admin" inside a file named log.txt and display only the matching lines.

**Answer 7:** To search for the word "admin" and display only the matching lines, I used the grep command, which is designed for pattern matching within files. I first created the log.txt file using the **touch** command and edited it using vim to contain some lines, since the file was not pre-existing in the system provided.

Command: **grep -n "admin" log.txt**
<img width="1065" height="667" alt="Screenshot (634)" src="https://github.com/user-attachments/assets/17886fe9-aeda-4a4e-9c3c-401ed4eee6de" />
<img width="1046" height="670" alt="Screenshot (635)" src="https://github.com/user-attachments/assets/251c1d9d-34d6-42eb-af7e-950dbd65fff2" />

8. System Information Check: 
Display the Linux kernel version currently running.

**Answer 8:** To display the current running kernel version, the command I used is **uname -r**.

Command: **uname -r**
<img width="1051" height="667" alt="Screenshot (636)" src="https://github.com/user-attachments/assets/512cbdd8-bbca-46ab-9f50-d6a919e5f097" />

9. Network Connectivity Test: 
Verify network connectivity by sending ICMP packets to www.google.com.

**Answer 9:** I used the ping command to verify connectivity. It sends ICMP Echo Request packets to the destination and waits for a reply to measure performance.

Command: **ping www.google.com**
<img width="1051" height="685" alt="Screenshot (637)" src="https://github.com/user-attachments/assets/c8d1e282-faeb-44d1-9caf-7823fd13b395" />

10. System Health Awareness: 
Display the command used to check system uptime and briefly explain its output (uptime duration, number of users, load average).

**Answer 10:** I used the command **uptime** to get the uptime duration, number of users, and load average.

- Uptime duration: How long the system has been running since the last boot.

- Number of users: How many users are currently logged in (similar to information provided by who -q).

- Load average: The average system load over the last 1, 5, and 15 minutes.
<img width="1050" height="668" alt="Screenshot (639)" src="https://github.com/user-attachments/assets/a8956924-6f8f-4b2e-96fa-084da926adb1" />
The **top** command can be used for monitoring real-time system activity, including CPU and memory usage.
<img width="1058" height="667" alt="Screenshot (638)" src="https://github.com/user-attachments/assets/32a34dfa-6097-4ba5-8036-2bd678bd9202" />

<h2>Question 2</h2>
You are working as a junior system administrator responsible for organizing project-related files in your home directory.
Your supervisor wants you to demonstrate your understanding of Linux file and directory management commands.

1. Project Workspace Setup: 
Create a directory named documents inside your home directory. This directory will store your project-related files.

**Answer 1:** To create the documents directory in my home directory, I used the mkdir command. The tilde (~) symbol is a shortcut for the home directory. I have used the **ls** command to show that the directory has been created.

Command: mkdir ~/documents
<img width="1068" height="672" alt="Screenshot (643)" src="https://github.com/user-attachments/assets/1f74a083-297f-4e35-9222-fe434f893675" />

2. File Creation: 
Navigate into the documents directory and create a file named plan.txt.

**Answer 2:** I navigated into the new directory using **cd** (change directory) and then created the plan.txt file using the **touch** command.

Command: **cd ~/documents** & **touch plan.txt**
<img width="1077" height="678" alt="Screenshot (644)" src="https://github.com/user-attachments/assets/f9c852c0-0c30-4d8f-a418-bb4f2dcb065f" />

3. Content Addition: 
Write some sample text of your choice into the plan.txt file. The content can be a short project note or reminder.

**Answer 3:** To add text to the file, I used the echo command with the > redirection symbol, which sends the text into the file.

Command: **echo "Reminder to complete the YouTube script on the story behind the first computer worm" > plan.txt**
<img width="1067" height="672" alt="Screenshot (645)" src="https://github.com/user-attachments/assets/a7cb5fbb-96f7-4fb1-b3d5-4ca30bf76ed0" />

4. File Metadata Verification: 
Display the permissions and ownership details of the plan.txt file. Ensure your username appears in the output.

**Answer 4:** To view the permissions, owner, and group details, I used ls -l (long format listing). The username in my system, which is "coder", appears on the output.

Command: **ls -l plan.txt**
<img width="1057" height="670" alt="Screenshot (646)" src="https://github.com/user-attachments/assets/b0d2346c-a953-45ef-a094-2386a6ea78e0" />

5. File Duplication: 
Create a copy of plan.txt and name it plan_copy.txt.

**Answer 5:** I used the cp (copy) command to create a duplicate of the **plan.txt** file.

Command: **cp plan.txt plan_copy.txt**
<img width="1072" height="675" alt="Screenshot (648)" src="https://github.com/user-attachments/assets/4b8f97ad-12cc-43d7-830a-22411fd210b2" />

6. Directory Renaming: 
Rename the documents directory to project_documents to reflect the project scope more clearly.

**Answer 6:** The mv (move) command is used for both moving and renaming files or directories. Therefore, I used the mv command with the directory names. I was in the directory that was being renamed, so I went back using **cd ..** and then used the **ls** command to check if the name had been changed. The name was changed successfully. Then I used cd with the directory name to go back inside the directory to do the further questions.

Command: **mv ~/documents ~/project_documents**
<img width="1055" height="672" alt="Screenshot (650)" src="https://github.com/user-attachments/assets/7128cb3f-05d1-477a-8897-307309f0a675" />

7. Archival Structure: 
Inside the project_documents directory, create a subdirectory named archive.

**Answer 7:** After navigating into the renamed directory, I used **mkdir** again to create the archive subdirectory. Then used **ls** to check if it had been created. The sub-directory had been successfully created.

Command: **mkdir archive**
<img width="1059" height="667" alt="Screenshot (651)" src="https://github.com/user-attachments/assets/2ab01cf0-39d2-4cdc-98c8-49d0cb1dd163" />

8. File Organization: 
Move plan_copy.txt into the archive subdirectory.

**Answer 8:** I moved the plan_copy.txt file into the archive directory using the mv command. I then used cd to change the directory to archive, then used ls to check if the file has been successfully tranferred. I also went back and checked if the file had been moved from the first directory to the subdirectory. The process was successful.

Command: **mv plan_copy.txt archive**
<img width="1056" height="667" alt="Screenshot (652)" src="https://github.com/user-attachments/assets/686f21ed-7cc0-43c2-8f59-03b75f464bad" />

9. Recursive Listing: 
List all files and subdirectories inside project_documents recursively so that the complete directory structure is visible.

**Answer 9:** To view the complete directory structure, including the contents of the archive subdirectory, I used ls -R (recursive listing). This command was used when I was already in the project_documents directory. If I were in the home directory, I would also have to include the path to that directory.

Command: **ls -R** & **ls -R ~/project_documents**
<img width="1052" height="667" alt="Screenshot (653)" src="https://github.com/user-attachments/assets/dd1313e1-1000-418a-adfb-863ce9bcff1a" />

10. Path Verification: 
Display the absolute path of the plan_copy.txt file after it has been moved to the archive directory.

**Answer 10:** I navigated into the archive directory and used **pwd** (print working directory) to display the absolute path, which shows the full location starting from the root ("/").

Command: **cd archive** then **pwd**
<img width="1052" height="667" alt="Screenshot (654)" src="https://github.com/user-attachments/assets/244612b9-245f-4a9f-9a8a-328a4ae97ea0" />

<h2>Question 3</h2>
You have been asked to understand how Linux manages files using links and disk usage information. As part of your role, you will perform the following operations within your own user space.

1. File Creation: 
Create a file named sample_data.txt in your home directory and add some sample text to it.

**Answer 1:** To create a new file in the home directory and add text, I used the touch command followed by echo and output redirection (>). I also used the cat command to check if the text has been successfully included in the file.

Command: **touch sample_data.txt** & **echo "Once upon a time, the planets and the fates and all the stars aligned." > sample_data.txt**
<img width="1063" height="683" alt="Screenshot (655)" src="https://github.com/user-attachments/assets/12c58efb-7304-4c4b-8d7c-c2312f7e5d2e" />

2. Hard Link Creation: 
Create a hard link to sample_data.txt named sample_hard.txt.

**Answer 2:** A hard link is a direct reference to the same data (inode) on the disk as the original file. I used the **ln** command to create the hard link.

Command: **ln sample_data.txt sample_hard.txt**
<img width="1052" height="673" alt="Screenshot (656)" src="https://github.com/user-attachments/assets/8e61ccc2-3072-4217-83ac-540ec7f35798" />

3. Symbolic Link Creation: 
Create a symbolic (soft) link to sample_data.txt named sample_soft.txt.

**Answer 3:** A symbolic (soft) link is a special file that acts as a shortcut by containing the path to the target file. To create a soft link, I used the command **ln** with the **-s** option.

Command: **ln -s sample_data.txt sample_soft.txt**
<img width="1045" height="669" alt="Screenshot (657)" src="https://github.com/user-attachments/assets/1ee4ac6d-4e28-4aff-9259-2775262e6919" />

4. Inode Verification: 
Display the inode numbers of sample_data.txt, sample_hard.txt, and sample_soft.txt.

**Answer 4:** To view the unique inode numbers associated with each file, I used the ls command with the -i option.

Command: **ls -i sample_data.txt sample_hard.txt sample_soft.txt**
<img width="1047" height="675" alt="Screenshot (658)" src="https://github.com/user-attachments/assets/0cacf7bb-d139-4b82-94df-9af3fc1d6894" />

5. Inode Analysis: 
Identify which files share the same inode number and briefly explain the reason.

**Answer 5:** The files sample_data.txt and sample_hard.txt shares the same inode number. This is because hard links are essentially different names for the same underlying data on the disk.

But sample_soft.txt will have a different inode because a symbolic link is a separate file that simply points to the path of the original.
<img width="948" height="85" alt="image" src="https://github.com/user-attachments/assets/54b92002-ad2f-47d8-b2c8-b69357699de9" />

6. File Metadata Inspection: 
Display detailed file information (permissions, ownership, size, timestamps) of sample_data.txt.

**Answer 6:** To view detailed information such as permissions, ownership, size, and timestamps, I used the ls -l (long format) command.

Command: **ls -l sample_data.txt**
<img width="1041" height="656" alt="Screenshot (659)" src="https://github.com/user-attachments/assets/53736ca9-044b-40a8-a603-df84fb6cd208" />

7. Disk Usage Check: 
Display the disk usage of your home directory in a human-readable format.

**Answer 7:** To estimate the disk space used by the home directory in a human-readable format (KB, MB, GB), I used the **du** command with the **-h** option, and the -s option was used to provide a summary total. **du -h** command will give a long, detailed list to scroll through, while using **-sh** gives the summary.

Command: **du -sh ~**
<img width="1040" height="660" alt="Screenshot (660)" src="https://github.com/user-attachments/assets/a3c58eae-3814-4738-8eb5-33120ed8d1f4" />


8. File Size Overview: 
Display the size of each file present in your home directory in a human-readable format.

**Answer 8:** To list all files in my home directory along with their sizes in a readable format, I combined ls with the -lh options.

Command: **ls -lh ~**
<img width="1039" height="752" alt="Screenshot (661)" src="https://github.com/user-attachments/assets/05375151-d8dc-4ada-ae6f-0b3c1c75dfa5" />

9. Link Deletion Test: 
Delete the symbolic link sample_soft.txt and verify that the original file sample_data.txt is unaffected.

**Answer 9:** Deleting a symbolic link does not affect the original file because a symbolic link is a separate file that simply points to the path of the original.

- Command: **rm sample_soft.txt** (or unlink sample_soft.txt)

- Verification: Run ls sample_data.txt to confirm the original still exists.
<img width="1036" height="584" alt="Screenshot (662)" src="https://github.com/user-attachments/assets/397ffe56-96f4-49cb-a1b8-7569e7d649f3" />

10. Disk Utility Demonstration: 
Demonstrate the usage of du and df commands using various useful options and briefly explain the output.

**Answer 10:** The du and df commands are essential for monitoring storage:

- du -h --max-depth=1: Displays the disk usage of immediate subdirectories in a human-readable format.
  <img width="1129" height="794" alt="Screenshot (663)" src="https://github.com/user-attachments/assets/068f17a6-85e6-4a4f-ad57-88b3895d9a25" />

- du -ch: Displays usage for all specified files/directories and includes a grand total at the end. The screenshot includes only the last lines as the list is too long to take individual screenshots of.
  <img width="1255" height="798" alt="Screenshot (664)" src="https://github.com/user-attachments/assets/79fee2e7-179e-44a7-99dc-c8c4443d07b6" />

- df -h: Shows the total, used, and available space on all mounted file systems.
  <img width="1920" height="387" alt="Screenshot (665)" src="https://github.com/user-attachments/assets/dea2f547-9de2-4b7b-ade8-aa1a3d06fbb9" />

- df -T: Displays the file system type (such as ext4 or XFS) alongside the usage data.
  <img width="1920" height="651" alt="Screenshot (666)" src="https://github.com/user-attachments/assets/5f666f3b-0460-4d69-97ba-8e1f0a40aa67" />

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

In Linux, background processing allows a task to run independently of the active terminal. To execute a command in the background, append an ampersand (&) to the end of the command (e.g., sleep 100 &). I verified it is running by using the ps command.

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

<h3>The assignment has been completed</h3>
