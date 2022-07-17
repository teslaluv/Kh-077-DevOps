# Task2
Task assignment.
1) Analyze the structure of the /etc/passwd and /etc/group file, what fields are 
present in it, what users exist on the system? Specify several pseudo-users, how 
to define them?

This file contains lines of the following form, separated by colons:
username: pswd: uid: gid: uid comments: directory: shell
Where:
- username - username
- pswd - password
- uid - unique identifier of the user within the system
- gid - unique identifier of the group within the system to which the user belongs
- uid comments - comment, extended user description, for example, full name
- directory - user's home directory
- shell - program name - the user's command interpreter

users with UIDs in the range of 1-999 are (daemons, pseudo-users, system and reserved users)

2) What are the uid ranges? What is UID? How to define it?

uid is a simple numeric designation for an individual user. This is usually a positive number not more
than 65535 (sometimes 32-bit). Some identifiers are reserved for special use. These include 0 (root),
1-999(daemons, pseudo-users, system and reserved users), 1000+ (regular users).

3) What is GID? How to define it?

Groups in Linux are defined by GIDs (group IDs). Just like with UIDs, the first 100 GIDs are usually reserved for system use. The GID of 0 corresponds to the root group and the GID of 100 usually represents the users group. GIDs are stored in the /etc/groups file.

4) How to determine belonging of user to the specific group?

groups [username]

5) What are the commands for adding a user to the system? What are the basic 
parameters required to create a user?

useradd [options] username
passwd username

6) How do I change the name (account name) of an existing user?

usermod -l newUsername oldUsername

7) What is skell_dir? What is its structure?

skell_dir is the directory containing the files to copy to the newly created own directory.

8) How to remove a user from the system (including his mailbox)?

userdel -r username

9) What commands and keys should be used to lock and unlock a user account?

Lock users in Linux:
passwd -l username
usermod -l username

Unlock users in Linux:
passwd -u username
usermod -u username

10) How to remove a user's password and provide him with a password-free 
login for subsequent password change?
11) Display the extended format of information about the directory, tell about 
the information columns displayed on the terminal.

The ls command lists files and directories within the file system, and shows detailed information about them.
The default output of the ls command shows only the names of the files and directories, which is not very informative.

The -l ( lowercase L) option tells ls to print files in a long listing format.

When the long listing format is used, you can see the following file information:
- The file type.
- The file permissions.
- Number of hard links to the file.
- File owner.
- File group.
- File size.
- Date and Time.
- File name.

12) What access rights exist and for whom (i. e., describe the main roles)? 
Briefly describe the acronym for access rights.

Types of Users:
Owner:
The user who creates the file or folder is the owner of that file or folder, and the owner can permit the other types of users to access that file and folder. It is denoted by ‘u’.

Group:
Each user can belong to a particular group in Linux. So, when a user creates a file or folder, then other members of the group where the user belongs can access the file or folder. When multiple users work on a particular folder, then it is better to create a group with those users to access that folder properly. It is denoted by ‘g’.

Others/All:
It indicates any user who is not the owner of a particular file or folder and does not belong to the file or folder owner’s group. If the owner of the file or folder gives any access permission to others, then any users can do that particular access only. ‘o’ is used to denote other users, and ‘a’ is used to denote all users.

Permission Types:
Three permission types exist in the Linux system, which is mentioned below.

Read:
This permission is used to read any file or folder only. It is denoted by ‘r’ when it is defined by character, and it is denoted by 4 when it is defined by a number.

Write:
This permission is used to write, append, or override any file or folder. It is denoted by ‘w’ when it is defined by the character, and it is denoted by 2 when it is defined by the number. If the user has to write permission to a file, but he/she has not to write permission on the folder where the file is located, then the user can modify the content of the file only, but he/she will not able to rename, move or delete the file.

Execute:
This permission is used to execute any file only. It is denoted by ‘x’ when it is defined by the character, and it is denoted by 1 when it is defined by the number.

13) What is the sequence of defining the relationship between the file and the 
user?

When clarifying the relationship between a file and the user who started the process, the role is defined as follows:

- If the UID of the file matches the UID of the process, the user is the owner of the file

- If the file's GID matches the GID of any group the user is a member of, the user is a member of the group that owns the file.

- If neither the UID nor the GID of the file overlap with the UID of the process and the list of groups that the user who launched it belongs to, that user is an outsider.

14) What commands are used to change the owner of a file (directory), as well 
as the mode of access to the file? Give examples, demonstrate on the terminal.

chown [OPTIONS] USER[:GROUP] FILE(s)

![Screenshot_38](https://user-images.githubusercontent.com/109180406/179394482-0adc3511-8715-426b-bca4-a436d53ab334.png)

15) What is an example of octal representation of access rights? Describe the 
umask command.

The umask command in Linux is used to set default permissions for files or directories the user creates.

How does the umask command work?
- The umask command specifies the permissions that the user does not want to be given out to the newly created file or directory.
- umask works by doing a Bitwise AND with the bitwise complement(where the bits are inverted, i.e. 1 becomes 0 and 0 becomes 1) of the umask.
- The bits which are set in the umask value, refer to the permissions, which are not assigned by default, as these values are subtracted from the maximum permission for files/directories.

![Screenshot_36](https://user-images.githubusercontent.com/109180406/179394094-453aacee-b3c6-45bb-b1a8-a30b2e0ebddc.png)

16) Give definitions of sticky bits and mechanism of identifier substitution. Give 
an example of files and directories with these attributes.
17) What file attributes should be present in the command script?
