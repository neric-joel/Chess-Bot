# Chess Bot

A simple chess automation demo using a Python backend and Chrome extension.

## Requirements

- Python 3
- Google Chrome
- A UCI chess engine ([Stockfish](https://stockfishchess.org/download/))

## Setup

### Backend

```bash
cd backend
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # MacOS/Linux
pip install -r requirements.txt
```

Create `backend/engines/` and place your engine inside it, then configure `backend/.env`:

```
ENGINE="stockfish.exe"
ENGINES_PATH="./engines"
```

Start the server:

```bash
python server.py
```

### Chrome Extension

1. Go to `chrome://extensions/`
2. Enable **Developer Mode**
3. Click **Load unpacked** and select the `extension` folder

## Usage

1. Start the backend server
2. Go to chess.com and set **Piece Notation** to **Text** in board settings
3. Start a game
4. Click **Start Engine** in the panel below the board
5. Make a move to get engine suggestions
