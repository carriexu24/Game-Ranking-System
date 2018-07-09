# Game-Ranking-System
Game ranking system implementation.

## Rules

You have been asked to implement the ranking system. All players have a rank determining their playing strength which gets updated after every game played. There are 25 regular ranks, and an extra rank, Legend, above that. The ranks are numbered in decreasing order, 25 being the lowest rank, 1 the second highest rank, and Legend the highest rank.

Each rank has a certain number of stars that one needs to gain before advancing to the next rank. If a player wins a game, she gains a star. If before the game the player was on rank 6-25, and this was the third or more consecutive win, she gains an additional bonus star for that win. When she has all the stars for her rank (see list below) and gains another star, she will instead gain one rank and have one star on the new rank.

For instance, if before a winning game the player had all the stars on her current rank, she will after the game have gained one rank and have 1 or 2 stars (depending on whether she got a bonus star) on the new rank. If on the other hand she had all stars except one on a rank, and won a game that also gave her a bonus star, she would gain one rank and have 1 star on the new rank.

If a player on rank 1-20 loses a game, she loses a star. If a player has zero stars on a rank and loses a star, she will lose a rank and have all stars minus one on the rank below. However, one can never drop below rank 20 (losing a game at rank 20 with no stars will have no effect).

If a player reaches the Legend rank, she will stay legend no matter how many losses she incurs afterwards.

The number of stars on each rank are as follows:

Rank 25-21: 2 stars
Rank 20-16: 3 stars
Rank 15-11: 4 stars
Rank 10-1: 5 stars
A player starts at rank 25 with no stars.

## Examples

Git clone the repository and run the code in the terminal.

1. Return 25.

```
python ranking.py WW
```

2. Return 24.

```
python ranking.py WWW
```

3. Return 24.

```
python ranking.py WLWLWLWL
```

4. Return 19.

```
python ranking.py WWWWWWWWWLLWW
```

5. Return 18.

```
python ranking.py WWWWWWWWWLWWL
```