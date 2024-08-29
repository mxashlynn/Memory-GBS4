# Memory ✨🎴🌈


## Layout

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

🃏 🃏 🃏 🃏 🃏

- 5x4 = 20 cards


## Cards

| Encoding | Name          | Revealed? | Glyph | Pairs |
| -------- | ------------- | --------- | ----- | ----- |
|  0       | UNINITIALIZED |       N/A |       | 0     |
|  1       | Moon          |         ✔ | 🌙    | 2     |
|  2       | Sun           |         ✔ | 🌞    | 2     |
|  3       | Stars         |         ✔ | ✨     | 2     |
|  4       | Planet        |         ✔ | 🪐     | 1     |
|  5       | Aurora        |         ✔ | 🌌    | 1     |
|  6       | Rainbow       |         ✔ | 🌈    | 1     |
|  7       | Lightning     |         ✔ | ⚡     | 1     |
| 11       | Moon          |        🚫 | 🌙    | 2     |
| 12       | Sun           |        🚫 | 🌞    | 2     |
| 13       | Stars         |        🚫 | ✨     | 2     |
| 14       | Planet        |        🚫 | 🪐     | 1     |
| 15       | Aurora        |        🚫 | 🌌    | 1     |
| 16       | Rainbow       |        🚫 | 🌈    | 1     |
| 17       | Lightning     |        🚫 | ⚡     | 1     |

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


## Matching Algorithm
- The game consists of turns.
- A turn consists of flipping two cards.
    - The turn begins when the first card is flipped and ends when the second card if flipped.
    - We call the first flipped card the "Old Card" and the second flipped card the "New Card".
    - Score is recorded in terms of flips, not turns.
- The player can move their selector both during and between turns.
    - When they hit the 'A' button, they select the card under the selector.
- When player selects a card:
    - If the card is already face up, nothing happens;
    - If the card is face down, it is Flipped up, revealing it.
- When a card is revealed:
    - Increment Flips Made Counter
    - If a Turn has not begun:
        - Begin Turn
        - Set Old Revealed Card Value to this card's value.
        - Set Old Revealed Card Index to this card's index.
        - Set Old Revealed Card X to selector's X.
        - Set Old Revealed Card Y to selector's Y.
    - If a Turn has begun:
        - Set New Revealed Card Value to this card's value.
        - Set New Revealed Card Index to this card's index.
        - Set New Revealed Card X to selector's X.
        - Set New Revealed Card Y to selector's Y.
        - Compare values of Old and New cards.
        - If this card's value matches Old Revealed Card's value:
            - Play a chime
            - Increment total match count
            - Reset Player HP
        - Else:
            - Play a buzz
            - Flip both cards back over to hide them
            - Decrement Player HP
        - Increment Turn count
        - End Turn
    - If total match count is 10:
        - Play Win Jingle
        - Display Congratulations and Total Turns
        - End Game
    - Else If HP is zero:
        - Play Fail Jingle
        - Display Game Over
        - End Game


## Variables

- Game State
    - 0 = Unstarted
    - 1 = In Play
    - 2 = Lost
    - 3 = Won
- Player Match Counter
    - 0…10 = How many card pairs found so far.
- Player Flips Made Counter
    - 0…MAX_INT = How many flips made so far.
- Player Flips Left Counter
    - 3…0 = How many flips remaining till game over.
- Card X,Y
    - 20 variables in a row forming an implicit array
    - Card 0,0 is the upper  left card and has index 4
    - Card 3,4 is the lower right card and has index 23
- Index I & Index J
    - Used in Shuffling algorithm
- Old Revealed Card Index
    - Indicates the index of the card the player has flipped face-up at the beginning of the turn.  Values:
        - -1    = No cards are revealed.  AKA, the current turn has not begun.
        - 0…19  = Index of revealed card.  AKA, we are mid-turn.
- Old Revealed Card Value
    - Value of the card revealed at the beginning of the current turn.
- Old Revealed Card X & Old Revealed Card Y
    - Tile coordinates of the card revealed at the beginning of the current turn.
- New Revealed Card Index
    - Index of the card the player has flipped face-up at the end of the turn.  Values as before.
- New Revealed Card Value
    - Value of the card revealed at the end of the current turn.
- New Revealed Card X & New Revealed Card Y
    - Tile coordinates of the card revealed at the end of the current turn.


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
