Pac-Man Animation
Overview
This project is a simple web-based animation of a Pac-Man character that moves horizontally across the screen. The character changes its appearance as it moves, simulating a basic game-like experience. The animation starts when the user clicks the "START" button.

Features
Pac-Man Animation: The character moves back and forth across the screen, changing images to simulate movement.
Responsive Design: The animation adapts to different screen sizes.
Simple User Interface: A single button to start the animation.
Prerequisites
Basic knowledge of HTML, CSS, and JavaScript.
A modern web browser to run the application.
Setup Instructions
Clone the Repository


git clone <repository-url>
cd <repository-directory>
Open the HTML File
Open the index.html file in your preferred web browser.

Image Assets
Ensure that the image files (PacMan1.png, PacMan2.png, PacMan3.png, PacMan4.png) are in the same directory as the HTML file for the animation to work correctly.

Usage
Click the START button to begin the animation. The Pac-Man character will appear and start moving across the screen.
The character will bounce back when it reaches the edges of the viewport.
Code Structure
HTML: Contains the structure of the webpage, including the button to start the game and the image element for the Pac-Man character.
CSS: Styles for the Pac-Man character, including its size and position.
JavaScript: Handles the logic for moving the character, changing images, and starting the animation.
Example Code Snippet
Here’s a brief look at the JavaScript code that controls the Pac-Man's movement and image changes:


function imgMove() {
    if (isGameStarted) {
        imageElement.src = currentImages[currentIndex];
        currentIndex = (currentIndex + 1) % currentImages.length;
    }
}

function move() {
    if (isGameStarted) {
        pos = pos + vel;
        if (pos > window.innerWidth - imageElement.width || pos < 0) {
            vel = -vel;
            currentImages = vel > 0 ? imagesRight : imagesLeft;
        }
        imageElement.style.left = pos + 'px';
    }
}
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgments
Thanks to the web development community for the resources and inspiration to create this project.


