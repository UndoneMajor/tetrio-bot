# Tetr.io Bot
# Tetr.io Bot with Hold Functionality

An intelligent Tetr.io bot that plays automatically with advanced hold mechanics, coordinate management, and strategic decision-making.

## 🚀 Features

- **Smart Hold System**: Automatically decides when to use hold based on piece evaluation
- **Coordinate Management**: Save/load coordinates for easy setup
- **Pause/Resume**: Pause the bot anytime during gameplay
- **Strategic AI**: Evaluates multiple move options and chooses the best one
- **Real-time Board Scanning**: Adapts to different game modes and situations
- **Easy Setup**: Simple coordinate configuration system

## 📋 Requirements

- Python 3.7+ (3.10 recommended because sigma)
  - https://www.python.org/downloads/release/python-3100/
- Required packages (install with `pip install -r requirements.txt`):
  - `keyboard`
  - `numpy`
  - `PIL` (Pillow its pillow!!!! pip install pillow NOT PIL)
  - `pyautogui`
  - `math` (built-in so not needed lmaoaoaoao)

## 🎮 Controls

### Main Controls **note that you can change all of them easily in the code just find it yh lol lmao
- **SPACE**: Start the bot
- **ESC**: Exit the bot
- **Q**: Pause/Unpause during gameplay (buggy sometiemes require you to hold sometimes not woa technologia)
- **;**: Reconfigure coordinates (in case you misclick or smth)

### Coordinate Setup (Manual Mode)
- **[-]**: Set board top-left corner
- **[=]**: Set board bottom-right corner
- **[[ ]**: Set first piece position
- **[] ]**: Set fifth piece position
- **[\ ]**: Set hold box position
- **ENTER**: Finish coordinate setup

## ⚙️ Setup Instructions (for newbs :P)

### 1. Install Dependencies
```
pip install -r requirements.txt
```

### 2. Run the Bot
```
python bet.py
```

### 3. Configure Coordinates
When you first run the bot, you'll see:
```
=== Coordinate Setup ===
1. Load coordinates from coordinates.json
2. Set coordinates manually
```

**Option 1 (Recommended)**: Load existing coordinates
- Choose `1` if you have a `coordinates.json` file
- Bot will load coordinates automatically

**Option 2**: Manual setup
- Choose `2` for manual coordinate setup
- Follow the on-screen instructions to set each coordinate
- Coordinates are automatically saved after setup to coordinates.json

### 4. Start Playing
- Press **SPACE** to start the bot
- Press **Q** to pause/unpause anytime
- Press **ESC** to exit

## 🧠 How It Works

### Hold System !!!! (WOWZA)
The bot intelligently (:P foreshadowing...) evaluates three options for each piece:
1. **Place current piece directly**
2. **Use held piece** (if available)
3. **Hold current piece and use next piece**

The bot chooses the option with the highest score, considering:
- Board state evaluation
- Piece placement efficiency
- Future piece possibilities
- Hold strategy optimization
(no ai involved in case you hate ai)
### Coordinate System
- **Board coordinates**: Define the playing field area
- **Piece coordinates**: Track the piece queue positions
- **Hold coordinates**: Monitor the hold box
- **Auto-calculation**: Intermediate piece positions are calculated automatically

### AI Strategy
The bot uses a evaluation system that considers:
- **Height management**: Prefers lower piece placements
- **Hole prevention**: Avoids creating gaps
- **Line clearing**: Prioritizes full row clears
- **Hold optimization**: Strategic use of hold feature

## 📁 File Structure

```
Tetrio-bot-main/
├── bet.py                 # Main bot script
├── TetrisBoard.py         # Board management class
├── coordinates.json       # Saved coordinates
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

## ⚡ Performance Settings

You can adjust these settings in `bet.py`:

```python
# AI Settings
calculation_accuracy = 5    # Higher = more accurate but slower (recommended: "5" because 6 7 :OOOOOO)
max_depth = 6              # Look ahead depth (max 6)
wait_time = 0.04           # its about screen refreshing so dont touch if it works why bother right lol

# Game Settings
key_delay = 0.02           # Delay between key presses
scan_board = True          # Enable board scanning
jstris = False             # Set to True for Jstris mode (who ever plays that mode bruh)
```

## 🎯 Game Modes

### Tetr.io Mode (Default)
- Optimized for Tetr.io interface
- Default colors and keybinds
- Standard coordinate ranges

### Jstris Mode
- Set `jstris = True` in the code
- Different colors and keybinds
- Adjusted coordinate ranges

## 🔧 Troubleshooting

### Common Issues !!!!!!!

**Bot not detecting pieces correctly:**
- Recalibrate coordinates using manual setup
- Ensure Tetr.io is in fullscreen mode and minimal graphics! (Idk sometimes works with extra graphics but alr idk)
- Check that coordinates are set accurately (dont delete coordinates.json it cant recreate itself)

**Hold not working:**
- Verify hold coordinates are set correctly
- Make sure hold key ('C') is not conflicting with other keys
- Check that hold box is visible and not covered

**Bot moving too fast/slow:**
- Adjust `key_delay` in settings
- Decrease `key_delay` if bot is too slow but just dont lol its suspicious.

### Performance Tips

- **Higher accuracy**: Increase `calculation_accuracy` (slower but better)
- **Faster gameplay**: Decrease `wait_time` and `key_delay`
- **Better hold decisions**: The bot automatically optimizes hold usage

## 📊 Coordinate File Format

The `coordinates.json` file contains: (NOTE THAT THIS IS JUST EXAMPLE AND YOU HAVE TO SET IT BY YOURSELF BECAUSE OF RESOLUTION DIFFERENCE!!!!!)
```json
{
    "x1_board": 777,
    "y1_board": 203,
    "x2_board": 1144,
    "y2_board": 937,
    "x1": 1264,
    "y1": 310,
    "x5": 1265,
    "y5": 744,
    "x_hold": 682,
    "y_hold": 309
}
```

## 🎮 Tips for Best Performance

1. **Use fullscreen mode** for consistent coordinate detection
2. **Set coordinates precisely** for accurate piece detection
3. **Adjust settings** based on your system performance (LOCK Chrome with 60fps or 120fps based on your screen refresh it doesnt make much sense and difference yet but still conscious.)
4. **Monitor the bot** during initial runs to ensure proper operation
5. **Use pause feature** (Q key) to stop/start as needed between round ending or resetting if bot is buggy

## ⚠️ Disclaimer

!!! This bot is for educational purposes. Please respect Tetr.io's terms of service and use responsibly. The bot is designed to help understand Tetris AI algorithms and should not be used to gain unfair advantages in competitive play !!!
!!! This is pretty bannable as i *tested* it on a high ranked account and got banned on **blitz** so dont even think about it. Its completely for educational PURPOSES ONLY !!!

https://github.com/user-attachments/assets/be0a750c-ffe3-4864-9ef5-c858dd4fa791


## 🤝 Contributing

Feel free to submit issues, feature requests, or improvements to make the bot even better! ill try to update it in 10 years if im alive. :P

---

**Enjoy your enhanced Tetr.io experience!** 🎮✨
