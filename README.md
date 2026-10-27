# Text-to-Sign-Language
A Python prototype that assembles sign-language video clips from text using a sign dictionary and MoviePy. It normalizes input text, attempts synonym and fuzzy matching, and combines available clips into a sequence.

> **Naming note:** Although the repository is named `TTS`, the main class is a sign-language video generator rather than a conventional text-to-speech engine.



https://github.com/user-attachments/assets/e6997df8-568c-45ae-96d3-a3386a53d779



## Problem it addresses

People may need a visual sign-language representation of supported words or phrases. This project explores turning text into a sequence of existing sign clips, using a dictionary to connect words with video resources.

## Features

- Loads a JSON dictionary mapping text to sign resources.
- Normalizes text and supports Arabic synonyms and approximate matching.
- Combines video clips with MoviePy.
- Includes concurrency utilities for selected operations.

## Demo

A verified generated-video demo is not currently included. After testing a supported phrase, add a real GIF or short video under `assets/demo.gif` or `assets/demo.mp4` and embed it here.

## Technologies

Python, JSON, MoviePy, SpeechRecognition, `difflib`, and `concurrent.futures`. See [requirements.txt](./requirements.txt) for dependencies.

## Repository contents

- [TTS.py](./TTS.py) — main implementation.
- [signs_dictionary.json](./signs_dictionary.json) — text-to-sign resource mapping.
- [signs/](./signs/) — sign video assets.
- [requirements.txt](./requirements.txt) — Python dependencies.

## Installation

```bash
git clone https://github.com/FY0499/TTS.git
cd TTS
python -m venv .venv
```

Windows:
```powershell
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

macOS/Linux:
```bash
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage status

The current `TTS.py` file defines the generator class but does not provide a complete command-line workflow. Therefore, `python TTS.py` is not a complete end-user demo.

To use the class, inspect its public methods in [TTS.py](./TTS.py), initialize it with the path to `signs_dictionary.json`, and call the relevant method for a phrase. Verify that every referenced video file exists before testing. A standalone example script should be added and tested before the project is presented as directly runnable.

## Limitations and licensing

- Output depends on dictionary coverage and the sign clips available.
- Clip timing and continuity should be reviewed.
- Only publish sign-language videos you have permission to redistribute.

## Future improvements

- Add a minimal tested example script.
- Include a real output video/GIF.
- Document the dictionary schema and how to add clips.
- Add tests for normalization, synonyms, and missing signs.
- Document a supported Python version and dependency compatibility.
