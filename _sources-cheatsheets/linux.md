---
title: Linux
layout: wiki
sidebar: toc
excerpt: ""
header:
  teaser: /assets/images/logos/logo_linux-tux.svg
---


## Basics

```shell
env                 # displays all environment variables

echo $SHELL         # displays the shell you're using
echo $BASH_VERSION  # displays bash version
echo $PATH          # displays the path content
echo $HOME          # displays the home directory path

bash                # if you want to use bash (type exit to go back to your previously opened shell)
whereis cmd         # locates the binary, source and manual-page for a command
which cmd           # finds out which program is executed as 'bash' (default: /bin/bash, can change across environments)

clear               # clears content on window (hide displayed lines)

shopt               # sets options for the shell

sudo -s             # login as root

exit                # logs out of current session
```


## Shortcuts

```shell
CTRL+A  # move to beginning of line
CTRL+B  # moves backward one character
CTRL+C  # halts the current command
CTRL+D  # deletes one character backward or logs out of current session, similar to exit
CTRL+E  # moves to end of line
CTRL+F  # moves forward one character
CTRL+G  # aborts the current editing command and ring the terminal bell
CTRL+H  # deletes one character under cursor (same as DELETE)
CTRL+J  # same as RETURN
CTRL+K  # deletes (kill) forward to end of line
CTRL+L  # clears screen and redisplay the line
CTRL+M  # same as RETURN
CTRL+N  # next line in command history
CTRL+O  # same as RETURN, then displays next line in history file
CTRL+P  # previous line in command history
CTRL+Q  # resumes suspended shell output
CTRL+R  # searches backward
CTRL+S  # searches forward or suspends shell output
CTRL+T  # transposes two characters
CTRL+U  # kills backward from point to the beginning of line
CTRL+V  # makes the next character typed verbatim
CTRL+W  # kills the word behind the cursor
CTRL+X  # lists the possible filename completions of the current word
CTRL+Y  # retrieves (yank) last item killed
CTRL+Z  # stops the current command, resume with fg in the foreground or bg in the background

ALT+B   # moves backward one word
ALT+D   # deletes next word
ALT+F   # moves forward one word
ALT+H   # deletes one character backward
ALT+T   # transposes two words
ALT+.   # pastes last word from the last command. Pressing it repeatedly traverses through command history.
ALT+U   # capitalizes every character from the current cursor position to the end of the word
ALT+L   # uncapitalizes every character from the current cursor position to the end of the word
ALT+C   # capitalizes the letter under the cursor. The cursor then moves to the end of the word.
ALT+R   # reverts any changes to a command you’ve pulled from your history if you’ve edited it.
ALT+?   # list possible completions to what is typed
ALT+^   # expand line to most recent match from history

CTRL+X then (        # start recording a keyboard macro
CTRL+X then )        # finish recording keyboard macro
CTRL+X then E        # recall last recorded keyboard macro
CTRL+X then CTRL+E   # invoke text editor (specified by $EDITOR) on current command line then execute resultes as shell commands

BACKSPACE  # deletes one character backward
DELETE     # deletes one character under cursor

!!       # repeats last command
!_abc_   # runs last command starting with _abc_
!_abc_:p # prints last command starting with _abc_
!$       # last argument of previous command
ALT-.    # last argument of previous command
!\*      # all arguments of previous command
^_abc_^_123_ # runs previous command, replacing _abc_ with _123_

```


## History

```shell
history   # shows command line history
!!        # repeats the last command
!<n>      # refers to command line 'n'
!<string> # refers to command starting with 'string'
!$        # refers to last argument of previous command
ALT-.     # refers to last argument of previous command
!\*       # refers to all arguments of previous command
^_abc_^_123_ # runs previous command, replacing _abc_ with _123_
```


## File Commands

