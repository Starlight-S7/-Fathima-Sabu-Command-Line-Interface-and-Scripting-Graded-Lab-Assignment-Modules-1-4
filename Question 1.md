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
