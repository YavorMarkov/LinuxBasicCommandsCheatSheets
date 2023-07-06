

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

## 4 – USER INFORMATION AND MANAGEMENT

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