```shell
ls                            # lists your files in current directory, ls <dir> to print files in a specific directory
ls -l                         # lists your files in 'long format', which contains the exact size of the file, who owns the file and who has the right to look at it, and when it was last modified
ls -a                         # lists all files in 'long format', including hidden files (name beginning with '.')
ls -R                         # lists recursively
ls -r                         # lists in reverse order
ls -t                         # lists sorting by last modified
ls -1                         # lists one file per line
ls -m                         # lists files separated by comma
ls -Q                         # lists files quoted
ln -s <filename> <link>       # creates symbolic link to file
readlink <filename>           # shows where a symbolic links points to
tree                          # show directories and subdirectories in easilly readable file tree
mc                            # terminal file explorer (alternative to ncdu)
touch <filename>              # creates or updates (edit) your file
file <filename>               # gets type of the file
mktemp -t <filename>          # make a temp file in /tmp/ which is deleted at next boot (-d to make directory)
cat <filename>                # prints file raw content (will not be interpreted)
any_command > <filename>      # '>' is used to perform redirections, it will set any_command's stdout to file instead of "real stdout" (generally /dev/stdout)
more <filename>               # shows the first part of a file (move with space and type q to quit)
head -n <nr> <filename>       # outputs the first <nr> lines (default: 10 lines) of file 
tail -n <nr> <filename>       # outputs the last <nr> lines (default: 10 lines) of file 
tail -F <filename>            # outputs the last lines of file as it changes (default: 10 lines)
more <filename>               # shows and paginate the file
less <filename>               # shows and paginate the file, being faster and more resourceful than "more"
vim <filename>                # opens a file in VIM (VI iMproved) text editor, will create it if it doesn't exist
mv <filename1> <dest>         # moves a file to destination, behavior will change based on 'dest' type (dir: file is placed into dir; file: file will replace dest (tip: useful for renaming))
cp <filename1> <dest>         # copies a file
rm <filename>                 # removes a file
diff <filename1> <filename2>  # compares files, and shows where they differ
wc <filename>                 # tells you how many lines, words and characters there are in a file. Use -lwc (lines, word, character) to ouput only 1 of those informations
sort <filename>               # sorts the contents of a text file line by line in alphabetical order, use -n for numeric sort and -r for reversing order.
sort -t -k <filename>         # sorts the contents on specific sort key field starting from 1, using the field separator t.
rev                           # reverse string characters (hello becomes olleh)
gzip <filename>               # compresses files using gzip algorithm
gunzip <filename>             # uncompresses files compressed by gzip
gzcat <filename>              # lets you look at gzipped file without actually having to gunzip it
lpr <filename>                # prints the file
lpq                           # checks out the printer queue
lprm <jobnumber>              # removes something from the printer queue
genscript                     # converts plain text files into postscript for printing and gives you some options for formatting
dvips <filename>              # prints .dvi files (i.e. files produced by LaTeX)
head -n file_name | tail +n   # Print nth line from file.
head -y lines.txt | tail +x   # want to display all the lines from x to y. This includes the xth and yth lines.
```


## Directory Commands

```shell
mkdir <dirname>               # makes a new directory
rmdir <dirname>               # remove an empty directory
rmdir -rf <dirname>           # remove a non-empty directory
mv <dir1> <dir2>              # rename a directory from <dir1> to <dir2>
cd                            # changes to home
cd ..                         # changes to the parent directory
cd <dirname>                  # changes directory
cp -r <dir1> <dir2>           # copy <dir1> into <dir2> including sub-directories
pwd                           # tells you where you currently are
cd ~                          # changes to home.
cd -                          # changes to previous working directory
ls -d */                      # lists all subfolders in the current folder
```


## Search Files and Directories

