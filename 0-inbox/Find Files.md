
## Waarom relevant?
Je gebruikt het heel veel. echt heel belangrijk dat je dit command beheerst

Kan met commando find. maar ook met locate

## [[Find]]
Find files by name
'find /home -name "ASTERIST.txt"' asterist is een wildcard. zoekt naar alles voor de punt.   Zoekt dus naar een file met de naam 'alleswatjekanvinden'.txt
'find . -name config' zoekt naar het bestand config, startend vanaf de huidige directory

Find files by type
find /var -type d -name "log" zoekt naar Type d (directory) met de naam log

Find files by size
'find /var/log -size +10M' zoekt naar bestanden groter dan 10megabytes

## [[Locate]]
Is een sneller commando, want het gebruikt een database. Maar deze database kan wel outdated zijn.
'locate find' laat alle bestanden met find zien.
'touch pim.txt', hierna 'locate pim.txt' laat niets zien. 'sudo updatedb' en daarna 'locate pim.txt' zoekt in de herziene db, en kan het dan wel vinden

pim@hpprodesk02:~$ touch pim.txt
pim@hpprodesk02:~$ locate pim.txt
pim@hpprodesk02:~$ sudo updatedb
pim@hpprodesk02:~$ locate pim.txt
/home/pim/pim.txt
pim@hpprodesk02:~$ 

## [[which]] 
find command location
pim@hpprodesk02:~$ which ls
/usr/bin/ls

## [[command]]
pim@hpprodesk02:~$ command -v mkdir
/usr/bin/mkdir
pim@hpprodesk02:~$ 

Is vergelijkbaar met 'which' maar is meer betrouwbaar. 
Is beschikbaar in MEER systemen. de standaard in [[posix]] en het werkt in [[scripts]] en 'which' werkt daar soms niet.
Enige mits, het is iets meer/langer om te typen.

pim@hpprodesk02:~$ command -v cd
cd
pim@hpprodesk02:~$ 
Geen directory. gek he? Het is een built-in van de Shell.

pim@hpprodesk02:~$ type cd
cd is a shell builtin
pim@hpprodesk02:~$ 

## [[type]]
'type' zegt of iets een alias, builtin of extern commando is. Het geeft meer informatie dan 'which'.

## [[man]]
'man ls', geeft je de manual van een commando. 
exit uit het bestand met: q
Gebruik geen internetsearch. Probeer eerst de man-pages te lezen. Als je hierin goed kan navigeren, is het een key-skill om vanuit de CLI dit kan leren.

pijltjes omhoog/omlaag scrol je per regel
spatie, bladert een hele pagina
'/woordje' zoekt naar 'woordje' in de manual. '/prese' laat alles met 'prese' dus zien

man pages zijn gemaakt in genummerde sectie
1 user commands
2 system calls (kernal functions)
3 library functions
4 device files
5 file formats
6 games
7 miscellaneous
8 system admin commands
'man 5 password'

pim@hpprodesk02:~$ man -k mkdir
gnumkdir (1)         - make directories
mkdir (1)            - Create the given DIRECTORY(ies) if they do not exist
mkdir (2)            - create a directory
mkdirat (2)          - create a directory
rust-mkdir (1)       - Create the given DIRECTORY(ies) if they do not exist
pim@hpprodesk02:~$ man -k systemctl
deb-systemd-helper (1p) - subset of systemctl for machines not running systemd
deb-systemd-invoke (1p) - wrapper around systemctl, respecting policy-rc.d
systemctl (1)        - Control the systemd system and service manager
pim@hpprodesk02:~$ 

## [[help]]
pim@hpprodesk02:~$ type cd
cd is a shell builtin
pim@hpprodesk02:~$ help cd
cd: cd [-L|[-P [-e]]] [-@] [dir]
    Change the shell working directory.
etc etc...

Omdat cd een builtin is, krijg je met 'help' wel info/manual erover.

## [[--help]]
Bijna alle commando's hebben de '--help' flag. daarma kan je ook uitleg krijgen.

## links:


202609231045
