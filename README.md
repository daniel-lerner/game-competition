# 🎲 Board Game Tournament Scoring System

An interactive Python application for managing board game tournament scoring with real-time Google Sheets integration and user-friendly GUI.

## 🌟 Features

- **Real-time scoring**: Automatic score calculation and Google Sheets updates
- **User-friendly interface**: Intuitive GUI with dropdown menus and confirmation dialogs
- **Multiple game support**: Pre-configured scoring rules for 11 different board games
- **Live leaderboard**: Real-time score display on TV/monitor via Google Sheets
- **Object-oriented architecture**: Clean, maintainable code structure
- **Error handling**: Robust error management and user feedback

## 🎮 Supported Games

- Exploding Kittens
- Halli Galli
- Saco de Ossos
- Futebol de Moeda
- Ticket to Ride
- King of Tokyo
- Paper Town
- Abstratus
- Imagine
- Mille Fiori
- 7 Wonders

## 🏗️ Architecture

The system is built with object-oriented programming principles:

- **GameConfig**: Manages player and game configurations
- **UIManager**: Handles GUI creation and user interactions
- **ScoreCalculator**: Calculates scores based on game-specific rules
- **GoogleSheetsManager**: Manages Google Sheets API integration
- **GameScoreManager**: Main orchestrator class

## 🚀 Setup

### Prerequisites

- Python 3.7+
- Google Cloud Project with Sheets API enabled
- Service account credentials (JSON file)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/daniel-lerner/game-competition.git
cd game-competition
```

2. Install required packages:
```bash
pip install pandas openpyxl pillow gspread oauth2client
```

3. Setup Google Sheets API:
   - Create a Google Cloud Project
   - Enable Google Sheets API
   - Create a service account
   - Download credentials JSON file
   - Rename it to `credentials.json` and place in project root

4. Create your Google Sheets spreadsheet with:
   - Column headers: Jogador, [Game Names], Total
   - Player names in the first column

5. Add the image file `Taverna_Lerner.webp` (optional) for GUI decoration

### Running the Application

```bash
python main.py
```

## 🎯 How It Works

1. **Start the application**: Run the main script to open the menu
2. **Select "Add Score"**: Choose this option to register a new game result
3. **Fill game details**: 
   - Select player name
   - Choose the game played
   - Specify number of players
   - Select final position
4. **Confirm**: Review and confirm the information
5. **Automatic update**: The system calculates points and updates the Google Sheets in real-time

## 🏆 Scoring System

Points are calculated based on:
- **Game complexity**: More complex games award more points
- **Number of players**: More players = higher competition = more points
- **Final position**: 1st place gets full points, 2nd and 3rd get proportional rewards
- **Game duration**: Longer games typically award more points

## 📊 Real-time Display

The Google Sheets integration allows for:
- Live leaderboard display on any screen
- Real-time score updates
- Shareable link for remote viewing
- Automatic total calculation

## 🔧 Customization

The system supports easy customization of:
- Player names (modify `GameConfig.players`)
- Game list (modify `GameConfig.games`)
- Scoring rules (modify `ScoreCalculator.calculate_points`)
- UI appearance (modify `UIManager` methods)

## 🚀 Future Improvements

- **JSON Configuration**: External configuration files for games, players, and scoring rules
- **Modular Structure**: Better folder organization and project structure
- **Plugin System**: Easy addition of new games without code modification
- **Enhanced Scalability**: More flexible and maintainable architecture
- **Configuration UI**: Admin interface for managing games and rules
- **Statistics Dashboard**: Advanced analytics and game statistics

## 🛠️ Tech Stack

- **Python 3.7+**: Core programming language
- **Tkinter**: GUI framework
- **Google Sheets API**: Real-time data synchronization
- **Pandas**: Data manipulation
- **PIL (Pillow)**: Image handling
- **gspread**: Google Sheets Python API

## 📝 License

This project is open source and available under the MIT License. Feel free to adapt for your own gamimg events!

---

*Transform your board game nights into competitive tournaments with automated scoring!* 🎲✨