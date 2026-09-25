
## Belangrijk
Komt erg veel voor tijdens het werken met [[containers]]

'[[id]]' toont je user ID nummer, en je primary group ID.
Je hebt Users en Groups. En users zijn leden van groups.
Als je meerdere users managed, kun je die vanuit 1 group rechten oid verlenen.
Groups bestaan om permissions, makkelijker te managen.

'[[groups]]' toont in welke groups je zit



gebleven op minuut 14:37. stukje terugspoelen. 
sudo adduser testuser

ww; wachtwoord / of / password

**pim@prodesk01**:**~**$ sudo adduser testuser
[sudo: authenticate] Password:          
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for testuser
Enter the new value, or press ENTER for the default
Full Name []: greetje aardappel
Room Number []: 67
Work Phone []: 06
Home Phone []: 050
Other []: 
Is the information correct? [Y/n] Y
**pim@prodesk01**:**~**$

'cat /etc/passwd' laat alle users zien met ID's en groups.

## User verwijderen

**pim@prodesk01**:**~**$ pwd
/home/pim
**pim@prodesk01**:**~**$ cd ..
**pim@prodesk01**:**/home**$ ls
**pim**  **testuser**
**pim@prodesk01**:**/home**$ sudo deluser testuser
[sudo: authenticate] Password:          
**pim@prodesk01**:**/home**$ ls
**pim**  **testuser**
**pim@prodesk01**:**/home**$ rm -r testuser/
rm: cannot remove 'testuser/': Permission denied
**pim@prodesk01**:**/home**$ sudo !!
sudo rm -r testuser/
**pim@prodesk01**:**/home**$ ls
**pim**
**pim@prodesk01**:**/home**$

## [[File Permissions]]

```
- rw- r-- r--  1  root  root  1842  Dec 10 14:30  /etc/passwd
│├──┤├──┤├──┤ │  │     │     │         │           │
│ │   │   │   │  │     │     │         │           └── Filename
│ │   │   │   │  │     │     │         └── Modification date
│ │   │   │   │  │     │     └── Size in bytes
│ │   │   │   │  │     └── Group owner
│ │   │   │   │  └── User owner
│ │   │   │   └── Number of hard links
│ │   │   └── Others permissions
│ │   └── Group permissions
│ └── Owner permissions
└── File type (- = file, d = directory, l = link)
```
 Voorbeelden
```
-rw-r--r--   Regular file, owner can read/write, others can only read
-rwxr-xr-x   Executable, owner full access, others can read/execute
drwxr-xr-x   Directory, owner full access, others can read/enter
-rw-------   File only owner can read/write (private)
```

## **Changing Permissions: [[chmod]]**

```
chmod u+x script.sh    # Add execute for user (owner)
chmod g+w file.txt     # Add write for group
chmod o-r file.txt     # Remove read for others
chmod a+r file.txt     # Add read for all (a = all)
chmod u+rwx file.txt   # Add read, write, execute for user

Symbols:
u = user (owner)
g = group
o = others
a = all
+ = add permission
- = remove permission
= = set exactly

Each permission has a value:
r = 4   
w = 2   
x = 1
Dit telt uniek bij elkaar op, tot 7 om alle combinaties te krijgen

Voorbeelden
chmod 755 script.sh    # rwxr-xr-x (executable by all)
chmod 644 file.txt     # rw-r--r-- (readable by all)
chmod 600 secret.txt   # rw------- (private file)
chmod 700 private_dir  # rwx------ (private directory)
```

### **Changing Ownership: [[chown]]**

```
sudo chown newowner file.txt
sudo chown newowner:newgroup file.txt.   # Change owner and group
sudo chgrp newgroup file.txt             # change just the group
sudo chown -R user;group directory       # recursive (for directories)

```

