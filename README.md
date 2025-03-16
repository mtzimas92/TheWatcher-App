# TheWatcher-App
An MHServerEmu-based application that allows you to see your account and character gear/stats away from the game.

## Setup
1. Place required game files in  `Data` folder in application directory:
   ```
   Data/
   └── Game/
       ├── Calligraphy.sip
       └── mu_cdata.sip
   ```
3. Place your account database file in `Data` folder (.json or .db)
4. Configure database type in `Config.ini`:
   ```ini
   [PlayerManager]
   UseJsonDBManager=false

   [JsonDBManager]
   FileName=Player.json
   PlayerName=Player

   [SQLiteDBManager]
   FileName=your_database.db
   ```
If you are using .json file, set UseJsonDBManager to true and adjust the filename and the PlayerName

## Usage
- After you've placed the required files, open the application and wait for it to load.
- Type your email and click on load.
- Wait for your main inventory to be populated or for the dropdown menu beneath your email to show all characters.

### Character Selection
- Select character from the dropdown menu.
- Character portrait and basic info will be displayed.
- Click Stats button to view detailed analysis.

### Gear Management
- If you want to swap gear, click on the Unlock gear button.
- Click on load stash to show your full stash.
- Select the stash page you want so you can see your items.
- Drag & drop items between stash and character (gear should match the equipment slot).
- Track your swapped items by the green borders.
- Hover for detailed tooltips.
- Background colors indicate item rarity similar to the game.

### Stats Window
Shows calculations for:
- Defensive stats (EHP, Defense, Block, Dodge)
- Offensive stats (Crit/Brutal ratings, damage types)
- Infinity system bonuses
- Attribute-based bonuses
Updated every time you swap gear. You may need to reopen the stats windows for the updates to be reflected.


## Development
Built with:
- C# WPF
- SQLite/JSON database support
- MHServerEmu game data parsing

## Credits
Crypto137 for his work on MHServerEmu and some help for extracting all the properties.
AlexBond007 for the UI pictures and stats calculations from itembase.mhbugle.com.

## Bug Reports 
Please contact me in discord regarding any bugs you may find and if possible steps to reproduce the error. There is a TheWatcher-Logs.log file that is produced when you run the app but I do not track all the issues. 

## Development Help
If you want to help with the continued development of this project you are welcome to contact me with any updates you have on the included files, or ideas you have about the application.
