# Grammar_Scoring_Engine_for_spoken_data_samples #

This repository contains my submission for the SHL Intern Hiring Assessment, where the goal is to predict the grammar correctness of spoken audio clips.

📌 Problem Statement
Given a dataset of audio files and labels representing the quality of grammar used in speech, the task is to:

Transcribe the audio files

Estimate the grammar correctness of the transcribed text

Train a model to predict the grammar score (label) based on the transcription

🛠️ Approach
1. Audio Transcription
Used OpenAI's whisper model (base) to transcribe audio to text.

2. Grammar Scoring
Used a transformers-based grammar checking model (textattack/bert-base-uncased-CoLA) to estimate grammar score.

Normalized the grammar scores to a 0–5 range.

3. Model Training
Trained a RandomForestRegressor on the training data using only the grammar score as a feature.

Evaluated model performance using Mean Squared Error (MSE).

4. Prediction
Applied the model to the test set to generate predicted labels.

Saved the results in the required submission format.

🧪 Results
The final submission CSV contains 195 rows (one for each test audio).

Model performance was validated on the training set.

🗃️ Files in this Repo
File	Description
notebook.ipynb	Main Jupyter Notebook with full pipeline
my_submission.csv	Submission file with predictions
README.md	This readme file
dataset/	Folder containing train/test audio and CSVs (if not large)
shl-intern-hiring-assessment.zip	Final zipped submission (if needed)

🚀 How to Run

# 1. Clone the repository
git clone https://github.com/your-username/shl-intern-hiring-assessment.git
cd shl-intern-hiring-assessment

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
jupyter notebook notebook.ipynb

🧠 Model Used

Whisper (OpenAI) – for speech-to-text

BERT (CoLA) – for grammar checking

Random Forest – for final prediction

👤 Author
Jonnadula Saikiran
[GitHub] (https://github.com/saikiran6789)
