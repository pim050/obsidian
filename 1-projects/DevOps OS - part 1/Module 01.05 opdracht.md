## **Challenge**

**Task**: Investigate the `/etc` directory.

1. How many files and directories are in `/etc`? (hint: `ls` + `wc`)
    
2. Find all files in `/etc` that contain the word “network”
    
3. What is the largest file in `/var/log`?
    
4. How much total disk space is used on your system?
    

**Verify**: You should be able to answer all four questions using commands from this module.




1: 
pim@prodesk01:**/**$ ls -lah /etc | wc -l
203

2:
**pim@prodesk01**:**~**$ sudo grep -r "network" /etc

3: du -Ahq

**pim@prodesk01**:**~**$ ls -lahS /var/log | head -5

total 11M

-rw-r-----  1 syslog    adm             6.5M Sep 23 18:20 syslog

-rw-r-----  1 syslog    adm             2.3M Sep 20 00:24 syslog.1

-rw-r--r--  1 root      root            783K Sep 23 12:13 dpkg.log

-rw-r-----  1 syslog    adm             331K Sep 13 00:44 syslog.2.gz

4
ls -lhS /var/log