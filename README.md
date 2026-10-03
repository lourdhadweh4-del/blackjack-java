# Blackjack — Java Swing

A desktop Blackjack game developed as a Programming II final project. Built with Java and Swing, with separate classes for cards, decks, hands, players, the dealer, game state, and the interface.

## Features

- Custom-drawn playing cards and a hidden dealer card.
- Hit, stand, and start a new round.
- Simulated chips in denominations of 1, 10, 100, and 500.
- A starting balance of 1,000 and win, loss, and tie handling.
- Ace values adjust from 11 to 1 when needed; the dealer draws below 17.

## Run

Requires a desktop Java environment. Compiled and checked with JDK 24; no third-party libraries are required.

From the repository root:

```sh
mkdir -p out
javac -d out src/*.java
java -cp out Main
```

In IntelliJ, open the folder, select a JDK, mark `src` as Sources Root if needed, and run `Main`. In VS Code, open the folder with Java support installed and run `Main.java`.

Select one or more chip buttons, then **New Game** to deal. Use **Hit** for another card or **Stand** to finish your turn. After a completed round, place a new bet and select **New Game** again.

## Code map

| Area | Classes |
| --- | --- |
| Cards and scoring | `Card`, `Deck`, `Hand` |
| Participants | `Player`, `Dealer` |
| Round and betting state | `BlackJackGame` |
| Swing interface | `BlackJackFrame`, `GamePanel`, `ControlPanel` |
| Entry point | `Main` |

## Project scope

This is a classroom implementation with simplified rules: wins return twice the stake, including a starting blackjack. It does not implement splitting, doubling down, insurance, or the full set of casino rules. A starting player blackjack ends the round immediately.

The interface uses a green table background when the optional `BlackJackBackground.png` resource is absent. The original image is not included in this source release. Reports, recordings, compiled files, and editor metadata are excluded.

## Validation

The source compiles with JDK 24. Automated checks cover deck uniqueness, flexible ace scoring, balance changes, round initialization, and rendering the game panel without an image. A full interactive playthrough has not been verified.
