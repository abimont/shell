# Shell: Processes and Signals

This project was developed as part of the Holberton School training. Each file in this directory contains the answer corresponding to an exercise of Processes and Signals project, and explores signals, how to find and kill process, what is PID, among others.

### What is a process?

A process can be thought of as an instance of a program in execution. We called this an ‘instance of a program’, because if the same program is run lets say 10 times then there will be 10 corresponding processes.

Moving ahead, each process has its own unique process ID through which it is identified in the system. Besides it own ID, a parent’s process ID is also associated with a process.

Here are some commands to take control of these processes:

ps: The ps command is a flexible tool for identifying the programs that are running on the system and the resources they are using.
pgrep: It allows a user to find process IDs in the running program in the system's current state.
pkill: It signals a program to run based on various parameters.
kill: It sends a signal (by default, the SIGTERM signal) to a running process. This default action normally stops processes.
exit: The command causes the shell or program to terminate.
trap: Trap allows you to catch signals and execute code when they occur.
