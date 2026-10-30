# Text-to-Sign-Language

A system that helps people who communicate through sign language understand spoken or written messages. It accepts **typed text or audio**. When the input is audio, it first converts speech into text, then finds the matching signs and combines their video clips into one sign-language video.

## How it works

1. The user enters text or sends an audio recording.
2. Audio is converted into written text.
3. The system matches the words with entries in the sign dictionary, including supported synonyms.
4. The matching sign clips are combined into a video.

## Demo

https://github.com/user-attachments/assets/e6997df8-568c-45ae-96d3-a3386a53d779

## Features

- Accepts written text and audio input.
- Converts speech to text.
- Matches Arabic words and phrases using a sign dictionary, synonyms, and fuzzy matching.
- Combines the selected sign clips into a video.
- Can be connected to the Flutter app flow.

## Technologies

Python, MoviePy, SpeechRecognition, JSON, difflib, and concurrent.futures.

## Setup

```bash
git clone https://github.com/FY0499/Text-to-Sign-Language.git
cd Text-to-Sign-Language
python -m venv .venv
```

Install the project dependencies:

```bash
pip install -r requirements.txt
```

The main implementation is in [TTS.py](./TTS.py), and the sign video mapping is stored in [signs_dictionary.json](./signs_dictionary.json).
