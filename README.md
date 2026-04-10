# Mini Project 3: Beyond the Joke
**INFO 230 | Spring 2026**

---

## Overview

How do US political and COVID memes differ in how they assign blame, victimhood, and heroism. Do visual, textual, and acoustic features reinforce those framings? This project applies a full multimodal cultural analytics pipeline across three datasets and eight steps of analysis to find out.

For the full analysis, results, discussion, and interpretations see **`code/project-workflow.ipynb`**.

---

## Datasets

| Source | Description |
|---|---|
| [Memes Images: OCR Data](https://www.kaggle.com/datasets/yogesh239/text-data-ocr) (Kaggle, yogesh239) | 5,552 political and COVID memes with OCR text and entity tags (hero, villain, victim) + 16 sample PNG images |
| [2020 US Presidential Election Campaign Speeches](https://doi.org/10.1038/s41597-025-04681-x) (Chalkiadakis et al., 2025) | 1,081 cleaned campaign speeches from Trump, Biden, Pence, and Harris (Jan 2019 to Jan 2021) |
| [M-Arg Multimodal Argumentation Dataset](https://aclanthology.org/2021.argmining-1.8/) (Mestre et al., 2021) | 17 MP3 audio clips from the 5 US 2020 presidential debates with force-aligned utterance timestamps |

---

## Repo Structure
```
cultural-analytics-project-3/
├── code/
│   ├── project-workflow.ipynb       <- full analysis lives here
│   └── environment.yaml             <- conda environment
├── data/
│   ├── audio_data/                  <- M-Arg debate audio dataset
│   │   ├── files_explanation.md
│   │   ├── M-arg_preprocessing.py
│   │   └── data/
│   │       ├── split audio/         <- 17 MP3 debate clips
│   │       ├── timestamps/          <- force-aligned utterance timestamps
│   │       └── tokenised text/      <- speaker-labeled transcripts
│   ├── data_clean/                  <- 2020 campaign speech TSVs
│   ├── SampleImagesData/
│   │   └── SampleImagesData/
│   │       ├── covidMemes/          <- 8 COVID meme PNGs
│   │       └── usPoliticsMemes/     <- 8 US Politics meme PNGs
│   ├── text_with_ocr.csv            <- meme training set (5,552 rows)
│   └── validation_data.csv          <- meme validation set (650 rows)
├── README.md
└── index.html
```
---

## How to Run

1. Clone the repo
2. Create and activate the conda environment: `conda env create -f code/environment.yaml`
3. Install librosa separately: `pip install librosa`
4. Run `code/project-workflow.ipynb` top to bottom

---

## Dependencies
pandas, numpy, nltk, scikit-learn, plotly, matplotlib,
wordcloud, Pillow, opencv-python, librosa

```bash
conda env create -f code/environment.yaml
pip install librosa
```

---

## Course Context

Mini Project 3 (INFO 230: Cultural Analytics, Spring 2026)

By Maddie MacDonald | UC Berkeley Statistics, MA