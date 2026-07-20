# Chess System in Java

In this project, I developed a complete console-based chess system using Java and Object-Oriented Programming.

The main goal was to apply the concepts studied throughout the course in a larger and more structured project, combining class design, inheritance, polymorphism, exceptions, collections and game rules.

## Topics Covered
- Object-Oriented Programming
- Encapsulation and access modifiers
- Constructors
- Associations between objects
- Inheritance
- Method overriding
- Polymorphism
- Abstract classes and methods
- Enumerations
- Custom exceptions
- Defensive programming
- Method overloading
- Static members
- Layered architecture
- Matrices
- Lists
- Git and GitHub version control

## Project Structure
The system was organized into different layers and responsibilities:

- Board layer for managing positions, pieces and board rules
- Chess layer for implementing match rules and chess-specific behavior
- User interface layer for reading data and displaying the match in the console
- Application layer for controlling the execution flow

This organization helped separate responsibilities and keep the project easier to understand and maintain.

## Main Classes
Some of the main classes created during the project were:

- `Position`
- `Board`
- `Piece`
- `ChessPosition`
- `ChessPiece`
- `ChessMatch`
- `UI`
- `BoardException`
- `ChessException`

Each chess piece was represented by its own class:

- `King`
- `Queen`
- `Rook`
- `Bishop`
- `Knight`
- `Pawn`

## Key Concepts

### Board Representation
The chessboard was represented using a matrix, allowing each position to store a chess piece or remain empty.

The system converts traditional chess positions, such as `a1` or `e4`, into matrix coordinates used internally by the application.

### Inheritance and Polymorphism
The chess pieces inherit common attributes and behaviors from base classes.

Each piece implements its own movement rules by overriding an abstract method responsible for calculating possible moves.

This allows the system to work with different pieces through a common type while executing the correct behavior for each specific piece.

### Possible Moves
The system calculates the possible movements of a selected piece and represents them using a boolean matrix.

This matrix is also used by the interface to highlight the valid destination positions on the board.

### Exception Handling
Custom exceptions were created to represent invalid operations related to the board and the chess match.

The system validates situations such as:

- Selecting a position outside the board
- Selecting an empty position
- Selecting an opponent's piece
- Choosing a piece without possible moves
- Moving to an invalid destination
- Attempting a move that leaves the player's own king in check

Defensive programming was applied to keep the game state consistent.

## Implemented Features
- Complete chessboard setup
- Piece positioning
- Piece movement
- Validation of source and target positions
- Possible move calculation
- Turn control
- Current player control
- Piece capture
- Captured piece display
- Move counter
- Check detection
- Checkmate detection
- Undoing moves during validations
- Colored piece display in the terminal

## Chess Rules
The project implements the individual movement rules for all main chess pieces:

- King
- Queen
- Rook
- Bishop
- Knight
- Pawn

It also includes important chess rules and special moves:

### Castling
The system validates the movement of the king and rook, their move counts and the required free positions before performing castling.

### En Passant
The match keeps track of the pawn vulnerable to an *en passant* capture and only allows the movement during the correct turn.

### Promotion
When a pawn reaches the opposite side of the board, it can be replaced by another piece.

## Match Flow
During each turn, the system:

1. Displays the current board and match information
2. Reads the source position
3. Shows the possible moves for the selected piece
4. Reads the target position
5. Performs and validates the movement
6. Handles possible captures
7. Checks whether the move placed a king in check
8. Tests for checkmate
9. Changes the current player

## What I Learned
This project was especially important because it brought together several concepts that had previously been studied separately.

Developing the chess system helped me understand how classes collaborate inside a larger application and how inheritance, polymorphism and abstraction can be used to represent different behaviors without duplicating logic.

I also practiced organizing responsibilities, validating business rules, handling exceptions and maintaining a consistent application state.

Implementing check, checkmate and special moves showed how more complex rules can be divided into smaller methods and responsibilities.

---

## 📌 Resumo (Português)

Neste projeto desenvolvi um sistema completo de jogo de xadrez em Java pelo terminal, aplicando diversos conceitos estudados ao longo do curso.

Trabalhei com encapsulamento, herança, polimorfismo, classes e métodos abstratos, enumerações, composição, sobrecarga, exceções personalizadas, matrizes, listas e organização do sistema em camadas.

Cada peça foi representada por uma classe própria e implementou suas regras de movimento através do polimorfismo. O sistema também calcula e exibe os movimentos possíveis de cada peça.

Foram implementados o controle de turnos, capturas, validação de movimentos, contagem de movimentos, xeque, xeque-mate e os movimentos especiais de roque, *en passant* e promoção.

Esse foi um projeto muito importante para consolidar os conteúdos estudados, porque reuniu vários conceitos de orientação a objetos dentro de uma aplicação maior, com regras mais complexas e responsabilidades bem divididas.
