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
| [2020 US Presidential Election Campaign Speeches](https://doi.org/10.5281/zenodo.14785782) (Chalkiadakis et al., 2025) | 1,081 cleaned campaign speeches from Trump, Biden, Pence, and Harris (Jan 2019 to Jan 2021) |
| [M-Arg Multimodal Argumentation Dataset](https://zenodo.org/records/5653504) (Mestre et al., 2021) | 17 MP3 audio clips from the 5 US 2020 presidential debates with force-aligned utterance timestamps |

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
2. Create and activate the conda environment: 
```bash
conda env create -f environment.yaml
conda activate cultural_analytics
```
3. Run `code/project-workflow.ipynb` top to bottom

---

## Environment
All dependencies are managed via `environment.yaml` using the `cultural_analytics` conda environment. Key packages include: `pandas`, `numpy`, `nltk`, `scikit-learn`, `plotly`, `matplotlib`, `Pillow`, `opencv-python`, `librosa`

---

## References

### Datasets

yogesh239. (2023). Memes Images: OCR Data. Kaggle. https://www.kaggle.com/datasets/yogesh239/text-data-ocr

Chalkiadakis, I., Angles d'Auriac, L., Peters, G.W., and Frau-Meigs, D. (2025). A text dataset of campaign speeches of the main tickets in the 2020 US presidential election. *Scientific Data*, 12, 662. https://doi.org/10.1038/s41597-025-04681-x | Dataset: https://doi.org/10.5281/zenodo.14785782

Mestre, R., Milicin, R., Middleton, S.E., Ryan, M., Zhu, J., and Norman, T.J. (2021). M-Arg: Multimodal Argument Mining Dataset for Political Debates with Audio and Transcripts. *Proceedings of the 8th Workshop on Argument Mining*, pp. 78-88. Association for Computational Linguistics. https://aclanthology.org/2021.argmining-1.8/ | Dataset: https://zenodo.org/records/5653504

### Methods and Tools

Chowdhury, J.H., Ramanna, S., and Kotecha, K. (2025). Speech emotion recognition with light weight deep neural ensemble model using hand crafted features. *Scientific Reports*, 15, 11824. https://doi.org/10.1038/s41598-025-95734-z

Hutto, C.J. and Gilbert, E.E. (2014). VADER: A Parsimonious Rule-Based Model for Sentiment Analysis of Social Media Text. *Proceedings of the 8th International AAAI Conference on Weblogs and Social Media (ICWSM-14)*. https://doi.org/10.1609/icwsm.v8i1.14550

McFee, B., Raffel, C., Liang, D., Ellis, D.P.W., McVicar, M., Battenberg, E., and Nieto, O. (2015). librosa: Audio and Music Signal Analysis in Python. *Proceedings of the 14th Python in Science Conference (SciPy 2015)*, pp. 18-24. https://doi.org/10.25080/majora-7b98e3ed-003

## AI Disclosure

Claude (Anthropic) was used as an AI assistant throughout this project for help with code structure, debugging, implementation decisions, and writing feedback. All code was read through, understood, and retyped manually. All analytical decisions, interpretations, and conclusions are my own. Claude helped, but the thinking was mine.

By Maddie MacDonald | UC Berkeley Statistics, MA