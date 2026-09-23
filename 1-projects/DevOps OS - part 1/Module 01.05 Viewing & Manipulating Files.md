ipv 'cat var/log/syslog' die een heel veel text er op knalt, gebruik dan...
'less /var/log/syslog'. Hier kan je met / weer zoeken. n of shift+n zoek je naar volgende of vorige

space of f = volgende pagina
b = vorige pagina
Pijl omhoog/omlaag = regel omhoog/laag
g = begin
G = einde
q = quit

[[head]] laat de eerste 10 regels van iets zien 'head -20 /var/log/syslog' laat de je eerste 20 zien.

[[tail]] idem als head.
'tail -f /var/log/syslog' laat de ontwikkelingen in de file in realtime zien.
Dit commando is essentieel bij [[debuggin]] 

## Searching for file content
[[grep]] "error" /var/log/syslog en filterd alle lijnen eruit waarin het woord error zit.

Opletten met Casesensitivity. Het zoekkommando met Grep is hoofdletter gevoelig. Met de flag -i is die hoofdlettergevoeligheid weg. vindt op deze manier dan ook ErRoR

grep -v "error" /var/log/syslog. laat alles met error eruit.

grep -r "password" /etc/ laat alle files zien met het woord password zien in /etc/

'grep -c "error" /var/log/syslog' Toont het aantal Counts van error
'grep -B 2 -A2 "error" /var/log/syslog' toont 2 regels Before en 2 regels After "error".

[[grep]] Kan ook naar patronen zoeken, niet alleen letterlijke tekst
'grep "^root" /etc/passwd' zoekt naar bestanden waarin de eerste lijn met root begint
'^' ook wel carrot genoemt, betekent; start met
'$' betekent 'eindigt met'

'grep "user[0-9]" /etc/passwd' zoekt naar elke user* in zijn naam, user0 user1 user2 etc.

Zoeken met 'grep "^....."' en 'grep "$.....'" is erg krachtig. start met/eindigt met.


## File information
Wat voor type file is dit
'[[file]] /var/log/syslog' 
**pim@prodesk01**:**~**$  file /var/log/syslog
/var/log/syslog: ASCII text, with very long lines (378)

Detailed informatie over een file
'[[stat]] /etc/passwd'

## Count words, lines, characters
'[[wc]] /etc/password' output is 32 54 1842 (lines/words/characters)
'wc -l /etc/password' out is 32. alleen lines
-w words

## How big is this directory
'[[du]] -sh /var/log'. DiskUsage
'[[df]] -h' shows all mounted filesystems and their space usage. -h voor Human readable format.


