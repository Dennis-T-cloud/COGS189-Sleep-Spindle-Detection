# COGS189-Sleep-Spindle-Detection
Automated pipeline for detecting Sleep Spindles in NREM sleep using the ds000201 dataset.

# Impact of Sleep Deprivation on Sleep Spindle Density

## dicussion area(delete this area when Prjoect completed):
    Team Update (Week 6):
    I've initialized our GitHub repository with the standard project structure and a modular README. Please clone the repo and run 

    pip install -r requirements.txt 

    in your local VS Code (Terminal). I've also uploaded a draft_pipeline.ipynb containing the initial signal processing logic (11-16 Hz band-pass filter).

* **Project Proposal**: [Google Doc Link](https://docs.google.com/document/d/1lLJhXjg3Ygftyn3R03wnejl5A9Q4btqbOSzXj6YAyFE/edit?usp=sharing)

## Data Acquisition Status (Updated)

    Metadata: participants.tsv and participants.json have been integrated for subjective rating analysis.

    EMG/Physio Data: Pre-processed via convert_physio_files.py from the sourcedata directory.

    Raw PSG Data: Access Request Pending. A formal request has been submitted to the Stockholm SleepyBrain Project lead (Dr. Gustav Nilsonne) to acquire raw EEG channels for high-fidelity spindle detection.

## 1. Project Overview
[cite_start]This project focuses on developing an **automated pipeline** to detect **Sleep Spindles** (11-16 Hz) during Non-Rapid Eye Movement (**NREM**) sleep[cite: 14]. [cite_start]By quantifying neurophysiological oscillations, we aim to establish a data-driven link between overnight EEG features and next-day subjective cognitive alertness.

## 2. Methodology & Data
* [cite_start]**Methodological Reference**: Adapted from *"Image Reconstruction from Electroencephalography using Latent Diffusion"* (Fei and de Sa, 2024), utilizing EEG encoding and linear mapping techniques[cite: 19, 20].
* [cite_start]**Primary Dataset**: **Stockholm SleepyBrain Project (ds000201)**, featuring a sleep-deprived cross-over design.
* **Scalability**: The pipeline is designed with a **Modular Data Loader** architecture to support future BIDS-compliant datasets beyond the primary OpenNeuro source.

## 3. Technical Pipeline

* [cite_start]**Signal Processing**: Band-pass filtering (11-16 Hz), artifact rejection for raw PSG data, and integration of EMG signals.
* [cite_start]**Automated Detection**: Linear mapping framework to identify spectral power of VEP-like components.
* [cite_start]**Statistical Analysis**: Pearson/Spearman correlation between spindle metrics (density, duration) and Subjective Sleepiness scales.

## 4. Repository Structure
```text
.
├── data/               # Dataset documentation & metadata (participants.tsv)
├── notebooks/          # Jupyter notebooks for exploratory analysis
│   └── draft_pipeline.ipynb
├── scripts/            # Modular Python scripts
│   ├── preprocessing.py # Filtering & Artifact rejection
│   └── detection.py     # Spindle identification algorithm
├── README.md           # Project documentation
└── requirements.txt    # Dependencies (mne, numpy, scipy, pandas)
```

## 5. Team & Roles (Overthinking)

    Dennis Sun: Lead for Data Acquisition and Algorithm Development.

    Evelyn Zhang: Algorithm Development & Signal Processing Pipeline.

    Qirui Zheng: Results Analysis & Correlation with Subjective Ratings.

    Yixuan Xin: Results Analysis & Results Discussion.

