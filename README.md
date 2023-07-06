

# Essentials Linux Commands Cheat Sheet


# 1 – SYSTEM INFORMATION


### Display Linux system information

```sh
uname -a
```

### Display kernel release information

```sh
uname -r
```

### Show which version of redhat installed

```sh
cat /etc/redhat-release
```

### Show how long the system has been running + load

```sh
uptime
```

### Show system host name

```sh
hostname
```

### Display the IP addresses of the host

```sh
hostname -I
```
### Show system reboot history

```sh
last reboot
```
### Show the current date and time

```sh
date
```

### Show this month's calendar

```sh
cal
```
### Display who is online

```sh
w
```

### Who you are logged in as

```sh
whoami
```

# 2 – HARDWARE INFORMATION


### Display messages in kernel ring buffer

 ```sh
dmesg
  ```

### Display CPU information
  ```sh
cat /proc/cpuinfo
  ```

### Display memory information
  ```sh
cat /proc/meminfo
  ```

### Display free and used memory ( -h for human readable, -m for MB, -g for GB.)
  ```sh
free -h
  ```

### Display PCI devices
  ```sh
lspci -tv
  ```

### Display USB devices
  ```sh
lsusb -tv
  ```

### Display DMI/SMBIOS (hardware info) from the BIOS
  ```sh
dmidecode
  ```

### Show info about disk sda
  ```sh
hdparm -i /dev/sda
  ```

### Perform a read speed test on disk sda
  ```sh
hdparm -tT /dev/sda
  ```

### Test for unreadable blocks on disk sda
  ```sh
badblocks -s /dev/sda
  ```

# 3 – PERFORMANCE MONITORING AND STATISTICS

### Display and manage the top processes
  ```sh
top
  ```

### Interactive process viewer (top alternative)
  ```sh
htop
  ```

### Display processor related statistics
  ```sh
mpstat 1
  ```

### Display virtual memory statistics
  ```sh
vmstat 1
  ```

### Display I/O statistics
  ```sh
iostat 1
  ```

### Display the last 100 syslog messages (Use /var/log/syslog for Debian based systems.)
  ```sh
tail 100 /var/log/messages
  ```

### Capture and display all packets on interface eth0
  ```sh
tcpdump -i eth0
  ```

### Monitor all traffic on port 80 ( HTTP )
  ```sh
tcpdump -i eth0 'port 80'
  ```

### List all open files on the system
  ```sh
lsof
  ```

### List files opened by user
  ```sh
lsof -u user
  ```

### Display free and used memory ( -h for human readable, -m for MB, -g for GB.)
  ```sh
free -h
  ```

### Execute "df -h", showing periodic updates
  ```sh
watch df -h
  ```

# 4 – USER INFORMATION AND MANAGEMENT

### Display the user and group ids of your current user.
  ```sh
id
  ```

### Display the last users who have logged onto the system.
  ```sh
last
  ```

### Show who is logged into the system.
  ```sh
who
  ```

### Show who is logged in and what they are doing.
  ```sh
w
  ```

### Create a group named "test".
  ```sh
groupadd test
  ```

### Create an account named john, with a comment of "John Smith" and create the user's home directory.
  ```sh
useradd -c "John Smith" -m john
  ```

### Delete the john account.
  ```sh
userdel john
  ```

### Add the john account to the sales group
  ```sh
usermod -aG sales john
  ```

# 5 – FILE AND DIRECTORY COMMANDS

### List all files in a long listing (detailed) format
  ```sh
ls -al
  ```

### Display the present working directory
  ```sh
pwd
  ```

### Create a directory
  ```sh
mkdir directory
  ```

### Remove (delete) file
  ```sh
rm file
  ```

### Remove the directory and its contents recursively
  ```sh
rm -r directory
  ```

### Force removal of file without prompting for confirmation
  ```sh
rm -f file
  ```

### Forcefully remove directory recursively
  ```sh
rm -rf directory
  ```

### Copy file1 to file2
  ```sh
cp file1 file2
  ```

### Copy source_directory recursively to destination. If destination exists, copy source_directory into destination, otherwise create destination with the contents of source_directory.
  ```sh
cp -r source_directory destination
  ```

### Rename or move file1 to file2. If file2 is an existing directory, move file1 into directory file2
  ```sh
mv file1 file2
  ```

### Create symbolic link to linkname
  ```sh
ln -s /path/to/file linkname
  ```

### Create an empty file or update the access and modification times of file.
  ```sh
touch file
  ```

### View the contents of file
  ```sh
cat file
  ```

### Browse through a text file
  ```sh
less file
  ```

### Display the first 10 lines of file
  ```sh
head file
  ```

### Display the last 10 lines of file
  ```sh
tail file
  ```

### Display the last 10 lines of file and "follow" the file as it grows.
  ```sh
tail -f file
  ```

# 6 – PROCESS MANAGEMENT

### Display your currently running processes
  ```sh
ps
  ```

### Display all the currently running processes on the system.
  ```sh
ps -ef
  ```

### Display process information for processname
  ```sh
ps -ef | grep processname
  ```

### Display and manage the top processes
  ```sh
top
  ```

### Interactive process viewer (top alternative)
  ```sh
htop
  ```

### Kill process with process ID of pid
  ```sh
kill pid
  ```

### Kill all processes named processname
  ```sh
killall processname
  ```

### Start program in the background
  ```sh
program &
  ```

### Display stopped or background jobs
  ```sh
bg
  ```

### Brings the most recent background job to foreground
  ```sh
fg
  ```

### Brings job n to the foreground
  ```sh
fg n
  ```
