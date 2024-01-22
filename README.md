 # Blackjack Game with MongoDB Integration

This repository contains a Python script that simulates a blackjack game with multiple players and a dealer. The game is played according to standard blackjack rules, with the goal of getting as close to 21 as possible without going over. The script also integrates with MongoDB to store the scores of each player.

## Prerequisites

To run this script, you will need the following:

* Python 3 or later
* MongoDB installed and running
* A MongoDB client, such as Robo 3T or MongoDB Compass

## Installation

To install the required dependencies, run the following command in your terminal:

```
pip install pymongo
```

## Usage

To play the game, simply run the `blackjack.py` script. You will be prompted to enter the number of players (up to 3) and then the game will begin.

## Gameplay

The game is played in turns, with each player taking their turn before the dealer. On their turn, a player can either hit (take another card) or stand (keep their current hand). If a player goes over 21, they bust and lose the game.

The dealer hits until they reach 17 or higher. If the dealer goes over 21, all players who have not busted win the game.

## Scoring

The winner of the game is the player who gets closest to 21 without going over. If a player and the dealer tie, the dealer wins.

## MongoDB Integration

The script uses MongoDB to store the scores of each player. After each game, the player's name, score, and result are inserted into a MongoDB collection called `scores`.

## Code Overview

The script is written in Python and uses the `pymongo` library to connect to MongoDB. The main function of the script is called `bj()`, which runs the game loop.

The `bj()` function first prompts the user to enter the number of players. It then deals two cards to each player and two cards to the dealer (one of the dealer's cards is hidden).

The function then loops through each player, giving them the option to hit or stand. If a player hits, they are dealt another card. If a player stands, their turn is over.

After all players have taken their turns, the dealer takes their turn. The dealer hits until they reach 17 or higher.

Once the dealer has taken their turn, the scores of each player are calculated.
