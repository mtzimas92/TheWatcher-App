# TheWatcher-App
An MHServerEmu-based application that allows you to see your account and character gear/stats away from the game.

## Setup
1. Download the latest release of The Watcher
2. Locate the required game files (found in your Marvel Heroes installation directory, in Marvel Heroes\Data\Game). Copy the two sip files in the  `Data\Game` folder in the Watcher application directory:
   ```
   Data/
   └── Game/
       ├── Calligraphy.sip
       └── mu_cdata.sip
   ```
3. Get your account database file (.json or .db)
   - To obtain the .json file, enter the game in your favorite MHServerEmu server and type !account download in the game chat.
   - To obtain the .db file, navigate to your local MHServerEmu application directory, and copy the Account.db file in the `MHServerEmu\Data` folder.
4. Copy the database file from Step 3 in the `Data` directory of the Watcher application (e.g. TheWatcher-v1.2\Data).
5. Configure the database type in `Config.ini`:
   ```ini
   [PlayerManager]
   UseJsonDBManager=false

   [JsonDBManager]
   FileName=Player.json
   PlayerName=Player

   [SQLiteDBManager]
   FileName=your_database.db
   ```
If you are using .json file, set UseJsonDBManager to true and adjust the filename and the PlayerName. The filename must match your json file (you can rename it), and the PlayerName should match your in-game character's name.

## Usage
- After you've placed the required files, open the application and wait for it to load.
- Type your email and click on load. For json database, you can type whatever you want.
- Wait for your main inventory to be populated or for the dropdown menu beneath your email to show all characters.

### Character Selection
- Select a character from the dropdown menu.
- Character portrait and basic info will be displayed.
- Click the Stats option to view detailed analysis.

### Gear Management
- If you want to swap gear, click the Unlock gear button.
- Click on load stash to show your full stash.
- Select the stash page you want so you can see your items.
- Drag & drop items between stash and character (gear should match the equipment slot).
- Track your swapped items by the green borders.
- Hover for detailed tooltips.
- Background colors indicate item rarity similar to the game.
- You can also now sort based on typically useful stats (highest first)

### Stats Window
Shows calculations for:
- Defensive stats (EHP, Defense, Block, Dodge)
- Offensive stats (Crit/Brutal ratings, damage types)
- Infinity system bonuses
- Attribute-based bonuses
- Synergy-based bonuses
Updated every time you swap gear. You may need to reopen the stats windows for the updates to be reflected.

### Character Import/Export
Save your current stats and items and share it with anyone who uses the app.

### The Holy Grail
A tracker for hardcore enthusiasts, dreaming to get every single item in the game. 

## Development
Built with:
- C# WPF
- SQLite/JSON database support
- MHServerEmu game data parsing


## Bug Reports 
Please contact me in discord regarding any bugs you may find and if possible steps to reproduce the error. There is a TheWatcher-Logs.log file that is produced when you run the app but I do not track all the issues. 

## Development Help
If you want to help with the continued development of this project you are welcome to contact me with any updates you have on the included files, or ideas you have about the application.

## Credits
- Crypto137 for his work on MHServerEmu and some help for extracting all the properties.
- AlexBond007 for the UI pictures and stats calculations from itembase.mhbugle.com.
- Jermanfu for his idea on the Holy Grail and his help testing the various features.
