

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

## 2 – HARDWARE INFORMATION

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
