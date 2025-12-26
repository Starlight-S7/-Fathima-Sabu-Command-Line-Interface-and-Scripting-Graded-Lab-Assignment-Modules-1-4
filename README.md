# -Fathima-Sabu-Command-Line-Interface-and-Scripting-Graded-Lab-Assignment-Modules-1-4
This repository contains the completed assignment of the Command Line Interface and Scripting Graded Lab Assignment done by Fathima Sabu
**Coursera Labs** was used to complete this assignment.

<h2>Question 1</h2>
You have just joined IxD Systems as a junior systems engineer. On your first day, the Linux administrator asks you to perform a basic environment verification on the lab machine using your own login account.

1. User Identity Verification
Display your currently logged-in username and all groups your user account belongs to.
Your name or login ID must appear in the output.

**Answer 1:** I used the command whoami to display my current logged-in username. To see all groups that my user account belongs to, along with my unique user ID (UID), I used the id command
Command: **whoami** and **id**
<img width="1790" height="895" alt="Screenshot (625)" src="https://github.com/user-attachments/assets/db7cd89c-e845-4157-b50b-cfefdf140696" />
I used the **clear** command after each question's commands to keep it looking tidy and easy to spot.

2. Workspace Validation
Display the current working directory and list all files and directories in that location using long format listing.

**Answer 2:** To display my current working directory, I used the **pwd** (print working directory) command.
And to list all files and directories in that location in a detailed format, I used **ls -l**, which provides the long format listing including permissions, owner, and size.
Command: **pwd** and **ls -l**
<img width="1122" height="716" alt="Screenshot (626)" src="https://github.com/user-attachments/assets/537de018-6f1f-4936-8071-f31a0713a7db" />
<img width="1079" height="683" alt="Screenshot (627)" src="https://github.com/user-attachments/assets/6e50f3bc-b071-4d4a-88ba-d48fd42a6408" />

3. Environment Confirmation File
Create a file named user_info.txt and write the line:
"Linux user environment verified"

**Answer 3:** To create the file and write the specific string to it, I used the echo command combined with output redirection (>). The > symbol redirects the text into the specified file, creating it if it does not exist. This was the easier way. The longer way would've been to first use the **touch** command to create the file and then use the **echo** command to write the line into the file.
Then I used the **cat** command to check if it worked. The proper command used was **cat user_info.txt**. This showed that the line was written successfully, as shown in the screenshot.
Command: **echo "Linux user environment verified" > user_info.txt**
<img width="1088" height="686" alt="Screenshot (629)" src="https://github.com/user-attachments/assets/236f1633-e79b-4927-804a-72974d446e22" />

4. File Integrity Check
Display the number of characters present in user_info.txt.

**Answer 4:** I used the Linux command **wc -m user_info.txt** to display the number of characters present in the user_info.txt file.
It was observed that there were 32 characters in the user_info.txt file.
Command: **wc -m user_info.txt**
<img width="1065" height="677" alt="Screenshot (640)" src="https://github.com/user-attachments/assets/9d2b1500-8d26-42b5-a3b9-1079ea628c3c" />

5. Learning the Tools
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

6. Home Directory Inspection
List the contents of your home directory sorted alphabetically.

**Answer 6:** The home directory is represented by the tilde (~) symbol. To list its contents, I used the **ls ~** command. By default, ls lists entries alphabetically.
Command: **ls ~**
<img width="1064" height="683" alt="Screenshot (642)" src="https://github.com/user-attachments/assets/b5366364-fcc9-48f2-8bc3-d36b24b3c95b" />

7. Log Investigation
Search for the word "admin" inside a file named log.txt and display only the matching lines.

**Answer 7:** To search for the word "admin" and display only the matching lines, I used the grep command, which is designed for pattern matching within files. I first created the log.txt file using the **touch** command and edited it using vim to contain some lines, since the file was not pre-existing in the system provided.
Command: **grep -n "admin" log.txt**
<img width="1065" height="667" alt="Screenshot (634)" src="https://github.com/user-attachments/assets/17886fe9-aeda-4a4e-9c3c-401ed4eee6de" />
<img width="1046" height="670" alt="Screenshot (635)" src="https://github.com/user-attachments/assets/251c1d9d-34d6-42eb-af7e-950dbd65fff2" />

8. System Information Check
Display the Linux kernel version currently running.

**Answer 8:** To display the current running kernel version, the command I used is **uname -r**.
Command: **uname -r**
<img width="1051" height="667" alt="Screenshot (636)" src="https://github.com/user-attachments/assets/512cbdd8-bbca-46ab-9f50-d6a919e5f097" />

9. Network Connectivity Test
Verify network connectivity by sending ICMP packets to www.google.com.

**Answer 9:** I used the ping command to verify connectivity. It sends ICMP Echo Request packets to the destination and waits for a reply to measure performance.
Command: **ping www.google.com**
<img width="1051" height="685" alt="Screenshot (637)" src="https://github.com/user-attachments/assets/c8d1e282-faeb-44d1-9caf-7823fd13b395" />

10. System Health Awareness
Display the command used to check system uptime and briefly explain its output (uptime duration, number of users, load average).

