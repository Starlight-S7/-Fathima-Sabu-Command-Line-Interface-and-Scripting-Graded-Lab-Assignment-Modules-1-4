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
