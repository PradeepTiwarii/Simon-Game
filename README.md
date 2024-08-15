# Simon Says Game - README

## Project Overview

This project is a **Simon Says Game** implemented using HTML, CSS, and JavaScript. The game generates a sequence of colors that the user must replicate by clicking the corresponding buttons. The sequence becomes progressively longer as the game advances, increasing the difficulty. The game tracks the highest score achieved during the session.

### Features:
1. **Start Game**: Press any key to begin the game.
2. **Color Buttons**: Four interactive buttons (Red, Yellow, Green, Purple) that light up to represent the sequence.
3. **Sequence Matching**: The player replicates the displayed sequence, with feedback provided when the user is incorrect.
4. **Score Tracking**: Displays the highest score achieved during the session.
5. **Game Over**: If the player makes a mistake, the game resets and displays the score.

---

## Project Structure:

### HTML:
The `index.html` file includes:
- Titles: 
  - `h1`: Game name ("Simon Says Game")
  - `h2`: Instructions and level display
  - `h3`: High score tracking
- Four colored buttons arranged in a grid (Red, Yellow, Green, Purple) to simulate the Simon Says board.
- JavaScript file `app.js` linked for game functionality.

### CSS:
The `style.css` file handles the basic layout and button styling:
- **Center alignment**: The game elements are centered on the page.
- **Buttons**: Each color button is styled to have a specific background color and a border. They change color when clicked using the `.flash` class.
- **Responsive Layout**: The buttons are arranged in two rows.

### JavaScript:
The `app.js` file contains the game logic:
- **Game Sequence**: An array `gameSeq[]` stores the randomly generated sequence.
- **User Sequence**: The array `userSeq[]` stores the sequence of button presses by the user.
- **Score and Levels**: Tracks the highest score and the current level.
- **Event Listeners**: Listens for keypress events to start the game and button clicks to record user input.
- **Game Over**: Resets the game when the user makes a mistake and updates the high score if applicable.

---

## Project Breakdown:

### 1. **Game Initialization**:
- The game starts when the user presses any key. Once the game starts, the `levelUp()` function is called to generate a new sequence.

### 2. **Button Flashing**:
- Each button has a distinct color and will "flash" white when the button is pressed or selected by the game. This visual feedback helps the user track the sequence.

### 3. **Leveling Up**:
- As the user progresses through the game, the difficulty increases by adding a new color to the sequence every time the user successfully completes the current sequence.

### 4. **Checking User Input**:
- When the user presses a button, the game checks the user’s input against the sequence stored in `gameSeq[]` using the `checkAns()` function.
- If the user is correct, the game proceeds to the next level. If not, the game is over, and the user's score is compared with the highest score.

### 5. **Game Reset**:
- If the user makes a mistake, the game resets the sequence, level, and user input. The background flashes red briefly to indicate game over.

---

## How to Run the Project

### 1. Clone the Repository:
```bash
git clone https://github.com/your-repo-name.git
```

### 2. Open the Project:
Open the `index.html` file in any modern web browser to view and play the game.

### 3. File Structure:

```
/Simon-Says-Game
│
├── index.html       # Main HTML file
├── style.css        # CSS file for styling the game
├── app.js           # JavaScript file for game logic
└── README.md        # This readme file
```

### 4. Game Instructions:
1. Press any key to start the game.
2. The game will flash a sequence of colors. Replicate the sequence by clicking on the respective color buttons.
3. As you progress, the sequence will get longer.
4. If you make a mistake, the game will end, and you can restart by pressing any key.

---

## Customization:

1. **Colors**: You can customize the colors of the buttons by modifying the `.red`, `.yellow`, `.green`, and `.purple` classes in the CSS file.
2. **Game Difficulty**: Adjust the time delay or button flashing duration in the `btnFlash()` function to make the game easier or harder.
3. **Sequence Length**: Modify the random sequence generation logic to make the game more challenging by changing the number of buttons or adding more colors.

---

## Credits:
This project was built using basic web technologies: 
- **HTML** for structure.
- **CSS** for design.
- **JavaScript** for functionality and game logic.

---

### License:

This project is licensed under the MIT License. You are free to use, modify, and distribute the project for personal or educational purposes.
