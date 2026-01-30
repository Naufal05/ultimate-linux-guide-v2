# User Management in Linux

## Introduction to User Management in Linux

Linux is a multi-user operating system, meaning multiple users can operate on a system simultaneously. Proper user management ensures security, controlled access, and system integrity.

Key files involved in user management:

- `/etc/passwd` – Stores user account details.
- `/etc/shadow` – Stores encrypted user passwords.
- `/etc/group` – Stores group information.
- `/etc/gshadow` – Stores secure group details.

## Creating Users in Linux

To create a new user in Linux, use:

### `useradd` Command (For most Linux distributions)

```bash
useradd username
```

This creates a user without a home directory.

To create a user with a home directory:

```bash
useradd -m username
```

To specify a shell:

```bash
useradd -s /bin/bash username
```

### `adduser` Command (For Debian-based systems)

```bash
adduser username
```

This is an interactive command that asks for a password and additional details.

## Managing User Passwords

To set or change a user’s password:

```bash
passwd username
```

### Enforcing Password Policies

- **Password expiration**: Set password expiry days
  ```bash
  chage -M 90 username
  ```
- **Lock a user account**
  ```bash
  passwd -l username
  ```
- **Unlock a user account**
  ```bash
  passwd -u username
  ```

## Modifying Users

Modify an existing user with `usermod`:

- Change the username:
  ```bash
  usermod -l new_username old_username
  ```
- Change the home directory:
  ```bash
  usermod -d /new/home/directory -m username
  ```
- Change the default shell:
  ```bash
  usermod -s /bin/zsh username
  ```

## Deleting Users

To remove a user but keep their home directory:

```bash
userdel username
```

To remove a user and their home directory:

```bash
userdel -r username
```

## Working with Groups

### Creating Groups

```bash
groupadd groupname
```

### Adding Users to Groups

```bash
usermod -aG groupname username
```

### Viewing Group Memberships

```bash
groups username
```

### Changing Primary Group

```bash
usermod -g new_primary_group username
```

## Sudo Access and Privilege Escalation

### Adding a User to Sudo Group

On Debian-based systems:

```bash
usermod -aG sudo username
```

On RHEL-based systems:

```bash
usermod -aG wheel username
```

### Granting Specific Commands with Sudo

Edit the sudoers file:

```bash
visudo
```

Then add:

```bash
username ALL=(ALL) NOPASSWD: /path/to/command
```

# Extra notes

//------------- USER MANAGEMENT ----------------//

1. How to create users ?

- useradd mnaufalmz

vim /etc/passwd // has all the user information

cat- to directly print the content of the file in your terminal

2. create password
   -sudo passwd mnihal

- cat /etc/shadow // has the encrypted password to view the password

decryption of the password is not possible, if somebody forgets the password after 1month,
there is no way to restore it.

3. Delete user from the organisation

userdel mnihal

Note : using useradd - there is no folder for the user in the home dir (ls /home).

For that use - adduser

to switch user:

- sudo su - mnihal
-     whoami

if you switch the root user to mnihal user, then try delete sbin folder (rm -rf /sbin)
then the user wont be able to delte any file, as bydefault they will not have permission like the the **root user**

1. Difference between userradd nd adduser
   - useradd - is very useful when you are writing scripts, because adduser is interactive, when script are used to automate we use useradd, which creates a user (no interactive way)

2. Restore the password of a Linux user -> No

//-------GROUPS-------//

1. create a group

- groupadd devops
- cat /etc/group -> create a root group

2. add user to the group

- usermod -aG devops mnihal

- ssh -> on the Linux server there is sshd, this process allow you to login to the Linux server.
  install ssh client -> has a package called ssh

-ssh mnihal@<ip-adress>

![Aws-screeshot-1](images/aws-screeshot-1)
