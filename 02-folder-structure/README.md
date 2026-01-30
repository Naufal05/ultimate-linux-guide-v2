# Understanding the Folder Structure

### Explanation of System Directories

### **Symbolic Links (Less Significant)**

| Directory            | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| `/sbin -> /usr/sbin` | System binaries for administrative commands (linked to `/usr/sbin`). |
| `/bin -> /usr/bin`   | Essential user binaries (linked to `/usr/bin`).                      |
| `/lib -> /usr/lib`   | Shared libraries and kernel modules (linked to `/usr/lib`).          |

### **Important System Directories**

| Directory | Description                                                              |
| --------- | ------------------------------------------------------------------------ |
| `/boot`   | Stores files needed for booting the system (not relevant in containers). |
| `/usr`    | Contains most user-installed applications and libraries.                 |
| `/var`    | Stores logs, caches, and temporary files that change frequently.         |
| `/etc`    | Stores system configuration files.                                       |

### **User & Application-Specific Directories**

| Directory | Description                                                           |
| --------- | --------------------------------------------------------------------- |
| `/home`   | Default location for user home directories.                           |
| `/opt`    | Used for installing optional third-party software.                    |
| `/srv`    | Holds data for services like web servers (rarely used in containers). |
| `/root`   | Home directory for the root user.                                     |

### **Temporary & Volatile Directories**

| Directory | Description                                             |
| --------- | ------------------------------------------------------- |
| `/tmp`    | Temporary files (cleared on reboot).                    |
| `/run`    | Holds runtime data for processes.                       |
| `/proc`   | Virtual filesystem for process and system information.  |
| `/sys`    | Virtual filesystem for hardware and kernel information. |
| `/dev`    | Contains device files (e.g., `/dev/null`, `/dev/sda`).  |

### **Mount Points**

| Directory | Description                                                     |
| --------- | --------------------------------------------------------------- |
| `/mnt`    | Temporary mount point for external filesystems.                 |
| `/media`  | Mount point for removable media (USB, CDs).                     |
| `/data`   | Likely your **mounted volume** from Windows (`C:/ubuntu-data`). |

# My notes and references

## In aws

sudo su - //
cd / // takes to the root location of the file system

---

/sbin - system binary for administraative commands
/lib - used by linux kernel
/boot - in aws,, it actually restarts linux environment - in ubuntu in windows - it is simulation
/bin - user binaries - these are non administrative
ls /usr - bin, lib and sbin are mportant within usr diretory
/srv - store any configuration info related to the servers
/opt - important folder - its a common location for all the 3rd party dependencies
/mnt - mount -> used to mount new volums or new disks
/media - adding audio or video files
/var - to store log files, or some 3rd party libraries. Mostly used to store logs. or log of we
server

/home -

there are two commands to create a user - adduser and useradd.
Note: useradd command creates user but does not create home directory.

/data - for storing any data, which needs to be shared to other people/admins in the organization.

/proc - virtual file system for processors and system information
cd /tmp - temporary files are placed here.

root - home directory of the root
run/ - stores the run-time data of the processes

/etc - similar to the C folder
cat /etc/os-release - give info about the os.

which ls - returns what is the location of ls command is.

PATH
