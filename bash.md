# Linux Bash Shell Cheat Sheet
---

## Basic Terminal Shortcuts
---

#### Clear the terminal
`CTRL L`

#### Logout
`CTRL D`

#### Go up/down the terminal
`SHIFT Page Up/Down`

#### Cursor to start of line
`CTRL A`

#### Cursor to the end of line
`CTRL E`

#### Delete left of the cursor
`CTRL U`

#### Delete right of the cursor
`CTRL K`

#### Delete word on the left
`CTRL W`

#### Paste (after CTRL U, K or W)
`CTRL Y`

#### Auto completion of file or command
`TAB`

#### Reverse search history
`CTRL R`

#### Repeat last command
`!!`

#### Stops the current command (resume with `fg` in foreground or `bg` in background)
`CTRL Z`

---

## Basic Terminal Navigation
---

#### List all files and folders
`ls -a`

#### List files in folder
`ls <folderName>`

#### Detailed list, Human readable
`ls -lh`

#### List jpeh files only
`ls -l *.jpg`

#### Result for file only
`ls -lh <fileName>`

---

#### Change directory. If `folderName` has spaces use " "
`cd <folderName>`

#### Go to root
`cd /`

#### Go up one folder
`cd ..`

---

#### Disk usage of folders, human readable
`du -h`

#### Disk usage of files and folders, Human readable
`du -ah`

#### Only show disc usage of folders
`du -sh`

---

#### Print working directory
`pwd`

---

#### Shows manual (RTFM)
`man <command>`

---

## Basic file Manipulation
---

#### Show content of file
`cat`
`less`
`more`

#### From the top
`head [-n <#oflines>] <fileName>`

#### From the bottom
`tail [-n <#oflines>] <fileName>`

---

#### Create new folder
`mkdir <folderName> [Destination]`

---

#### Copy and rename file
`cp image.jpg newimage.jpg`

#### Copy to folder
`cp image.jpg <folderName>/`

#### Copy and rename a folder
`cp -R stuff otherStuff`

#### Copy all of `*<file type>` to folder
`cp *.txt stuff/`

---

#### Move file to a folder
`mv file.txt Documents/`

#### Move `<folderName>` in `<folderName2>`
`mv <folderName> <folderName2>`

#### Rename file
`mv filename.txt filename2.txt`

#### Move `<folderName>` up in hierarchy
`mv <folderName>/ ..`

---

#### Delete file(s)
`rm <fileName>`

#### Ask for confirmation each file
`rm -i <fileName>`

#### Forde deletion of a file
`rm -f <fileName>`

#### Delete folder
`rm -r <folderName>`

---

#### Create or update a file
`touch <fileName>`

---

#### Physical link
`ln file1 file2`

#### Symbolic link
`ln -s file1 file2`

---

## Researching Files
---

### The slow method (sometimes very slow)
---

#### Search the content of all the files
`locate <text>`

#### Search for a file
`locate <fileName>`

#### Update database of files
`sudo updatedb`

---

### The fast method
---

#### Search for files who start with the word text
`find -name "<fileName>"`

#### Search for files who end with the word text
`find -name "*<fileName>"`

---

### Advanced Search
---

#### Search from file Size (in `~`)
`find ~ -size +10M`

#### Search from last access
`find -name "<filetype>" -atime -5`

#### Search only files or directory's
`find -type -f`
`find -type -d`

---

## Extract, sort and filter data
---

#### Search for text in file
`grep <someText> <fileName>`

#### Doesn't consider uppercase words
`grep -i <someText> <fileName>`

#### Exclude binary files
`grep -I <someText> <fileName>`

---

### With Regular Expressions
---

#### Search start of lines with the word `<text>`
`grep -E ^<text> <fileName>`

#### 
