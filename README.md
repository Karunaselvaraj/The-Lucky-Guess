# The-Lucky-Guess
# Guess the Number Game

A simple, fun, and interactive number-guessing game built with **HTML**, **CSS**, and **JavaScript**. The objective of the game is to guess a randomly generated number between 0 and 9. Players have a limited number of attempts to get the correct answer.

## Features
- Random number generation for every new game.
- User-friendly interface with input validation.
- Score tracking with decreasing points for incorrect guesses.
- Alerts for winning or losing the game.
- Responsive and visually appealing design.

## How to Play
1. Enter a number (between 0 and 9) in the input field.
2. Click the "Check" button to see if your guess is correct.
3. If your guess matches the randomly generated number, you win! If not, your score decreases.
4. The game ends when the score reaches 0 or you guess the correct number.

## Screenshots
![image](https://github.com/user-attachments/assets/05cedd31-1267-47bb-9e30-b7037f07dd82)
 <!-- Add a screenshot link here if needed -->

## Installation
1. Clone this repository or download the files.
2. Open the `index.html` file in any modern web browser.

## Code Structure
- **HTML**: The structure of the game interface.
- **CSS**: Styling for a neat and formal appearance.
- **JavaScript**: Game logic, random number generation, and interactivity.

## Code Example
Here is a snippet of the main game logic:

```javascript
var minus = 10;
var r = Math.random();
r = Math.floor(r * 10);
console.log(r);

function check() {
    var a = document.getElementById("num");
    var ans = document.getElementById("wr");
    var s = document.getElementById("score");

    if (r == a.value) {
        ans.textContent = "🎉 Correct! You guessed it!";
        ans.style.color = "#10b981";
        alert("WON");
    } else {
        ans.textContent = "❌ Incorrect. Try again!";
        ans.style.color = "#ef4444";
        s.textContent = "Score: " + minus;
        minus--;

        if (minus < 0) {
            alert("Game Over! The correct number was " + r);
            location.reload();
        }
    }
}
```

## Technologies Used
- **HTML** for structure
- **CSS** for styling
- **JavaScript** for functionality

## Future Improvements
- Add a "Play Again" button to reset the game without refreshing the page.
- Include a difficulty setting (e.g., easy, medium, hard).
- Add animations for a more interactive user experience.
- Expand the range of numbers (e.g., 0–99).

## License
This project is open-source and available for use under the [MIT License](LICENSE).

---
Enjoy the game and have fun guessing! 🎮
