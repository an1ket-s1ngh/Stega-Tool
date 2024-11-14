# Multi-Format Data Concealment Tool using Steganography

This tool provides a multi-format steganography solution, allowing you to conceal text data within text, audio, and video files. It leverages various techniques like LSB encoding, Zero-Width Characters (ZWC), and RC4 stream cipher for encryption.

## Features

* **Text Steganography:**
    * Encodes secret text messages within a cover text file using Zero-Width Characters (ZWC).
    * Decodes hidden messages from stego text files.
* **Audio Steganography:**
    * Encodes secret messages into an audio file using Least Significant Bit (LSB) encoding.
    * Decodes hidden messages from stego audio files.
* **Video Steganography:**
    * Encodes secret messages into a specific frame of a video file using LSB encoding and RC4 encryption.
    * Decodes hidden messages from the specified frame of a stego video file.

## Usage

1. **Clone the repository:**

   ```bash
   git clone https://github.com/an1ket-s1ngh/Stega-Tool

2. **Navigate to the project directory:**

   ```bash
   cd multi-format-steganography
   ```

3. **Run the tool:**

   ```bash
    python Steganography.py
   ```



Follow the on-screen menu to choose the desired steganography operation and format.

**Sample Cover Files**
The "Sample_cover_files" directory contains sample cover files for each format:

cover_text.txt
cover_audio.wav
cover_video.mp4
You can replace these with your own files.

# Code Overview
## Text Steganography
Encoding:
Converts the secret message to binary.
Applies transformations (XOR with 170) and adds identifiers.
Embeds the binary data into the cover text file using ZWC.
Decoding:
Extracts the ZWC characters from the stego text file.
Reverses the transformations to retrieve the original message.
## Audio Steganography
Encoding:
Reads the audio file and converts it to a byte array.
Converts the secret message to binary.
Embeds the binary data into the least significant bits of the audio data.
Decoding:
Extracts the least significant bits from the stego audio file.
Converts the binary data back to the original message.
## Video Steganography
Encoding:
Reads the video file and selects a specific frame for embedding.
Encrypts the secret message using RC4.
Converts the encrypted message to binary.
Embeds the binary data into the least significant bits of the frame's pixel data.
Decoding:
Extracts the least significant bits from the specified frame of the stego video file.
Converts the binary data back to the encrypted message.
Decrypts the message using RC4 to retrieve the original message.

## Dependencies
Python 3
NumPy
OpenCV
Matplotlib
Wave

## Note
This tool is for educational and research purposes only.
The authors are not responsible for any misuse of this tool.
The effectiveness of steganography depends on the cover file and the amount of data hidden.
