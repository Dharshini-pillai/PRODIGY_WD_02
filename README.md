This is a fully self-contained and functional Stopwatch Web Application!

Since you provided the complete HTML, CSS (in a <style> block), and JavaScript (in a <script> block) all in one file, there's no need to separate them. I'll provide you with a README.md for this specific file, explaining what it does and how it works, as if this were a single deliverable.

README.md
Stopwatch Web Application
This is a simple, modern, and fully functional Stopwatch web application implemented using pure HTML, inline CSS, and vanilla JavaScript. It allows users to start, stop, and reset a timer.

The entire application is contained within a single index.html file for easy deployment and testing.

🚀 Getting Started
Prerequisites
A modern web browser (Chrome, Firefox, Safari, Edge, etc.).

Usage
Save the Code: Save the provided code snippet as a single file named stopwatch.html (or index.html).

Open in Browser: Double-click the file to open it in your web browser.

Interact:

Click Start to begin the timer.

Click Stop (which replaces "Start") to pause the timer.

Click Reset to stop the timer (if running) and clear the displayed time back to 00:00:00.

⚙️ Implementation Details
HTML Structure
The HTML is minimal, providing the container, the main title, the time display (divided into separate <span> elements for hours, minutes, and seconds for easy manipulation), and two control buttons.

CSS Styling
The styles are written directly in a <style> tag within the head of the document.

Uses a clean, centered layout with a light background and a subtle shadow on the main container.

The time display is large and readable.

Buttons are color-coded: Green for Start, Amber/Orange for Stop, and Red for Reset.

CSS classes are dynamically swapped via JavaScript to change the button color and text when the timer is running/paused.

JavaScript Logic
The logic is contained within a <script> tag at the end of the <body>.

Variables:

[hours, minutes, seconds]: Array storing the current time value.

timer: Holds the ID returned by setInterval(), allowing the timer to be cleared (stopped).

isRunning: A boolean flag to track the state of the stopwatch.

stopwatch() Function:

Increments the seconds count every time it is called.

Manages the rollover from 60 seconds to 1 minute, and 60 minutes to 1 hour.

Uses a pad() helper function to ensure all time units are displayed with two digits (e.g., 05 instead of 5).

startStop() Function:

Checks the isRunning flag.

If running (true), it calls clearInterval(timer) to pause, updates the button text to "Start," and swaps the button's color class (stop-btn to start-btn).

If stopped (false), it calls setInterval(stopwatch, 1000) to begin the counting, updates the button text to "Stop," and swaps the button's color class (start-btn to stop-btn).

resetStopwatch() Function:

Clears the interval, resets the time variables to 0, updates the display to 00:00:00, and ensures the button text is set back to "Start."

💻 Tech Stack
HTML5

CSS3 (Inline)

Vanilla JavaScript (ES6+)
