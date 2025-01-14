# Labaratory-LinuxCommandLine101
Laboratory for Day 1: Linux Basics
Objective:

    Learn to work with files, directories, and permissions.
    Familiarize yourself with the structure of a Linux system.

Laboratory Setup
Tools:

    Install VirtualBox or VMware.
    Create a virtual machine (Ubuntu/Debian).
    If you cannot use virtual machines, try these alternatives:
        Linux Survival.
        JSLinux (Linux emulator in a browser).

Environment:

    Local user with administrator rights (sudo).
    Pre-created empty working directory: /home/your_user/my_lab.

Laboratory Tasks
1. Explore the File System

    Navigate to your home directory:

cd ~

View the list of files:

ls -al

Explore the root file system:

    cd /
    ls

What to find:

    Key directories: /bin, /home, /etc, /var.

2. Directory Navigation and Structure

    Create a directory my_lab in your home folder:

mkdir ~/my_lab

Inside my_lab, create the following structure:

    my_lab/
    ├── projects/
    ├── notes/
    └── scripts/

Commands:

mkdir ~/my_lab/projects
mkdir ~/my_lab/notes
mkdir ~/my_lab/scripts

3. File Operations

    Create an empty text file in the notes folder:

touch ~/my_lab/notes/day1.txt

Add text to the file:

echo "These are my day one notes" > ~/my_lab/notes/day1.txt

Copy the file to the projects folder:

cp ~/my_lab/notes/day1.txt ~/my_lab/projects/

Rename the file in the projects folder:

mv ~/my_lab/projects/day1.txt ~/my_lab/projects/day1_notes.txt

Delete the file:

    rm ~/my_lab/projects/day1_notes.txt

4. File Permissions

    Examine file permissions:

ls -l ~/my_lab/notes/day1.txt

Set permissions: allow only the owner to read and write the file.

chmod 600 ~/my_lab/notes/day1.txt

Verify the updated permissions:

    ls -l ~/my_lab/notes/day1.txt

5. Simple Test

    Try deleting the scripts folder if it is empty:

    rmdir ~/my_lab/scripts

Completing the Lab

    Review:
        Check the directory structure:

    tree ~/my_lab

    Ensure all tasks are completed.

Clean Up:

    Delete the created files and directories if they are no longer needed:

        rm -r ~/my_lab

Advanced Task:

    Write a simple Bash script to create the directory structure and add files with text automatically:

    #!/bin/bash
    mkdir ~/my_lab
    mkdir ~/my_lab/projects ~/my_lab/notes ~/my_lab/scripts
    echo "This is an automatically created file" > ~/my_lab/notes/day1.txt

Save the script as setup_lab.sh, make it executable (chmod +x setup_lab.sh), and run it:

./setup_lab.sh