**Answer 10:** I used the command **uptime** to get the uptime duration, number of users, and load average.
Uptime duration: How long the system has been running since the last boot.
Number of users: How many users are currently logged in (similar to information provided by who -q).
Load average: The average system load over the last 1, 5, and 15 minutes.
<img width="1050" height="668" alt="Screenshot (639)" src="https://github.com/user-attachments/assets/a8956924-6f8f-4b2e-96fa-084da926adb1" />
The **top** command can be used for monitoring real-time system activity, including CPU and memory usage.
<img width="1058" height="667" alt="Screenshot (638)" src="https://github.com/user-attachments/assets/32a34dfa-6097-4ba5-8036-2bd678bd9202" />

<h2>Question 2</h2>
You are working as a junior system administrator responsible for organizing project-related files in your home directory.
Your supervisor wants you to demonstrate your understanding of Linux file and directory management commands.

1. Project Workspace Setup
Create a directory named documents inside your home directory. This directory will store your project-related files.

**Answer 1:** To create the documents directory in my home directory, I used the mkdir command. The tilde (~) symbol is a shortcut for the home directory. I have used the **ls** command to show that the directory has been created.
Command: mkdir ~/documents
<img width="1068" height="672" alt="Screenshot (643)" src="https://github.com/user-attachments/assets/1f74a083-297f-4e35-9222-fe434f893675" />

2. File Creation
Navigate into the documents directory and create a file named plan.txt.

**Answer 2:** I navigated into the new directory using **cd** (change directory) and then created the plan.txt file using the **touch** command.
Command: **cd ~/documents** & **touch plan.txt**
<img width="1077" height="678" alt="Screenshot (644)" src="https://github.com/user-attachments/assets/f9c852c0-0c30-4d8f-a418-bb4f2dcb065f" />

3. Content Addition
Write some sample text of your choice into the plan.txt file. The content can be a short project note or reminder.

**Answer 3:** To add text to the file, I used the echo command with the > redirection symbol, which sends the text into the file.
Command: **echo "Reminder to complete the YouTube script on the story behind the first computer worm" > plan.txt**
<img width="1067" height="672" alt="Screenshot (645)" src="https://github.com/user-attachments/assets/a7cb5fbb-96f7-4fb1-b3d5-4ca30bf76ed0" />

4. File Metadata Verification
Display the permissions and ownership details of the plan.txt file. Ensure your username appears in the output.

**Answer 4:** To view the permissions, owner, and group details, I used ls -l (long format listing). The username in my system, which is "coder", appears on the output.
Command: **ls -l plan.txt**
<img width="1057" height="670" alt="Screenshot (646)" src="https://github.com/user-attachments/assets/b0d2346c-a953-45ef-a094-2386a6ea78e0" />

5. File Duplication
Create a copy of plan.txt and name it plan_copy.txt.

**Answer 5:** I used the cp (copy) command to create a duplicate of the **plan.txt** file.
Command: **cp plan.txt plan_copy.txt**
<img width="1072" height="675" alt="Screenshot (648)" src="https://github.com/user-attachments/assets/4b8f97ad-12cc-43d7-830a-22411fd210b2" />

6. Directory Renaming
Rename the documents directory to project_documents to reflect the project scope more clearly.

**Answer 6:** The mv (move) command is used for both moving and renaming files or directories. Therefore, I used the mv command with the directory names. I was in the directory that was being renamed, so I went back using **cd ..** and then used the **ls** command to check if the name had been changed. The name was changed successfully. Then I used cd with the directory name to go back inside the directory to do the further questions.
Command: **mv ~/documents ~/project_documents**
<img width="1055" height="672" alt="Screenshot (650)" src="https://github.com/user-attachments/assets/7128cb3f-05d1-477a-8897-307309f0a675" />

7. Archival Structure
Inside the project_documents directory, create a subdirectory named archive.

**Answer 7:** After navigating into the renamed directory, I used **mkdir** again to create the archive subdirectory. Then used **ls** to check if it had been created. The sub-directory had been successfully created.
Command: **mkdir archive**
<img width="1059" height="667" alt="Screenshot (651)" src="https://github.com/user-attachments/assets/2ab01cf0-39d2-4cdc-98c8-49d0cb1dd163" />

8. File Organization
Move plan_copy.txt into the archive subdirectory.

**Answer 8:** I moved the plan_copy.txt file into the archive directory using the mv command. I then used cd to change the directory to archive, then used ls to check if the file has been successfully tranferred. I also went back and checked if the file had been moved from the first directory to the subdirectory. The process was successful.
Command: **mv plan_copy.txt archive**
<img width="1056" height="667" alt="Screenshot (652)" src="https://github.com/user-attachments/assets/686f21ed-7cc0-43c2-8f59-03b75f464bad" />

9. Recursive Listing
List all files and subdirectories inside project_documents recursively so that the complete directory structure is visible.

**Answer 9:** To view the complete directory structure, including the contents of the archive subdirectory, I used ls -R (recursive listing). This command was used when I was already in the project_documents directory. If I were in the home directory, I would also have to include the path to that directory.
Command: **ls -R** & **ls -R ~/project_documents**
<img width="1052" height="667" alt="Screenshot (653)" src="https://github.com/user-attachments/assets/dd1313e1-1000-418a-adfb-863ce9bcff1a" />

10. Path Verification
Display the absolute path of the plan_copy.txt file after it has been moved to the archive directory.

**Answer 10:** I navigated into the archive directory and used **pwd** (print working directory) to display the absolute path, which shows the full location starting from the root ("/").
Command: **cd archive** then **pwd**
<img width="1052" height="667" alt="Screenshot (654)" src="https://github.com/user-attachments/assets/244612b9-245f-4a9f-9a8a-328a4ae97ea0" />

<h2>Question 3</h2>
