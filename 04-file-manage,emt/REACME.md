# File management in Linux

### File and Directory Management

1. **`ls`** – Lists files and directories in the current location.
2. **`cd /path/to/directory`** – Changes the working directory.
3. **`pwd`** – Prints the current working directory.
4. **`mkdir new_folder`** – Creates a new directory.
5. **`rmdir empty_folder`** – Removes an empty directory.
6. **`rm file.txt`** – Deletes a file.
7. **`rm -r folder`** – Deletes a folder and its contents.
8. **`cp file1.txt file2.txt`** – Copies a file.
9. **`cp -r dir1 dir2`** – Copies a directory recursively.
10. **`mv old_name new_name`** – Moves or renames a file or directory.

### File Viewing and Editing

11. **`cat file.txt`** – Displays file content.
12. **`tac file.txt`** – Displays file content in reverse order.
13. **`less file.txt`** – Opens a file for viewing with scrolling support.
14. **`more file.txt`** – Similar to `less`, but only moves forward.
15. **`head -n 10 file.txt`** – Displays the first 10 lines of a file.
16. **`tail -n 10 file.txt`** – Displays the last 10 lines of a file.
17. **`nano file.txt`** – Opens a simple text editor.
18. **`vi file.txt`** – Opens a powerful text editor.
19. **`echo 'Hello' > file.txt`** – Writes text to a file, overwriting existing content.
20. **`echo 'Hello' >> file.txt`** – Appends text to a file without overwriting.

# Additional notes

//------ File viewing and Editing---------//
Vim is a wrapper on top of vi

- which vim
- less
- tail -20 demo-file.txt
- head -20 demo-file.txt
  echo
  >     -> replace
  >
  > >     -> append

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

-
-
-
