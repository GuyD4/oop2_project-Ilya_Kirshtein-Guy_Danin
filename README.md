# OOP2_Project

## Authors:
- Ilya Kirshtein	
- Guy Danin	

## Overview:
This project is a Chess Engine developed as part of an Object-Oriented Programming 2 course. The game includes the following features:
- Player vs Player and Player vs AI gameplay options.
- Chess puzzle solving.
- Game review functionality.

The AI utilizes the Minimax algorithm with alpha-beta pruning for decision making. The architecture incorporates various design patterns for clean code, scalability, and maintainability.

## Created Files:
### Command Classes:
- `BackToMenuCommand.h`: Navigate back to the main menu.
- `ButtonCommand.h`: Base class for all button commands.
- `ChangeGameStateCommand.h`: Change the current game state.
- `ExitCommand.h`: Exit the game.
- `NextPuzzleCommand.h`: Load the next puzzle.
- `NextStateCommand.h`: Move to the next game state.
- `PuzzleCommand.h`: Puzzle management commands.
- `PVPCommand.h`: Player vs Player mode.
- `RematchCommand.h`: Initiate a rematch.
- `UndoPuzzleCommand.h`: Undo the last puzzle move.
- `VBlackAICommand.h`: Set AI as black.
- `VWhiteAICommand.h`: Set AI as white.

### State Classes:
- `GameOverState.h`: Represents game over state.
- `GameState.h`: Base class for all game states.
- `PlayerXPromotionState.h`: Player promotion state.
- `PlayerXTurnState.h`: Player's turn state.
- `PuzzleGameState.h`: Puzzle gameplay state.
- `ReviewState.h`: Review game state.
- `WaitGameState.h`: Waiting during gameplay state.
- `HistoryState.h`: Manages game history.

### UI Classes:
- `EndGameUI.h`: End game screen UI.
- `GameUI.h`: Base class for game UI elements.
- `PlayUI.h`: Main gameplay screen UI.
- `PuzzleUI.h`: Puzzle mode UI.
- `ReviewUI.h`: Review mode UI.

### Factory Classes:
- `BlackAICreator.h`: Creates AI for black pieces.
- `GameHistoryCreator.h`: Creates game history object.
- `MainMenuCreator.h`: Creates main menu.
- `MenuCreator.h`: Base class for menu creation.
- `MenuFactory.h`: Factory class for menus.
- `PlayMenuCreator.h`: Creates play menu.
- `PuzzleMenuCreator.h`: Creates puzzle menu.
- `WhiteAICreator.h`: Creates AI for white pieces.

### SFML Classes:
- `SFMLBoard.h`: Renders chessboard using SFML.
- `SFMLPiece.h`: Represents chess piece in SFML.
- `SFMLPieceFactory.h`: Factory class for SFML chess pieces.
- `Tile.h`: Represents a tile on the chessboard.

### Controller Classes:
- `AIController.h`: Manages AI.
- `Controller.h`: Base class for controllers.
- `PlayerController.h`: Manages player interactions.

### Test Classes:
- `TestAI.h`: Tests AI functionality.

### Menu Classes:
- `Menu.h`: Game menu.
- `MenuState.h`: Manages menu state.
- `StateMachine.h`: Manages game states.

### Observer Classes:
- `IObservable.h`: Manages list of observers.
- `IObserver.h`: Receives updates from observables.

### Logic Classes:
- `IGenerate.h`: Interface for generating moves.
- `NBoard.h`: Manages board state and moves.
- `OpeningBook.h`: Manages opening book for chess moves.
- `PieceLogic.h`: Contains piece movement logic.
- `PromotionBox.h`: Handles pawn promotion in chess.

### Utility Classes:
- `Assets.h`: Manages game assets.
- `BoardStack.h`: Saves and restores game moves.
- `Button.h`: Represents a game button.
- `Utilities.h`: Utility functions and constants.

## Data Structures:
### BoardStack:
- Role: Saves and restores game moves.

### StateMachine:
- `std::stack<statePtr> m_stateStack`: Uses shared pointers for efficient state management.

### NBoard:
- Role: Efficiently manages chess engine operations.

## Algorithms:
### Minimax Algorithm with Alpha-Beta Pruning:
- Role: Decision-making algorithm for AI player.

### Fen Algorithm:
- Role: Translates FEN strings to board positions.

### PieceLogic:
- Role: Manages piece movements and rules in chess.

## Design:
The project design incorporates several design patterns:
- Command Pattern: For menu actions and game state changes.
- State Pattern: Manages different game states.
- Factory Pattern: Creates instances of game components.
- Observer Pattern: Allows multiple objects to react to game events.

## Remarks:
This project demonstrates advanced OOP principles and design patterns in game development, with integration of AI algorithms.

## Known Bugs:
- None reported currently.
