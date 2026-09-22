
'cat' - Inhoud van file tonen. Geschikt voor kleine bestanden. Grote bestanden zijn slecht te lezen. Alles komt te snel voorbij.

'less' - Door een text scrollen. 
KeyAction`Space` or `f`Forward one page`b`Back one page`↑` / `↓`Line by line`g`Go to beginning`G`Go to end`/pattern`Search forward`n`Next search result`q`Quit

'head' - Laat je de bovenkant van een file zien. 'head -10 /var/log/syslog', laat de eerste 10 zien.

'Tail' Idem maar dan de laatste regels van een file. 
In realtime een log bekijken 'tail -f /var/log/syslog'. ctrl-c stopt dit.
**This is essential for [[debugging]].** When something goes wrong, you `tail -f` the log file, reproduce the problem, and watch the errors appear.

