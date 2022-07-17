# TASK5.3
## Part1
1. How many states could has a process in Linux?

There are five Linux process states. They are as follows: running & runnable, interruptable_sleep, uninterruptable_sleep, stopped, and zombie.

2. Examine the pstree command. Make output (highlight) the chain (ancestors) of the current 
process.

pstree -h

Highlights the current process and its ancestors.

3. What is a proc file system?

Proc file system (procfs) is virtual file system created on fly when system boots and is dissolved at time of system shut down.
It contains useful information about the processes that are currently running, it is regarded as control and information center for kernel.
The proc file system also provides communication medium between kernel space and user space.

4. Print information about the processor (its type, supported technologies, etc.).

cat /proc/cpuinfo

5. Use the ps command to get information about the process. The information should be as 
follows: the owner of the process, the arguments with which the process was launched for 
execution, the group owner of this process, etc.
6. How to define kernel processes and user processes?

User-space processes have its own virtual address space.
Kernel processes or threads do not have their own address space, they operate within kernel address space only. And they may be started before the kernel has started any user process

7. Print the list of processes to the terminal. Briefly describe the statuses of the processes. 
What condition are they in, or can they be arriving in?
8. Display only the processes of a specific user.

![Screenshot_39](https://user-images.githubusercontent.com/109180406/179421248-85398bab-b900-416a-b1c4-cc23327f360b.png)

9. What utilities can be used to analyze existing running tasks (by analyzing the help for the ps 
command)?

We can see every process on the system with the ps -e command. In addition, there is the ps axjf command, which is used to print the process tree. To get security information we can use ps axZ and to get information about threads we can use ps axms.

10. What information does top command display?

top command is used to show the Linux processes. It provides a dynamic real-time view of the running system. Usually, this command shows the summary information of the system and the list of processes or threads which are currently managed by the Linux Kernel.

11. Display the processes of the specific user using the top command.

top -u username

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
14. Concept of priority, what commands are used to set priority?

You can change the process priority using nice and renice utility. Nice command will launch a process with an user defined scheduling priority. Renice command will modify the scheduling priority of a running process. Linux Kernel schedules the process and allocates CPU time accordingly for each of them.

15. Can I change the priority of a process using the top command? If so, how?
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

bg - put suspended process into background
fg - bring process into foreground
jobs - list processes
nohup (No Hang Up) is a command in Linux systems that runs the process even after logging out from the shell/terminal.

## Part2
1. Check the implementability of the most frequently used OPENSSH commands in the MS 
Windows operating system. (Description of the expected result of the commands + 
screenshots: command – result should be presented)
2. Implement basic SSH settings to increase the security of the client-server connection (at least 
3. List the options for choosing keys for encryption in SSH. Implement 3 of them.
4. Implement port forwarding for the SSH client from the host machine to the guest Linux 
virtual machine behind NAT.
5*. Intercept (capture) traffic (tcpdump, wireshark) while authorizing the remote client on the 
server using ssh, telnet, rlogin. Analyze the result
