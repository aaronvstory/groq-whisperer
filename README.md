# Groq Whisperer: Voice-to-Text Transcription Tool

**Groq Whisperer** is a Python-based application that allows users to record audio and transcribe it to text using Groq's Whisper implementation. The transcribed text is automatically copied to the clipboard for easy pasting into other applications.

Create a real-time speech-to-text transcription React application using Next.js and Groq's Whisper API. The application must:

1. Visualize a live audio waveform.
2. Include a "Start/Stop" button to control transcription, a customizable keyboard shortcut to start, and an option to automatically end transcription after a period of silence.
3. Display the transcribed text in a scrollable text area that updates in real time.
4. Implement error handling for the Groq API and display any errors to the user.
5. Use Vite for project setup and development.

Assume the Groq API key is stored in a `.env` file. The interface must be responsive and visually appealing, with clear user feedback.


## Features

- Record audio by holding down the **PAUSE** key
- Transcribe recorded audio to text using Groq's API
- Automatically copy transcription to clipboard
- Continuous operation for multiple recordings

## Prerequisites

- Python 3.7 or higher
- A Groq API key (set as an environment variable)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/KennyVaneetvelde/groq_whisperer
   cd whisperer
   ```

2. Create a virtual environment:
   ```
   python -m venv venv
   ```
[System.Environment]::SetEnvironmentVariable("GROQ_API_KEY", "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", "User")
3. Activate the virtual environment:
   - On Windows:
     ```
     venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```
     source venv/bin/activate
     ```

4. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

5. Set up your Groq API key as an environment variable:
   - On Windows:
     ```
     setx GROQ_API_KEY "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"
     ```
   - On macOS and Linux:
     ```
     export GROQ_API_KEY="your-api-key-here"
     ```

## Usage

1. Run the script:
   ```
   python main.py
   ```

2. Press and hold the PAUSE key to start recording.
3. Release the PAUSE key to stop recording and start transcription.
4. The transcribed text will be automatically copied to your clipboard.
5. Repeat steps 2-4 for additional recordings.

## Dependencies

The project relies on the following main libraries:

- `pyaudio`: For audio recording
- `keyboard`: For detecting key presses
- `pyautogui` and `pyperclip`: For clipboard operations
- `groq`: For interacting with the Groq API

For a complete list of dependencies, see the `requirements.txt` file.

## Notes

- Make sure your microphone is properly configured and working before running the script.
- The transcription quality may vary depending on the audio quality and background noise.
- Ensure you have a stable internet connection for the transcription process.

## License

[MIT License](LICENSE)
