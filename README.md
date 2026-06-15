# Aadhar-Facevoting-system

A Python-based prototype for biometric voting using face recognition.

This project captures face images through a webcam, trains a simple KNN-based face recognizer, and allows registered voters to cast a vote once while recording the selection in a CSV file.

## Features

- Capture face samples and register users with `add_faces.py`
- Recognize a voter in real time with `give_vote.py`
- Prevent duplicate voting by checking recorded votes
- Log the vote with party choice, date, and time in `Votes.csv`
- Audio feedback using Windows SAPI

## Files

- `add_faces.py`: Captures face images and stores face data in `data/faces_data.pkl` and labels in `data/names.pkl`
- `give_vote.py`: Loads the stored face dataset, recognizes the user, lets them vote for a party, and writes the vote record to `Votes.csv`
- `background.png`: Background image used during the voting display
- `data/`: Folder where generated face data and labels are stored
- `.venv/`: Local virtual environment (ignored by Git)
- `.idea/`: IDE settings folder (ignored by Git)

## Requirements

- Python 3.8+
- `opencv-python`
- `numpy`
- `scikit-learn`
- `pywin32`

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Usage

1. Run `add_faces.py` and enter your Aadhaar number when prompted.
2. Follow the webcam display until sample capture completes.
3. Run `give_vote.py` and allow the app to detect your face.
4. Press:
   - `1` for BJP
   - `2` for CONGRESS
   - `3` for AAP
   - `4` for NOTA

## Notes

- The project depends on a webcam and Windows speech support.
- The `data/` folder is created automatically if needed.
- `Votes.csv` is generated when a vote is recorded.
