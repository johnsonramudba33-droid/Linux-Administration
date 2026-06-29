================================================================================
RNOS TECHNOLOGY
PostgreSQL DBA Training Program

DAY 03 – LINUX FILE MANAGEMENT COMMANDS

================================================================================

Objective
---------
Understand Linux file management commands, file creation, editing,
viewing, copying, moving, deleting, and disk usage monitoring used by
Linux Administrators and Database Administrators.

================================================================================
1. PACKAGE INSTALLATION
================================================================================

Purpose:
--------
Install software packages from Ubuntu repositories.

Syntax:

apt install <package_name>

Examples:

apt install ncal

apt install tree

apt install curl

apt install net-tools

Real-Time DBA Usage:
--------------------
Install monitoring tools.
Install PostgreSQL dependencies.
Install troubleshooting utilities.

================================================================================
2. WHOAMI COMMAND
================================================================================

Purpose:
--------
Display current logged-in user.

Command:

whoami

Example Output:

root

or

ubuntu

Real-Time DBA Usage:
--------------------
Verify current user before executing administrative commands.

================================================================================
3. HISTORY COMMAND
================================================================================

Purpose:
--------
Display previously executed commands.

Commands:

history

history 20

history | grep ssh

history | grep apt

Example Output:

101 apt install curl
102 systemctl status ssh
103 history

Real-Time DBA Usage:
--------------------
Audit executed commands.
Troubleshoot accidental changes.

================================================================================
4. UNAME COMMAND
================================================================================

Purpose:
--------
Display Linux kernel information.

Commands:

uname

uname -a

Example Output:

Linux

Linux rnos-session 6.8.0-60-generic x86_64 GNU/Linux

Real-Time DBA Usage:
--------------------
Verify operating system version before installing software.

================================================================================
5. DATE COMMAND
================================================================================

Purpose:
--------
Display current system date and time.

Commands:

date

date -I

date +%m

date +%M%y

Example Output:

Mon Jun 29 10:15:35 UTC 2026

2026-06-29

06

1526

Real-Time DBA Usage:
--------------------
Timestamp backup files.
Generate daily reports.
Verify server time.

================================================================================
6. CALENDAR COMMAND
================================================================================

Commands:

cal

cal 2027

cal 1 2026

Purpose:
--------
Display calendar.

Real-Time DBA Usage:
--------------------
Plan maintenance windows.
Schedule patching activities.

================================================================================
7. DISK USAGE COMMAND
================================================================================

Purpose:
--------
Display directory and file sizes.

Commands:

du -sh data

du -sh *

du -sh * | sort -hr

Example Output:

93G     data
200M    log
46M     new_welina_db
228K    restore.log
128K    stream_restore.log

Real-Time DBA Usage:
--------------------
Identify large directories.
Monitor database growth.
Find disk-consuming files.

================================================================================
8. PRESENT WORKING DIRECTORY
================================================================================

Command:

pwd

Example Output:

/app/postgres

Purpose:
--------
Display current directory.

================================================================================
9. LIST FILES
================================================================================

Commands:

ls

ls -l

ls -lr

ls -lrth

Example Output:

-rw-r--r-- demo.txt

drwxr-xr-x data

Purpose:
--------
Display directory contents.

Real-Time DBA Usage:
--------------------
Verify backup files.
Check configuration files.
Confirm log file creation.

================================================================================
10. CREATE FILE
================================================================================

Command:

touch demo.txt

touch welina_tracker

Verify:

ls -lrth

Purpose:
--------
Create an empty file.

================================================================================
11. FILE EDITOR
================================================================================

Command:

vi demo.txt

Insert Mode:

Press i

Save & Exit:

ESC
:wq

Exit Without Saving:

ESC
:q!

Purpose:
--------
Edit configuration files.

Real-Time DBA Usage:
--------------------
Modify application configuration.
Edit shell scripts.
Update Linux configuration files.

================================================================================
12. VIEW FILE CONTENT
================================================================================

CAT COMMAND

cat demo.txt

cat -n demo.txt

Purpose:
--------
Display complete file content.

------------------------------------------------------------

MORE COMMAND

more demo.txt

Purpose:
--------
View file page by page.

------------------------------------------------------------

LESS COMMAND

less demo.txt

Purpose:
--------
Navigate large files efficiently.

Real-Time DBA Usage:
--------------------
Read configuration files.
Analyze application logs.
View backup reports.

================================================================================
13. COPY FILE
================================================================================

Command:

cp demo.txt demo_backup_`date -I`

Example:

cp welina_track welina_track_backup_`date -I`

Verify:

ls -lrth

Purpose:
--------
Create backup copies.

Real-Time DBA Usage:
--------------------
Backup configuration files before modification.

================================================================================
14. MOVE / RENAME FILE
================================================================================

Command:

mv demo.txt demo_new.txt

Verify:

ls -lrth

Purpose:
--------
Rename or move files.

Real-Time DBA Usage:
--------------------
Rename backup files.
Move log files.
Archive reports.

================================================================================
15. DELETE FILE
================================================================================

Command:

rm demo_new.txt

Delete Forcefully:

rm -rf demo_new.txt

Verify:

ls

Purpose:
--------
Delete unwanted files.

Real-Time DBA Usage:
--------------------
Remove temporary files.
Delete old reports.
Clean obsolete backup files.

================================================================================
REAL-TIME SCENARIO
================================================================================

Scenario:

Database server disk usage reaches 95%.

Step 1

du -sh *

Find largest directory.

Step 2

ls -lrth

Identify backup files.

Step 3

cp important.conf important.conf_backup_`date -I`

Take backup.

Step 4

vi important.conf

Modify configuration.

Step 5

cat important.conf

Verify changes.

================================================================================
INTERVIEW QUESTIONS
================================================================================

Q1. Which command displays current logged-in user?

Answer:

whoami

------------------------------------------------------------

Q2. Which command displays current directory?

Answer:

pwd

------------------------------------------------------------

Q3. Which command displays file size?

Answer:

du -sh

------------------------------------------------------------

Q4. Which command displays operating system information?

Answer:

uname -a

------------------------------------------------------------

Q5. Which command creates an empty file?

Answer:

touch

------------------------------------------------------------

Q6. Which command copies a file?

Answer:

cp

------------------------------------------------------------

Q7. Which command renames a file?

Answer:

mv

------------------------------------------------------------

Q8. Which command deletes a file?

Answer:

rm

================================================================================
STUDENT PRACTICALS
================================================================================

1. Install tree package.
2. Verify current user.
3. Display command history.
4. Display Linux version.
5. Display current date.
6. Display calendar.
7. Check directory size.
8. Create a file.
9. Edit the file using vi.
10. Display file using cat.
11. View file using more.
12. View file using less.
13. Copy the file.
14. Rename the file.
15. Delete the file.
16. Verify deletion.

================================================================================
IMPORTANT COMMANDS LEARNED TODAY
================================================================================

apt install
whoami
history
uname
uname -a
date
cal
du
pwd
ls
touch
vi
cat
more
less
cp
mv
rm

================================================================================
Prepared By:
RNOS Technology

PostgreSQL DBA Training Program

DAY 03 – Linux File Management Commands

Version 2.0

================================================================================