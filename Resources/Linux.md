# Linux commands

### apropos

```
## What to do when you don`t remember the   command  ##

apropos zip     # What are the commands that relates with zip
```

### User basics

```
useradd         # Add new user
passwd          # Reset user password
whoami          # Find oud who you are
users, who, w   # Find oud who is logged in
history         # Last executed commands
last            # who logged into system and when it has been logged in
usermod -aG groupname usernasme # Add user to the group
```

### File creation

```
touch  <filenaeme>      # Create a file
cat <filenaeme>
nano / vi <filenaeme>
```

### File Viewing

```
cat 
less
more            # Display page by page
tail            # Display last few lines
head            # Display first few lines
wc <filename>   # See how many lines theres in the file
```

### Listing Directories 

```
ls -l / ll  # Lists the contents of the current directory
ls -a       # Listing of hidden files and directories 
ls -R       # recourses through th subdirectory it encounters
ls --help   # For help
```

### Changing permissions- [documentation](https://www.pluralsight.com/blog/it-ops/linux-file-permissions)


```
chmod [mode] filenaeme
chmod [mode] -R 
```

### Change file ownership - [Documentation](https://www.geeksforgeeks.org/chown-command-in-linux-with-examples/)


```
chown [OPTION]… [OWNER][:[GROUP]] FILE…
chown [OPTION]… –reference=RFILE FILE…

```

### Files-Directories-movements


```
mv
rm
```

### Checking-Free-Space 


```
df    # Reports filesyste, disk space usage
du -h # Displays filesystem information in human readable format
```

### files Compression


```
tar -cvf filename.tar filename  # Creates tar file from a file
tar -xvf filename.tar           # uncompress a tar file
```

