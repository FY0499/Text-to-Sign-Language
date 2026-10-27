# Sign Language Video Generator

A Python prototype for assembling sign-language video clips from text. The `SignLanguageVideoGenerator` class loads a sign dictionary, normalizes input, uses synonym and fuzzy matching, and combines available clips with MoviePy.

> Despite the repository name `TTS`, the main class in `TTS.py` is a **sign-language video generator**, not a conventional text-to-speech engine.

## The problem it explores

A text-to-sign resource can help people find visual sign equivalents for supported words and phrases. This project explores building a sign-language video sequence from existing clips and a dictionary.

## Main features

- Loads a JSON dictionary mapping text to sign resources.
- Normalizes text and supports Arabic synonyms and approximate matching.
- Processes and concatenates video clips using MoviePy.
- Uses concurrent-processing utilities for some operations.

## Demo

A verified generated-video demo is not included yet. Once tested, add a short sample video or GIF showing a supported input phrase and the resulting clip sequence.

Suggested location: `assets/demo.gif` or `assets/demo.mp4`.

## Repository contents

- [TTS.py](./TTS.py) — main implementation.
- [signs_dictionary.json](./signs_dictionary.json) — sign dictionary.
- [requirements.txt](./requirements.txt) — dependencies.
- [signs/](./signs/) — sign video assets.

## Tech stack

Python · JSON · MoviePy · SpeechRecognition · difflib · concurrent.futures

## Setup

Use a Python version compatible with the pinned dependencies.

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
# source .venv/bin/activate

pip install -r requirements.txt
```

## Run

`python TTS.py` currently loads the class definition but does not provide a complete command-line workflow. To run it, create a small script that imports `SignLanguageVideoGenerator`, initializes it with the path to `signs_dictionary.json`, and calls the appropriate public method for a phrase. Check the class methods in [TTS.py](./TTS.py) and make sure the dictionary's referenced video files are present before testing.

## Limitations and licensing

- Output depends on the available sign clips and dictionary coverage; missing signs may prevent a phrase from being represented.
- Review timing and continuity of generated clips.
- Only publish sign videos you have permission to redistribute.

## Roadmap

- [ ] Add a minimal tested example script with a sample phrase.
- [ ] Include a short real output video/GIF.
- [ ] Document the dictionary schema and how to add a sign clip.
- [ ] Add tests for normalization, synonyms, and missing-sign behavior.
- [ ] Review dependency compatibility and document a supported Python version.
