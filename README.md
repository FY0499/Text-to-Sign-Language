# Sign Language Video Generator

A Python utility for assembling sign-language video clips from text. The `SignLanguageVideoGenerator` class loads a sign dictionary, normalizes text, uses synonym and fuzzy matching, and relies on video-processing utilities to combine clips.

> Despite the repository name `TTS`, the main class in `TTS.py` is a sign-language video generator rather than a conventional text-to-speech engine.

## Key capabilities
- Load a JSON dictionary mapping text to sign resources.
- Normalize and match Arabic text, including synonyms and approximate matches.
- Process and concatenate video clips using MoviePy.
- Use concurrent processing utilities to support responsive operations.

## Repository contents
- [TTS.py](./TTS.py) — main implementation.
- [signs_dictionary.json](./signs_dictionary.json) — sign dictionary.
- [requirements.txt](./requirements.txt) — Python dependencies.
- [signs/](./signs/) — sign video assets.

## Setup
1. Use a Python version compatible with the pinned dependencies.
2. Create and activate a virtual environment.
3. Install dependencies: `pip install -r requirements.txt`
4. Keep `signs_dictionary.json` and the referenced video files in the expected locations.
5. Review the class constructor and expected dictionary structure in [TTS.py](./TTS.py), then create a small test using a phrase covered by your dictionary.

## Limitations
The generated result depends on the available sign clips and dictionary coverage. A phrase may not be representable if required signs are missing. Review the output clips for timing and continuity.

## Security and licensing
Only include sign videos that you have permission to redistribute. Do not add private recordings or identifiable personal data without appropriate consent.

## Project status
Core implementation and assets are present. Confirm dependency compatibility and test clip generation in your own environment before relying on it.
