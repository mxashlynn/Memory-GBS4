# Memory ✨🎴🌈


## 🚢 Week of the 31st
- When player selects a card:
    - If the card is already face up, nothing happens
    - If the card is face down, it is Flipped up, revealing it
- When a card is revealed:
    - Increment Flips Made Counter
    - If a Turn has not begun:
        - Begin Turn
        - Set Old Revealed Card Value to this card's value
        - Set Old Revealed Card Index to this card's index
        - Set Old Revealed Card X to selector's X
        - Set Old Revealed Card Y to selector's Y
    - If a Turn has begun:
        - Set New Revealed Card Value to this card's value
        - Set New Revealed Card Index to this card's index
        - Set New Revealed Card X to selector's X
        - Set New Revealed Card Y to selector's Y
        - Compare values of Old and New cards
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
- Play Music
    - Title
    - Playfield
- Play Sound Effects
    - Move Cursor
    - Flip Card
    - Flip Card, Match!
    - Flip Card, No Match!
    - Game Won
    - Game Lost
- Play Testing
- Bug Fixing
- Polish
- Post Finished Game


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
- Player can move Selector
- Player can Select cards

