# Chessmate Chess AI
Matric Computer Class Project in Java

## How to run
Run `src/build.bat` to compile and run. You will need the Java SDK.

I wrote this Java chess engine eight years ago in 2005 for my grade 12 high school project. I was 17 at the time, so I thought the code would be bad, but it still works and beats me every time! It won a regional prize or something (cash must have gotten lost in the mail). I'm pretty proud of it :).

![Chessmate Screenshot](/chessmate-screenshot.png "Chessmate Playing")

## Limitations
Chessmate has no opening book, cannot castle, nor take en passant. If you harbor sado-masochistic tendencies, you can easily modify the `Board` class and heuristic function to add castling.

## How does it work?
Chessmate uses an iterative deepening minimax search algorithm with alpha-beta pruning and simple horizon detection during exchanges with an original heuristic function.

That's a fancy way of saying it builds a tree of moves, rates each move with a number (using a heuristic function), then keeps exploring the leaf branches that seem promising. Minimax assumes its opponent will make the best sequence of moves it can think of and will then counter with a move that minimises your opportunities while maximising its own.

## Performance 
Chessmate has a terrible early game due the lack of an opening book, an average medium game and a pretty strong end game. It runs pretty fast for a Java application. I remember it searching through 500k moves/second on my shitty PC in 2005. I now get about 1.2M nodes/second on my Macbook Air running on a single thread.

## Database?
The project had a database requirement, but I ripped out the Access database prompt. It's mostly a gimmick that tracks a history of moves.

## Heuristic Function
The original heuristic function is probably the most interesting part of the project. I will write something about it as soon as I have read through it, 8 years after writing it.
