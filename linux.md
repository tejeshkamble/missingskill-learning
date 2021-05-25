# **LINUX**

### HISTORY

Bell-lab first introduce BSD(unix based os). Richard stallman first introudces free software foundation in 1985. It is godfather of free software.'firstly he introduce GNU. In 1990 Linus created own kernel for free and after that Richard and Linus created GNU-Linux OS.

### What is LINUX?
- Just like Windows, iOS, and Mac OS, Linux is an operating system. 
- In fact, one of the most popular platforms on the planet, Android, is powered by the Linux operating system.
- An operating system is software that manages all of the hardware resources associated with your desktop or laptop.
- To put it simply, the operating system manages the communication between your software and your hardware. Without the operating system (OS), the software wouldnt function.

### COMMANDS

- **ls**  -  list of all files and folders
	- ls -l = files with details
	- -rw = file
	- drw = directory
	- -h = human readable
	- -t = displays in ascending order and time
	- -r = reverse the order
	- -F = add '/' to the directory at 	last
	- ls --help = all the flags which are available in linux or we can write as 'ls -lhtrf'


- **cd** - change directory
	- cd<name> = enter to the 	directory
	- cd  = take back to users home
	- cd - = take to pevious 	folder
	- cd .. = one folder back
	- cd ~` = take to home folder
	- cd ../<name> = take to one step back and enter into <name>
	- cd /<name> = take to that folder
	- cd /<name1>/<name2> = directory inside directory

- **cp** -  copy file from location to another
    - Example. cp <source> <destination>
    - cp <source>../<destination>
	- cp<s1><s2><s3><d>= to copy multiple files
	 
	
- **mv(move)** - like cut and paste
    - Example. mv <current file> <destination>
	- mv <old name> <new name> = used to change name
	- mv <name1> ../<name2> = move and rename file

- **rm** -  remove the file and folder permanently
	- rm* -  delete all files and folder from same folder
	- rm -rf(recursive and forcefully) <directory> -  remove all file and folder from same 
	- rm -rf* - remove all files from main folder	directory
	- rm -rf <directory>/* - delete all files from same directory
	
- **pwd** - shows the current/print/present working directory
- **history** - shows all previous used commands in one list
- **cat** -  opening a file, and read and write into file.
	- cat>(name of file) - first time writing something
 	- cat>>(name of file) - to update file for next time
		- ***Risks*** - if name of file are same it will be overriden		
- **less <name>** - o/p in pagewise(gives more data)
	- spacebar - next page
	- ws - previous page
	- q - quit
- **more <name>** - (gives less data)
- **echo** - to print terminal input/parameter
	- echo $path - shows the system path 
- **top** - gives all the system level information current load of system
- **ps** -shows all the apps run in system
- **touch** - to create new file
- **ping** - to check connectivity of internet and speed
- **ifconfig** - shows ip
- **ssh(login user , ip)** - access the remote server
- **mkdir** - to create directory
	- mkdir ~ {name1,name2,name3} - to create multiple directory at a time
- **exit** - exit from terminal
- **whoami** - current login user
- **wh** - list of login users
- **rmdir** - remove only empty directory
- **which** - location of installed software
   - which node - gives location of node.
- **wget** - takes data from browser and save into json file.
- **man** - manual of commands
    - -a -  shows all folders/files and hidden folders/files also 
- **clear** -  clear the terminal(ctrl L)

- **ipinfo.io** - shows ip address of pc

### FILE SYSTEM OF LINUX

**start with root(/) file**

- **/boot** - where system kernel is located
- **/bin** - all usable app are stored or binary files are stored and commands are stored here
- **/home** - all users data are stored
- **/var** - system level varibles file
- **/root** - admin users and denoted by("#")
	- ***Note*** - we differentiate normal user and admin user by $ and #

- **/usr** - user system resource
- **/tmp** - temporary files are stored
- **/etc** - system configuration (extension for files .config)
- **/lib** - system libraries are stored here
- **/mnt /media** - use as the temporary mount points for mounting storage devices, such as CDROMs, floppy disks and USB (universal serial bus) key drives.
- **/opt** - user related softwares are stored
- **/proc** - system level configuration  
- **/dev** - external devices get mounted
- **/sbin** - system level third party commands are stored here