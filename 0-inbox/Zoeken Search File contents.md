
[[grep]] - grep "error" /var/log/syslog - Toont alle regels in syslog met "error"

grep -i "error" /var/log/syslog - Toont alles met Grote en kleine letters. error, Error of ERROR.

-n - toont in welke regel het is gevonden.
-v - toont alle andere regels waarin de zoekterm niet zit.
-r - toont Recursively alle bestanden in een folder met daarin de zoekterm. 'grep -r "linux" /etc/'



