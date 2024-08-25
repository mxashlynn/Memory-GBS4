# Memory ✨🎴🌈


## Layout

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

- 5x4 = 20 cards


## Cards

| Encoding | Name          | Glyph | Pairs |
| -------- | ------------- | ----- | ----- |
| 0        | UNINITIALIZED |       | 0     |
| 1        | Moon          | 🌙    | 2     |
| 2        | Sun           | 🌞    | 2     |
| 3        | Stars         | ✨     | 2     |
| 4        | Planet        | 🪐     | 1     |
| 5        | Aurora        | 🌌    | 1     |
| 6        | Rainbow       | 🌈    | 1     |
| 7        | Lightning     | ⚡     | 1     |

- 7 Card Types
- 20 Cards Total


## Shuffle Algorithm

Written here in pseudo-C:
```
for (byte i = high_index; i > low_index; i--)
{
    j = random(from low_index to i);
    push(array[i]);
    push(array[j]);
    array[i] = pop();
    array[j] = pop();
}
```


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
- Index I & Index J
    - Used in Shuffling algorithm
- Current Revealed Card
    - Indicates the index of the card the player has flipped face-up.  Values:
        - -1    = No cards are revealed.
        - 0…19  = Index of revealed card.


## Writing Every Card in Dialogue



\240¡



¢£



¤¥



¦§



¨©



ª«



¬\255

\216\217
\236\237
\256\257

### Dialogue Dealing Effect

\216\217 \216\217 \216\217 \216\217 \216\217
\236\237Shuffling\177\236\237
\256\257 \256\257 \256\257 \256\257 \256\257
