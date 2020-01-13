Basic Linux/Unix Shell

Linux (and other Unix like OSes), have “shells” or programs which present
a command line interface to users to type commands in. In this assignment
you need to use standard C libraries, including Linux system calls such as
fork(),exec() family system calls and wait() family of system calls.
There are two kinds of commands – “Internal” and “External”. Internal
commands are those which are interpreted by the shell program itself, without requiring a different program to handle the expected operations (of the
said command). Examples of internal commands are like ‘cd’, ‘pwd’, ‘exit’
etc. External commands on the other hand relate to commands which are not
handled directly by the shell program but by an external program. Common
examples include ‘ls’, ‘cat’, ‘grep’ etc.

Your task is to design your a simple shell that can handle five, internal commands – ‘cd’, ‘echo’, ‘history’, ‘pwd’ and ‘exit’. These commands
would be handled directly by the shell. Your shell should also be able to handle five external commands – ‘ls’, ‘cat’, ‘date’, ‘rm’ and ‘mkdir’. For
these external commands you need to write individual programs to handle these
commands. To handle these external commands, the shell should typically create a new process, using the fork() system call and within each process you
need to use the execl() family system call to run the individual program. The
parent program must also wait for the child program to terminate using the
wait() family of system calls.

For each of these commands, you need not handle all the command line
options. Two options per command is sufficient. You need to document which
two options you are handling and need to demonstrate correct functioning of
the command with respect to (atleast) your chosen options. You also need to
handle corner cases such as invalid options (graceful degradation).


What To Submit
• The C program sources.
• Makefile to compile the source and generate the running binary for the
shell.
• Write-up describing the system, the options the shell commands can take,
the errors you handled and the assumptions you made. Also provide test
cases to test the functioning of the shell.


Grading Rubric
• Successful compilation using Makefile – 5 points.
• Use of system calls like – fork(), execl() family of system calls, wait()
family of system calls to handle external commands – 10 points.
• Correct handling of commands (two options per command, as described
earlier) – 20 points.
• Successfully handling atleast two corner cases for each of the commands
– 20 points (List the bugs/errors/attacks that you defend against).
• Description of the systems, commands to execute and test the program
and the assumptions that you made – 5 points
