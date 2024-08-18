# Memory ✨🎴🌈

## Layout

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

- 5x4 = 20 cards

## Cards

| Index | Name          | Glyph | Pairs |
| ----- | ------------- | ----- | ----- |
| 0     | UNINITIALIZED |       | 0     |
| 1     | Moon          | 🌙    | 2     |
| 2     | Sun           | 🌞    | 2     |
| 3     | Stars         | ✨     | 2     |
| 4     | Planet        | 🪐     | 1     |
| 5     | Aurora        | 🌌    | 1     |
| 6     | Rainbow       | 🌈    | 1     |
| 7     | Lightning     | ⚡     | 1     |

- 7 Card Types
- 20 Cards Total


## Variables

- Game State
    - 0 = Unstarted
    - 1 = In Play
    - 2 = Lost
    - 3 = Won
- Player Match Count
    - 0…10 = How many card pairs found so far.
- Player Flips Made Count
    - 0…MAX_INT = How many flips made so far.
- Player Flips Left Count
    - 3…0 = How many flips remaining till game over.
- Card X,Y
    - 20 variables in a row forming an implicit array
    - Card 0,0 is the upper  left card and has index 4
    - Card 3,4 is the lower right card and has index 23
