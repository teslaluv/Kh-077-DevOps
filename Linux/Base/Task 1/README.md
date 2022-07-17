# Linux Base
## Task1. Part1
1) Log in to the system as root.
2) Use the passwd command to change the password. Examine the basic
parameters of the command. What system file does it change *?

![Screenshot_2](https://user-images.githubusercontent.com/109180406/179379415-b30c536a-a0fe-41bd-b8ce-4ded693f63ff.png)

It changes /etc/passwd file

3) Determine the users registered in the system, as well as what commands they
execute. What additional information can be gleaned from the command
execution?

![Screenshot_31](https://user-images.githubusercontent.com/109180406/179379411-d92aa677-87d1-40e7-b63d-d938f5c81b8d.png)

The results of the w command:

- User ⁠— username.
- TTY ⁠— terminal name
- From ⁠— the name of the remote host.
- Login@ ⁠— login time.
- Idle ⁠— idle time.
- JCPU ⁠— the amount of time used by processes attached to the TTY.
- PCPU ⁠— the time used by the process displayed in the WHAT field.
- WHAT ⁠— the user’s current process.

4) Change personal information about yourself.

![Screenshot_3](https://user-images.githubusercontent.com/109180406/179375479-4073cbef-106b-45cc-b362-4753567b0aba.png)

5) Become familiar with the Linux help system and the man and info commands.
Get help on the previously discussed commands, define and describe any two
keys for these commands. Give examples.

For example, the passwd command has a -d option (deletes the password for the specified account). The w command also has the option -s (Short format).

6) Explore the more and less commands using the help system. View the contents
of files .bash* using commands.

