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
