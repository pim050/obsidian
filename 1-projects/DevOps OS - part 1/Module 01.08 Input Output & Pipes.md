## **Questions We’ll Answer**

- What is stdin, stdout, and stderr?
- What are file descriptors (0, 1, 2)?
- How do I save command output to a file?
- How do I append to a file instead of overwriting?
- How do I feed a file into a command?
- How do I redirect error messages separately?
- What is a pipe and how does it work?
- How do I chain commands together?
- How do I sort output?
- How do I remove duplicate lines?
- How do I extract specific columns from output?
- How do I write to a file AND see output at the same time?
- What is a TTY?
- What’s the difference between interactive and non-interactive?


## Even goed opletten. [[stdin]] en [[stdout]] redirect.

Het symbool/pijltje < of > geeft aan wat input of output is en van welke kant het komt.
**Input & Output omleiding (`<` en `>`)** Het symbool (`<` of `>`) werkt als een pijl die de stroomrichting van de data aangeeft:
- **`>` (Output):** Stroomt van **links naar rechts** (`commando > bestand`). De uitvoer (stdout) van het commando gaat het bestand in.
- **`<` (Input):** Stroomt van **rechts naar links** (`commando < bestand`). De inhoud van het bestand gaat als invoer (stdin) het commando in.


Elk programma heeft 3 standaard 'streams'.
'cat' tot nu toe gebruikt om inhoud van een file te tonen.
Maar 'cat' is ook een programma, en als je alleen 'cat' runt. dan kan je daarin input geven, en daarna output verwachten.
Een input stream, gevolgd door een output stream dus.
'standard in' wordt getoond met 'standard out' of 'standard error'

Mischa: Om het makkelijker te maken, bedenk 'standard' er even niet bij. Elk commando heeft dus een input, een output, of error (wat ook een soort output is).

```
cat /etc/passwd | wc -l                                           # stdin
35                                                                # stdout
ls /nonexistent                                                   # standin 
ls: cannot access '/nonexistent': No such file or directory       # stderr
```

## Redirection

ls /etc (heeft output)
ls /etc > listing.txt ( > redirect het resultaat van een command naar een file)

'>' zet de output in een file. file.txt
'>>' (is append) voegt de output aan de onderkant van een file. file.txt

```
$ echo "line 1" > file.txt
$ cat file.txt
line 1
$ echo "line 2" >> file.txt
$ cat file.txt
line 1
line 2
$ echo "line 3" > file.txt
$ cat file.txt
line 3
```

## Redirect beide.  stdout &> stderr

```
$ ls /etc /nonexistent                                       # ls twee mappen
ls: cannot access '/nonexistent': No such file or directory  # stderr
<output voor /etc>                                           # stdout

# Door '>' te gebruiken wordt ALLEEN stdout (1) omgeleid naar het bestand.
# stderr (2) wordt niet omgeleid en verschijnt nog steeds direct op het scherm.
$ ls /etc /nonexistent > all-output.txt
ls: cannot access '/nonexistent': No such file or directory  # stderr

# Oplossing: Combineer stdout en stderr samen naar een bestand met '&>'
$ ls /etc /nonexistent &> all-output.txt

$ cat all-output.txt
# Beide streams (stdout én stderr) zitten nu samen in all-output.txt



```

```
Bash kent nummers toe aan de drie streams
0 = stdin
1 = stdout
2 = stderr
```

## Redirect beide, naar afzonderlijke files

```
ls /etc /nonexistent > stdout.txt 2> stderr.txt
```

## Discard output

```
$ ls /etc > /dev/null
# stdout gaat naar /dev/null (het 'black hole'), dus geen output

$ ls /nonexistent
ls: cannot access '/nonexistent': No such file or directory
# Dit is stderr (foutmelding)

$ ls /nonexistent > /dev/null
ls: cannot access '/nonexistent': No such file or directory
# '>' leidt alleen stdout om. stderr komt dus nog steeds op het scherm

$ ls /nonexistent 2> /dev/null
# '2>' leidt specifiek stderr om naar /dev/null. Geen zichtbare output meer!
```


## The Pipe Operator

The pipe '|' command sends stdout from one command to stdin of another command.

```
$ ls /etc | head -5
ModemManager
PackageKit
UPower
X11
adduser.conf
# this creates output in the terminal, but not a file
```
## Chaining commands
```
$ cat /etc/passwd | grep bash | wc -l

1 cat /etc/passwd reads file and sends contents to stdout #1
2 grep bash takes stdout #1 as stdin, filters lines containing 'bash', outputs to stdout #2
3 wc -l takes stdout #2 as stdin, counts lines, outputs result (2) as stdout #3 to terminal
```

## Practical examples
```
$ history | grep ssh
$ who | sort
$ w | sort
$ ls | wc -l
```

## Usefull filter Commands

 gebleven rond minuut 19:30
 