```shell
grep <pattern> <filename>     # looks for the string in the files
grep -r <pattern> <directory> # search recursively for pattern in directory
grep -i <pattern> <filename>  # searches in case insensitive mode for the string in the files
grep -v <pattern> <filename>  # searches for lines of <filename> that don't contain <pattern>
grep -o <pattern> <filename>  # shows only the part of a line matching <pattern>

find . -name <name or regex> # searches for file <name> or for files matching the <regex> expression in the current directory and all its sub-directories
find . -type <type> # searches for files (-type f) or directories (-type d) in the current directory and all its sub-directories
find . -user <user> # searches for files owned by <user>
find . -mmin <minutes> # searches for files in the current directory and all its sub-directories that were modifed less than <minutes> ago
locate _file_ # Find _file_ (quick search of system index)
```


## File and Directory Permis­sions

First digit is owner permis­sion, second is group and third is everyone.

``` shell
chmod -options MODE <filename>  # lets you change the read, write, and execute permissions of <filename> to MODE for respectively the owner, the group and everyone.
chmod 775 <filename>       # changes permissions of <filename> to 775
chmod -R 600 <foldername>  # applies chmod 600 recurs­ively chmod to <foldername>
chown <username>:<group> <filename> # Change <filename> owner to <username> and group to <group>
```

| Number | Permission Type | Symbol |
|---|---|---|
|0 | No Permission | `---` |
|1 | Execute | `--x` |
|2 | Write | `-w-` |
|3 | Execute + Write | `-wx` |
|4 | Read | `r--` |
|5 | Read + Execute | `r-x` |
|6 | Read +Write | `rw-` |
|7 | Read + Write +Execute | `rwx` |


## System Info

```shell
whoami                   # returns your username
passwd                   # lets you change your password
quota -v                 # shows what your disk quota is
date                     # shows the current date and time
cal                      # shows the month's calendar
uptime                   # shows current uptime
w                        # displays whois online
finger <user>            # displays information about user
uname -a                 # shows kernel information
head -n1 /etc/issue      # show linux distri­bution
mount                    # shows mounted filesy­stems
man <command>            # shows the manual for specified command
df                       # shows disk usage
df -h                    # shows disk usage in human readable format
du <filename>            # shows the disk usage of the files and directories in filename 
du -hs                   # shows the total disk usage of the folder in human readable format
lscpu                    # gives information about the cpu
last <yourUsername>      # lists your last logins
ps -u yourusername       # lists your processes
kill <PID>               # kills the processes with the ID you gave
killall <processname>    # kill all processes with the name
top                      # displays your currently active processes
htop                     # displays your currently active processes with nicer graphics
lsof                     # lists open files
bg                       # lists stopped or background jobs ; resume a stopped job in the background
fg                       # brings the most recent job in the foreground
fg <job>                 # brings job to the foreground
time <command>           # report time consumed by command execution
```


## SSH Commands

```shell
ssh user@host            # connects to host as user
ssh -p <port> user@host  # connects to host on specified port as user
ssh-copy-id user@host    # adds your ssh key to host for user to enable a keyed or passwordless login
```


## Netword Commands

```shell
ping <host>              # pings host and outputs results
whois <domain>           # gets whois information for domain
dig <domain>             # gets DNS information for domain
dig -x <host>            # reverses lookup host
wget <file>              # downloads file
host <server_name>       # shows the IP of server_name and vice-versa (host <ip>)
ip <server_name>         # shows the IP of server_name

scp /path/to/file user@server:/path/to/destination # Copy file from local directory to server directory
scp user@remote_host:remote_file local_file        # download file: remote -> local
scp local_file user@remote_host:remote_file        # upload file: local -> remote
```


## Command-line Processing Cycle

```shell
# The default order for command lookup is functions, followed by built-ins, with scripts and executables last.
# There are three built-ins that you can use to override this order: `command`, `builtin` and `enable`.

command  # removes alias and function lookup. Only built-ins and commands found in the search path are executed
builtin  # looks up only built-in commands, ignoring functions and commands found in PATH
enable   # enables and disables shell built-ins

eval     # takes arguments and run them through the command-line processing steps all over again
```


## Input/Output Redirectors

