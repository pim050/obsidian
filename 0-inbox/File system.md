
## Waarom relevant?
Goed om te weten waar alles staat.

## links:

[[Paths]] Absolute vs Relative
Absolute start van root '/'
Relative start vanaf je huidige positie 'documents/file.txt' als je in /home/username bent

pwd = waar ben ik. Print Working Directory
cd = change directory. 'cd /var/log'. 
'cd .' doet niets. laat je op het zelfde niveau
'cd ..' brengt je 1 niveau terug in de tree
'cd -' de '-' brengt je naar de vorige folder waar je vandaan kwam.

'ls' = basic listing van alles files op je huidige plek
'ls -l' = langer format, met meer details (lees/schrijf rechten) en (eigenaar) 
'ls -a' toont hidden files
'ls -la' toont alle files, gewone en hidden.

-rw-r-----  1 root              adm                  121 Sep 21 06:09 apport.log.3.gz
drwxr-xr-x  2 root          root               4096 Sep 22 21:11 apt
Het eerste character geeft aan wat het is
'-' gewone file
'd' directory
'l' symbolic link

'ls -lah' maakt het wat meer leesbaar voor een human gebruiker

'tree' laat directory structuur zien
'tree -L 2' laat het twee lagen diep zien 

'mkdir' maakt een directory
'mkdir -p projects/work/2025' maakt de achterliggende folders ook aan. Zonder die flag lukt het niet.

'touch notes.txt' maakt een nieuw leeg bestand, nu genaamt notes.txt

'cp notes.txt projects/' kopieert het bestand naar je projects/ folder
'cp -r projects projects-backup' kopieert een directory naar een andere directory. de -r flag betekent recursive, en neemt alles in de folder mee naar de nieuwe.

Move en Rename
'mv notes.txt documents/' verplaatst het bestand
'mv notes.txt  memo.txt' verplaatst en hernoemd

'mv -i notes.txt documents/' als bij de bestemming al een notes.txt staat krijg je een waarschuwing van overwriten. y/n
Zonder de -i overschrijft het systeem het gewoon. Best practise is ALTIJD -i erbij te doen.-rw-r-----  1 root              adm                  121 Sep 21 06:09 apport.log.3.gz
drwxr-xr-x  2 root              root                4096 Sep 22 21:11 apt


'rm folder/bestand' haat het weg. Als er nog iets in zit faalt dit.
'rm -r documents/' haalt alles in de directory weg.
Veilige manier om directory verwijderen is...
'rmdir' is mooier voor directories te verwijderen. Je krijgt een waarschuwing als die niet leeg is.
Best practice!! Bestand eerst verwijderen. Daarna pas directory.




202609231015
