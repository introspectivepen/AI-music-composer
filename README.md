AI Music Composer
The AI Music Composer is a Python-based application that uses natural language or emoji prompts to generate music using Meta's MusicGen model. The application maps emojis to descriptions, processes the input, and generates music based on the textual description or custom input provided by the user. It can then play the generated music directly in a notebook environment.

Features
Emoji-to-Description Mapping: Use emojis to describe moods or themes, and the application will generate music based on their associated descriptions.
Custom Text Input: Enter custom text prompts to generate music that matches your input.
Audio Playback: Directly play the generated music in your notebook.
GPU Acceleration: Automatically uses GPU if available for faster music generation.
Requirements
Python 3.8+
PyTorch (with CUDA support for GPU acceleration if executing in VScode or any other IDE)
Transformers library by Hugging Face
IPython for audio playback
Installation
Clone the repository or download the script.
Use Google colob or jupyter notebook fro the code execution.
Install the required Python packages:
pip install torch transformers ipython
Download the emoji_music_descriptions.csv file and place it in the same directory as the script.
Usage
Place the emoji_music_descriptions.csv file in the specified path.

This CSV file should contain two columns: Emoji(s) and Description.
Example:
Emoji(s),Description
🌞,Sunny and cheerful melody
🌊,Calm and relaxing ocean waves
Run the script:

python ai_music_composer.py
Input an emoji or custom text when prompted. For example:

Emoji: 🌞
Text: A relaxing tune for a quiet evening
Listen to the generated music directly in the notebook environment.

Code Structure
load_emoji_descriptions: Loads the emoji-to-description mappings from a CSV file.
generate_music: Generates music based on the input description using the MusicGen model.
play_audio: Plays the generated audio using IPython’s Audio class.
Main Script: Handles user input, maps it to a description, generates music, and plays it.
Example
Input:
Enter your emoji or text: 🌞
Output:
Generating music for: Sunny and cheerful melody
The application generates a cheerful melody and plays it in the notebook.

Notes
The MusicGen model generates music in waveform format. Ensure the output is compatible with the IPython.display.Audio class.
Use a GPU for faster processing, especially for larger prompts or more complex compositions.
Troubleshooting
Error: File not found:
Ensure the emoji_music_descriptions.csv file is in the correct path.
Audio not playing:
Check if audio_values is in the correct format (1D NumPy array).
Ensure the sampling rate is correctly configured.
Slow Performance:
Use a machine with a GPU for faster music generation.
Happy Reading :)
