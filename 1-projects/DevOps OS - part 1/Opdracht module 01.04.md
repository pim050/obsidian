
**pim@prodesk01**:**~**$ mkdir -p ~/projects/linux-course

**pim@prodesk01**:**~**$ ls

 **projects**   **'~'**

**pim@prodesk01**:**~**$ cd projects/

**pim@prodesk01**:**~/projects**$ ls

**linux-course**

**pim@prodesk01**:**~/projects**$ ls

**linux-course**

**pim@prodesk01**:**~/projects**$ cd linux-course/

**pim@prodesk01**:**~/projects/linux-course**$ ls

**pim@prodesk01**:**~/projects/linux-course**$ mkdir notes

**pim@prodesk01**:**~/projects/linux-course**$ mkdir scripts

**pim@prodesk01**:**~/projects/linux-course**$ touch readme.txt

**pim@prodesk01**:**~/projects/linux-course**$ mv readme.txt /notes

mv: cannot move 'readme.txt' to '/notes': Permission denied

**pim@prodesk01**:**~/projects/linux-course**$ mv readme.txt notes/

**pim@prodesk01**:**~/projects/linux-course**$ ls

**notes**  **scripts**

**pim@prodesk01**:**~/projects/linux-course**$ de notes

de: command not found

**pim@prodesk01**:**~/projects/linux-course**$ ls notes/

readme.txt

**pim@prodesk01**:**~/projects/linux-course**$ mv notes/readme.txt notes/module4.txt

**pim@prodesk01**:**~/projects/linux-course**$ ls notes/

module4.txt

**pim@prodesk01**:**~/projects/linux-course**$ cd ..

**pim@prodesk01**:**~/projects**$ ls

**linux-course**

**pim@prodesk01**:**~/projects**$ cd

**pim@prodesk01**:**~**$ ls

 **projects**   **'~'**

**pim@prodesk01**:**~**$ cd projects/

**pim@prodesk01**:**~/projects**$ /tree 2

-bash: /tree: No such file or directory

**pim@prodesk01**:**~/projects**$ tree -2

Command 'tree' not found, but can be installed with:

sudo apt install tree

**pim@prodesk01**:**~/projects**$ sudo apt install tree

[sudo: authenticate] Password:          

Installing:                     

  tree

  

Summary:

  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 1

  Download size: 53.5 kB

  Space needed: 125 kB / 85.9 GB available

  

Get:1 http://archive.ubuntu.com/ubuntu resolute/universe amd64 tree amd64 2.3.1-1 [53.5 kB]

Fetched 53.5 kB in 0s (140 kB/s)

Selecting previously unselected package tree.

(Reading database… 139745 files and directories currently installed.)

Preparing to unpack …/tree_2.3.1-1_amd64.deb…

Unpacking tree (2.3.1-1)…

Setting up tree (2.3.1-1)…

Processing triggers for man-db (2.13.1-1build1)…

Scanning processes...                                                                                                                                                      

Scanning processor microcode...                                                                                                                                            

Scanning linux images...                                                                                                                                                   

  

Running kernel seems to be up-to-date.

  

The processor microcode seems to be up-to-date.

  

No services need to be restarted.

  

No containers need to be restarted.

  

No user sessions are running outdated binaries.

  

No VM guests are running outdated hypervisor (qemu) binaries on this host.

**pim@prodesk01**:**~/projects**$ tree -2

tree: Invalid argument -`2'.

usage: **tree** [**-acdfghilnpqrstuvxACDFJQNSUX**] [**-L** _level_ [**-R**]] [**-H** [-]_baseHREF_]

[**-T** _title_] [**-o** _filename_] [**-P** _pattern_] [**-I** _pattern_] [**--gitignore**]

[**--gitfile**[**=**]_file_] [**--matchdirs**] [**--metafirst**] [**--ignore-case**]

[**--nolinks**] [**--hintro**[**=**]_file_] [**--houtro**[**=**]_file_] [**--inodes**] [**--device**]

[**--sort**[**=**]_name_] [**--dirsfirst**] [**--filesfirst**] [**--filelimit**[**=**]_#_] [**--si**]

[**--du**] [**--prune**] [**--charset**[**=**]_X_] [**--timefmt**[**=**]_format_] [**--fromfile**]

[**--fromtabfile**] [**--fflinks**] [**--info**] [**--infofile**[**=**]_file_] [**--noreport**]

[**--hyperlink**] [**--scheme**[**=**]_schema_] [**--authority**[**=**]_host_] [**--opt-toggle**]

[**--compress**[**=**]_#_] [**--condense**] [**--version**] [**--help**] [**--acl**] [**--selinux**]

[**--**] [_directory_ **...**]

**pim@prodesk01**:**~/projects**$ tree -L 2

**.**

└── **linux-course**

    ├── **notes**

    └── **scripts**

  

4 directories, 0 files

**pim@prodesk01**:**~/projects**$ ls notes/

ls: cannot access 'notes/': No such file or directory

**pim@prodesk01**:**~/projects**$ ls /notes

ls: cannot access '/notes': No such file or directory

**pim@prodesk01**:**~/projects**$ ls

**linux-course**

**pim@prodesk01**:**~/projects**$ cd linux-course/

**pim@prodesk01**:**~/projects/linux-course**$ ls notes/

module4.txt

**pim@prodesk01**:**~/projects/linux-course**$ rm notes/module4.txt 

**pim@prodesk01**:**~/projects/linux-course**$ cd ..

**pim@prodesk01**:**~/projects**$ rm linux-course/

rm: cannot remove 'linux-course/': Is a directory

**pim@prodesk01**:**~/projects**$ rm -r linux-course/

**pim@prodesk01**:**~/projects**$ ls -la

total 8

drwxrwxr-x 2 pim pim 4096 Sep 23 12:16 **.**

drwxr-x--- 9 pim pim 4096 Sep 23 12:10 **..**

**pim@prodesk01**:**~/projects**$ ls

**pim@prodesk01**:**~/projects**$