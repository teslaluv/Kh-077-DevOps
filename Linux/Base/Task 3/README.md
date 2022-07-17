# TASK 3
## Part 1
1. How many states could has a process in Linux?

There are five Linux process states. They are as follows: running & runnable, interruptable_sleep, uninterruptable_sleep, stopped, and zombie.

2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current 
process.

`pstree -h`

This command highlights the current process and its ancestors.

3. What is a proc file system?

Proc file system (procfs) is virtual file system created on fly when system boots and is dissolved at time of system shut down.
It contains useful information about the processes that are currently running, it is regarded as control and information center for kernel.
The proc file system also provides communication medium between kernel space and user space.

4. Print information about the processor (its type, supported technologies, etc.).

`cat /proc/cpuinfo`

5. Use the ps command to get information about the process. The information should be as 
follows: the owner of the process, the arguments with which the process was launched for 
execution, the group owner of this process, etc.

![image](https://user-images.githubusercontent.com/109180406/179424909-35ed4c07-dedb-478d-bd54-b514a3b54174.png)

6. How to define kernel processes and user processes?

User-space processes have its own virtual address space.
Kernel processes or threads do not have their own address space, they operate within kernel address space only. And they may be started before the kernel has started any user process

7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. 
What condition are they in, or can they be arriving in?

![Screenshot_42](https://user-images.githubusercontent.com/109180406/179423333-ff28ef94-3040-4bef-9871-db705b4ad48d.png)

![Screenshot_43](https://user-images.githubusercontent.com/109180406/179423335-0369680d-0212-4127-abbf-2162502e60b8.png)

PROCESS STATE CODES
       Here are the different values that the s, stat and state output specifiers (header "STAT" or "S") will display to describe the state of a process:
       D    uninterruptible sleep (usually IO)
       R    running or runnable (on run queue)
       S    interruptible sleep (waiting for an event to complete)
       T    stopped, either by a job control signal or because it is being traced.
       W    paging (not valid since the 2.6.xx kernel)
       X    dead (should never be seen)
       Z    defunct ("zombie") process, terminated but not reaped by its parent.

       For BSD formats and when the stat keyword is used, additional characters may be displayed:
       <    high-priority (not nice to other users)
       N    low-priority (nice to other users)
       L    has pages locked into memory (for real-time and custom IO)
       s    is a session leader
       l    is multi-threaded (using CLONE_THREAD, like NPTL pthreads do)
       +    is in the foreground process group.

From the screenshots, you can see that almost all of my processes are in the S (interruptible sleep) state and only one process is in the R (running or ready to run (run queue) state).

8. Display only the processes of a specific user.

![Screenshot_39](https://user-images.githubusercontent.com/109180406/179421248-85398bab-b900-416a-b1c4-cc23327f360b.png)

9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps 
command)?

We can see every process on the system with the ps -e command. In addition, there is the ps axjf command, which is used to print the process tree. To get security information we can use ps axZ and to get information about threads we can use ps axms.

10. What information does top command display?

top command is used to show the Linux processes. It provides a dynamic real-time view of the running system. Usually, this command shows the summary information of the system and the list of processes or threads which are currently managed by the Linux Kernel.

11. Display the processes of the specific user using the top command.

`top -u username`

12. What interactive commands can be used to control the top command? Give a couple of 
examples.

- Enter or Space

Refresh-Display
These commands awaken top, and following receipt of any input, the entire display is repainted. They also force an update of any hotplugged cpu or physical memory changes.
Use either of these keys if you have a large delay interval and want to see current status.
  
- ? or h

Help
There are two help levels available. The first provides a reminder of all the basic interactive commands. If top is secured, that screen is abbreviated.
Typing 'h' or '?' on that help screen takes you to help for those interactive commands applicable to alternate-display mode.

- A

Alternate-Display-Mode toggle
This command switches between full-screen mode and alternate-display mode.
  
13. Sort the contents of the processes window using various parameters (for example, the 
amount of processor time taken up, etc.)

![Screenshot_40](https://user-images.githubusercontent.com/109180406/179422445-cd57fc0b-3959-46ab-a6b2-19ad37828774.png)

![image](https://user-images.githubusercontent.com/109180406/179425122-ef026faa-58a9-417f-91af-74d1e68dfbdd.png)

14. Concept of priority, what commands are used to set priority?

You can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority. Renice command will modify the scheduling priority of a running process. Linux Kernel schedules the process and allocates CPU time accordingly for each of them.

15. Can I change the priority of a process using the top command? If so, how?

You can use the r command from the top utility to change the priority of a currently running process

16. Examine the kill command. How to send with the kill command
process control signal? Give an example of commonly used signals.

kill command sends a signal to a process which terminates the process. If the user doesn’t specify any signal which is to be sent along with kill command then default TERM signal is sent that terminates the process.

We can send the kill command process control signal using this commands:
- kill -s signalName PID
- kill -signalName PID
- kill -signalNumber PID

Commonly used signals:
- SIGINT
- SIGKILL
- SIGTERM	
- SIGTSTP

17. Commands jobs, fg, bg, nohup. What are they for? Use the sleep, yes command to 
demonstrate the process control mechanism with fg, bg.

- bg - put suspended process into background
- fg - bring process into foreground
- jobs - list processes
- nohup (No Hang Up) is a command in Linux systems that runs the process even after logging out from the shell/terminal.

![Screenshot_41](https://user-images.githubusercontent.com/109180406/179422667-6f704023-5e65-4f28-9710-472034f535f2.png)

## Part 2
1. Check the implementability of the most frequently used OPENSSH commands in the MS 
Windows operating system. (Description of the expected result of the commands + 
screenshots: command – result should be presented)

![image](https://user-images.githubusercontent.com/109180406/179424637-9f1162ab-db77-49a0-aa4f-c112136da665.png)

![image](https://user-images.githubusercontent.com/109180406/179424628-e69c9b63-4054-40e7-81ae-1865ca0477b5.png)

2. Implement basic SSH settings to increase the security of the client-server connection (at least 
3. List the options for choosing keys for encryption in SSH. Implement 3 of them.

RSA, DSA, ECDSA, and EdDSA

4. Implement port forwarding for the SSH client from the host machine to the guest Linux 
virtual machine behind NAT.

![image](https://user-images.githubusercontent.com/109180406/179423644-0873842d-b4e6-4c95-8a57-32cb539404bc.png)

5. Intercept (capture) traffic (tcpdump, wireshark) while authorizing the remote client on the 
server using ssh, telnet, rlogin. Analyze the result
