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
| 0     | Moon          | 🌙    | 4     |
| 1     | Sun           | 🌞    | 4     |
| 2     | Stars         | ✨     | 4     |
| 3     | Planet        | 🪐     | 2     |
| 4     | Aurora        | 🌌    | 2     |
| 5     | Rainbow       | 🌈    | 2     |
| 6     | Lightning     | ⚡     | 2     |
| 7     | UNINITIALIZED |       | 0     |

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