```shell
cmd1 | cmd2 # pipe; takes standard output of cmd1 as standard input to cmd2
cmd1 < cmd2 # takes standard output of cmd2 as file input to cmd1
< file     # takes standard input from file
> file     # directs standard output to file
>> file    # directs standard output to file; append to file if it already exists
>|file     # forces standard output to file even if noclobber is set
n>|file    # forces output to file from file descriptor n even if noclobber is set
<> file    # uses file as both standard input and standard output
n<>file    # uses file as both input and output for file descriptor n
n>file     # directs file descriptor n to file
n<file     # takes file descriptor n from file
n>>file    # directs file description n to file; append to file if it already exists
n>&        # duplicates standard output to file descriptor n
n<&        # duplicates standard input from file descriptor n
n>&m       # file descriptor n is made to be a copy of the output file descriptor
n<&m       # file descriptor n is made to be a copy of the input file descriptor
&>file     # directs standard output and standard error to file
<&-        # closes the standard input
>&-        # closes the standard output
n>&-       # closes the ouput from file descriptor n
n<&-       # closes the input from file descripor n
cmd > /dev/null      # discards stdout
cmd > /dev/null 2>&1 # discards both stdout and stderr
cmd 2> file # directs error output (stderr) of _cmd_ to _file_
cmd 1>&2    # directs stdout to same place as stderr
cmd 2>&1    # directs stderr to same place as stdout
cmd &> file # directs every output of cmd to file


|tee <file># output command to both terminal and a file (-a to append to file)
```


## Process Handling

```shell
# To suspend a job, type CTRL+Z while it is running. You can also suspend a job with CTRL+Y.
# This is slightly different from CTRL+Z in that the process is only stopped when it attempts to read input from terminal.
# Of course, to interrupt a job, type CTRL+C.

cmd1 ; cmd2  # runs cmd1 and then cmd2
cmd1 && cmd2 # runs cmd2 if cmd1 is successful
cmd1 || cmd2 # runs cmd2 if cmd1 is not successful
cmd &        # runs job in the background and prompts back the shell

jobs         # lists all jobs (use with -l to see associated PID)

fg           # brings a background job into the foreground
fg %+        # brings most recently invoked background job
fg %-        # brings second most recently invoked background job
fg %N        # brings job number N
fg %string   # brings job whose command begins with string
fg %?string  # brings job whose command contains string

kill -l               # returns a list of all signals on the system, by name and number
kill PID              # terminates process with specified PID
kill -s SIGKILL 4500  # sends a signal to force or terminate the process
kill -15 913          # ending PID 913 process with signal 15 (TERM)
kill %1               # where %1 is the number of job as read from 'jobs' command.
pkill _name_          # kills process with name _name_
killall _name_        # kills all processes with names beginning _name_

ps           # prints a line of information about the current running login shell and any processes running under it
ps -a        # selects all processes with a tty except session leaders

trap cmd sig1 sig2  # executes a command when a signal is received by the script
trap "" sig1 sig2   # ignores that signals
trap - sig1 sig2    # resets the action taken when the signal is received to the default

disown <PID|JID>    # removes the process from the list of jobs

wait                # waits until all background jobs have finished
sleep <number>      # wait # of seconds before continuing
watch -n <s> '<command>' # Issue the <command> every <s> seconds and display output
nohup sh custom-script.sh & # Lauches custom-script.sh without trapping the screen

pv                  # display progress bar for data handling commands. often used with pipe like |pv
yes                 # give yes response everytime an input is requested from script/process
```


## AWK Commands




## Profile Configuration: .bashrc





## Sources

<https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/bash.sh>{:target="_blank"}

<https://cheatography.com/davechild/cheat-sheets/linux-command-line/>{:target="_blank"}

<https://github.com/LeCoupa/awesome-cheatsheets/blob/master/tools/ubuntu.sh>{:target="_blank"}


## See Also

[Learn X in Y minutes](https://learnxinyminutes.com/docs/html/){:target="_blank"}