# AsciiArt
Mengonversi gambar ke seni ASCII menggunakan OpenCV.

## Usage:
    python3 ascii_art.py input.jpg
    python3 ascii_art.py input.jpg --width 120
    python3 ascii_art.py input.jpg --width 120 --color --output out.txt
    python3 ascii_art.py input.jpg --html out.html   # colored HTML output
 
## Core idea:
    1. Load image with cv2.
    2. Resize to fit target width, correcting for the fact that terminal
       characters are roughly twice as tall as they are wide.
    3. Convert to grayscale to get a brightness value per "cell".
    4. Map each brightness value to a character from a ramp that goes
       from "dense/dark" to "sparse/light" (or vice versa).
    5. Optionally keep the average color of each cell for colored output.
