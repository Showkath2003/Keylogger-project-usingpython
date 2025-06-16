Keylogger
A simple keylogger implemented in Python using the pynput library to capture keyboard input and log it to a file (log.txt).
Features

Captures keyboard input, including letters, numbers, and special keys.
Converts specific key events (e.g., space, enter) into readable characters.
Ignores certain keys (e.g., Shift, Ctrl) to avoid clutter in the log.
Appends all captured input to log.txt in the project directory.
Uses the with statement to ensure proper resource management and memory cleanup.

Prerequisites

Python 3.x
pynput library


Navigate to the project directory:cd keylogger


Install the required package:pip install pynput



Usage

Run the script:python keylogger.py


The program will start capturing keyboard input and saving it to log.txt.
To stop the program, press Ctrl+C or terminate the process.
Check the log.txt file in the project directory to view the captured input.

Code Explanation

The script uses the pynput.keyboard.Listener to listen for keyboard events.
The write_to_file function processes each key press:
Converts special keys (e.g., Key.space to a space, Key.enter to a newline).
Ignores modifier keys like Shift and Ctrl.
Appends the processed key to log.txt.


The with statement ensures the listener is properly closed, releasing system resources.

Example Output
If you type Hello World! and press Enter, log.txt will contain:
Hello World!

Notes

This project is for educational purposes only. Using a keylogger to capture input without consent is unethical and may be illegal.
The script appends to log.txt each time it runs. To start fresh, delete or rename the existing log.txt file.
Ensure you have write permissions in the directory where log.txt is created.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Disclaimer
Use this software responsibly. The author is not responsible for any misuse or damage caused by this program.
