Overview

This project demonstrates a basic online chess automation setup using:

A UCI-compatible chess engine (e.g., Stockfish)

A lightweight Python backend

A Chrome extension frontend

The implementation is intentionally simple and minimal. It is designed as a proof-of-concept, not a production-ready system.

Prerequisites

Make sure you have the following installed:

Python 3

A UCI chess engine (e.g., Stockfish: https://stockfishchess.org/download/
)

Google Chrome

To check your Python installation:

python -V
# or
python3 -V


If this returns a version number, you're good to go.

Project Structure
backend/
extension/


backend/ – Python server that communicates with the chess engine

extension/ – Chrome extension that interacts with the browser

Installation
Backend Setup
1. Navigate to the backend folder
cd backend

2. Create a virtual environment

Windows:

python -m venv venv


MacOS/Linux:

python3 -m venv venv

3. Activate the virtual environment

Windows:

venv\Scripts\activate


MacOS/Linux:

source venv/bin/activate

4. Install dependencies
pip install -r requirements.txt

5. Add your chess engine

Create an engines directory inside backend and place your UCI engine executable inside it.

Example:

backend/
└── engines/
    └── stockfish.exe

6. Configure the .env file

Create or edit a .env file inside backend:

ENGINE="stockfish.exe"
ENGINES_PATH="./engines"


Adjust the engine name if needed.

7. Start the backend server
python server.py


The server will run at:

http://localhost:5000


Make sure this is running before using the extension.

Frontend (Chrome Extension) Setup

Open Google Chrome

Navigate to:

chrome://extensions/


Enable Developer Mode (top right)

Click Load unpacked

Select the extension folder from this repository

The extension should now be installed.

Usage

The backend server must be running before using the extension.

Go to chess.com

Open board settings

Set Piece Notation to Text (not figurine)

Start a game

Look for the engine panel below the board

Click Start Engine

Make a move to receive engine suggestions

Important Notes

The repository does not include a chess engine. You must download one separately.

Stockfish is free and works well for this setup.

This project is intentionally minimal and does not follow full production best practices.

Use responsibly and respect the rules of any platform you use.