![Screenshot_4](https://user-images.githubusercontent.com/109180406/179375494-30e3e35a-f0d5-4ce5-b9c9-335d7fa60f29.png)

![Screenshot_5](https://user-images.githubusercontent.com/109180406/179375513-2eca92c5-56dc-4d59-9ced-64f1a831acba.png)


7) Describe in plans that you are working on laboratory work 1. Tip: You should
read the documentation for the finger command.

![Screenshot_7](https://user-images.githubusercontent.com/109180406/179375567-fbfef6bf-e325-47be-8b34-8dc82cc5f74e.png)

![Screenshot_8](https://user-images.githubusercontent.com/109180406/179375570-b057866c-c473-4349-81eb-07df32f474e2.png)

8) List the contents of the home directory using the ls command, define its files
and directories. Hint: Use the help system to familiarize yourself with the ls
command.

![Screenshot_32](https://user-images.githubusercontent.com/109180406/179375611-fb63b6a8-0a1b-4c01-8534-e1057172c5f2.png)

## Task1.Part2
1) Examine the tree command. Master the technique of applying a template, for
example, display all files that contain a character c, or files that contain a
specific sequence of characters. List subdirectories of the root directory up to
and including the second nesting level.

![Screenshot_10](https://user-images.githubusercontent.com/109180406/179375749-6c3d800e-69e9-4934-9095-186305c125c6.png)

![Screenshot_11](https://user-images.githubusercontent.com/109180406/179375750-1ea55533-bdfe-4cc1-8b7c-b047de495a5e.png)

2) What command can be used to determine the type of file (for example, text or
binary)? Give an example.

![Screenshot_12](https://user-images.githubusercontent.com/109180406/179375756-04526c63-f782-4861-8725-e02e360aa4bf.png)

3) Master the skills of navigating the file system using relative and absolute paths.
How can you go back to your home directory from anywhere in the filesystem?

![Screenshot_13](https://user-images.githubusercontent.com/109180406/179375764-a6d52a60-902f-427d-898c-5bd5a750cd05.png)

4) Become familiar with the various options for the ls command. Give examples
of listing directories using different keys. Explain the information displayed on
the terminal using the -l and -a switches.

![Screenshot_14](https://user-images.githubusercontent.com/109180406/179375774-a1bfeefa-12a2-497b-b2d5-b52603dc1629.png)

–a
Lists all entries including those starting with a period (.).

–l
Displays permissions, links, owner, group, size, time, name. See Long output format for details.

5) Perform the following sequence of operations:
- create a subdirectory in the home directory;
- in this subdirectory create a file containing information about directories
located in the root directory (using I/O redirection operations);
- view the created file;
- copy the created file to your home directory using relative and absolute
addressing.
- delete the previously created subdirectory with the file requesting removal;
- delete the file copied to the home directory.

![Screenshot_16](https://user-images.githubusercontent.com/109180406/179375885-2bbb0fe5-13bd-4d53-a3f8-5f9176d19b3b.png)

![Screenshot_15](https://user-images.githubusercontent.com/109180406/179375890-9e9fe08b-e2a3-4525-ae25-bf3d4b460e3d.png)

![Screenshot_17](https://user-images.githubusercontent.com/109180406/179375896-e3559ad5-cfef-4583-964d-1c53be1926ff.png)

![Screenshot_18](https://user-images.githubusercontent.com/109180406/179375898-51eb8fdb-ae14-4627-8805-4d0a1ecfd4ea.png)

6) Perform the following sequence of operations:
- create a subdirectory test in the home directory;

- copy the .bash_history file to this directory while changing its name to
labwork2;
- create a hard and soft link to the labwork2 file in the test subdirectory;
- how to define soft and hard link, what do these
concepts;
- change the data by opening a symbolic link. What changes will happen and
why
- rename the hard link file to hard_lnk_labwork2;
- rename the soft link file to symb_lnk_labwork2 file;
- then delete the labwork2. What changes have occurred and why?
7) Using the locate utility, find all files that contain the squid and traceroute
sequence.

![image](https://user-images.githubusercontent.com/109180406/179427163-f07f792a-8f10-4106-b627-737847c6d443.png)

![image](https://user-images.githubusercontent.com/109180406/179427196-570457eb-4cd1-4494-a118-43df27108888.png)


8) Determine which partitions are mounted in the system, as well as the types of
these partitions.

![image](https://user-images.githubusercontent.com/109180406/179426688-403c4ae5-37ee-4004-99c8-a42f054f3db5.png)

9) Count the number of lines containing a given sequence of characters in a given
file.

![Screenshot_22](https://user-images.githubusercontent.com/109180406/179375919-6a99646f-cbb3-40a7-8fa7-9f39b0073128.png)

10) Using the find command, find all files in the /etc directory containing the
host character sequence.

![Screenshot_23](https://user-images.githubusercontent.com/109180406/179375924-573b5255-b858-421f-b40e-25a905d39039.png)

11) List all objects in /etc that contain the ss character sequence. How can I
duplicate a similar command using a bunch of grep?

![Screenshot_24](https://user-images.githubusercontent.com/109180406/179375929-e447fa86-be6a-4008-8ea6-1076254f4275.png)

![Screenshot_25](https://user-images.githubusercontent.com/109180406/179375936-c3844a16-9a5a-4bcc-bc7a-49841e77488e.png)

![Screenshot_27](https://user-images.githubusercontent.com/109180406/179375950-ba3f9bb2-557b-4330-a42b-3a2538c2e0c1.png)

12) Organize a screen-by-screen print of the contents of the /etc directory. Hint:
You must use stream redirection operations.

![image](https://user-images.githubusercontent.com/109180406/179426814-f9f38b97-a308-4e00-8b7c-7b52351941f4.png)

13) What are the types of devices and how to determine the type of device? Give examples.

Linux supports three types of hardware device: character, block and network.

14) How to determine the type of file in the system, what types of files are there?

With the help of these commands, we can determine the type of file in the system:

- df
- fsck
- lsblk
- mount
- file

In Linux there are basically three types of files:

- Ordinary/Regular files
- Special files
- Directories

15) List the first 5 directory files that were recently accessed in the /etc
directory.

![Screenshot_35](https://user-images.githubusercontent.com/109180406/179379672-59463a84-4c7d-4b5b-ba14-caf48025b677.png)



