# Fake News Classification — ML Project

This repository contains a Jupyter notebook that implements a classical machine-learning baseline for fake news detection using the WELFake dataset. The notebook trains and compares Multinomial Naive Bayes and Logistic Regression on TF-IDF features.

## Repository contents
- `fake_news_classification.ipynb` — step-by-step notebook (data loading, preprocessing, feature extraction, training, evaluation).
- `fake-news-notebook-outline.md` — original outline used to design the notebook.
- `requirements.txt` — Python dependencies for quick setup.
- `.gitignore` — excludes the large dataset file from the repo.

## Dataset
The WELFake dataset is not included in this repository due to its size. Download it from:

https://drive.google.com/file/d/1hlOyDpC8g5jgbtPQq1TNcRFzIojxUauf/view?usp=sharing

After downloading, place the file in the project root and name it exactly:

`WELFake_Dataset.csv`

(Alternatively, see the Git LFS section if you want to version the dataset in the repo.)

## Quick setup (Windows PowerShell)
1. Create & activate a virtual environment

```powershell
python -m venv .venv
.\.venv\Scripts\Activate
```

2. Install dependencies

```powershell
pip install --upgrade pip
pip install -r requirements.txt
```

3. (Optional) If you want to programmatically download the dataset from Google Drive, install `gdown` and run:

```powershell
pip install gdown
# Use the Google Drive file id to download
gdown "https://drive.google.com/uc?id=1hlOyDpC8g5jgbtPQq1TNcRFzIojxUauf" -O WELFake_Dataset.csv
```

Note: Google Drive may require manual confirmation for some large files — if the `gdown` method fails, download manually through the link and place the file as described above.

4. Open the notebook

```powershell
jupyter notebook fake_news_classification.ipynb
# or
jupyter lab
```

Run cells from top to bottom. If you encounter an error about missing NLTK data, run the following in Python once:

```python
import nltk
nltk.download('punkt')
```

## Using Git LFS (optional)
If you'd like to store `WELFake_Dataset.csv` in the repository, use Git Large File Storage (LFS). Example steps:

```powershell
# Install git-lfs if not present, then:
git lfs install
# Track the file
git lfs track "WELFake_Dataset.csv"
# Commit the .gitattributes file that git-lfs creates, then add the dataset and push
git add .gitattributes
git add WELFake_Dataset.csv
git commit -m "Add dataset via Git LFS"
git push origin main
```

## Notes
- `.gitignore` already excludes `WELFake_Dataset.csv` to avoid accidentally committing a very large file.
- The notebook uses `sklearn`'s English stop words and NLTK's Porter stemmer. The `requirements.txt` includes the packages used.

## Recommended next steps
- Run the notebook and inspect metrics. Try hyperparameter tuning (GridSearchCV) and additional models (SVM, ensembles, or transformers) if you want improved performance.
- Add a small `data/` README or a download script to automate dataset setup for collaborators.

## Contact
If you want me to add a README badge, CI, or a small example script to run the notebook headlessly, tell me which option you prefer and I will add it.
