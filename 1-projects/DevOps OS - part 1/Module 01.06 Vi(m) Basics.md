Why vi? 
- Vi is installed on:
- Every Linux distribution
- Every Unix system
- macOS
- Minimal Docker containers
- Embedded systems and routers

When you SSH into a server at 3 AM to fix a production issue, vi will be there. VS Code won’t be.

Verschil tussen vi en viM.
Textexitor. in viM heb je meer features.

1. Press `i` to enter Insert mode
2. Type: `Hello, this is my first vi edit.`
3. Press `Esc` to return to Normal mode
4. Type `:wq` and press Enter
You just created and saved a file.

Minimale commando's vi
1. `i` - Start typing
2. `Esc` - Stop typing
3. `:wq` - Save and quit
4. `:q!` - Quit without saving
5. `dd` - Delete a line
6. `u` - Undo

in plaats van i (insert), kan je ook de edit moet 'o' de edit openen. en onder de cursor een nieuwe regel maken

gg - ga je mee naar de top van het bestand
G - ga je mee naar de bottom

vimtutor