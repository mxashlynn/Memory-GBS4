# Memory ✨🎴🌈

Painter Momo Array Discussion: https://discord.com/channels/554713715442712616/1209336784769523795

## 🚢 Week of the 31st
- Play Music
- Play Sound Effects
    - Move Cursor
    - Flip Card
    - Flip Card, Match!
    - Flip Card, No Match!
    - Game Won
    - Game Lost
- Polish
- More Bug Fixing
- Post Finished Game


## 🗺 Week of the 24th
- Player can Move pointer                               ⬅⬅⬅ HERE!
- Player can Select cards
- When player selects a card:
    - If the card is already face up, nothing happens
    - If the card is face down and no Move has begun:
        - Reveal card
        - Set First Revealed Card value to this card's value
        - Begin Move
    - If the card is face down and a Move has begun:
        - Reveal card
        - If this card's value matched First Revealed Card's value:
            - Play a chime
            - Increment total match count
            - Reset Player HP
        - Else:
            - Play a buzz
            - Flip both cards back over to hide them
            - Decrement Player HP
        - Increment Move count
        - End Move
    - If total match count is 10:
        - Play Win Jingle
        - Display Congratulations and Total Moves
        - End Game
    - Else If HP is zero:
        - Play Fail Jingle
        - Display Game Over
        - End Game
- Play Testing
- Bug Fixing


## ✓ Done
- Create a scene stating the rules
- Sets up fonts.
- Wait on Title Screen till Button Pressed
- Set up status line
- Set up player sprite
- Start a new game whenever playfield is loaded
- Store cards in array
- Start New Game
    - Set game state variables
    - Randomize card array
    - Display cards face down

