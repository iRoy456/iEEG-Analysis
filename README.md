# iEEG-Analysis

## Neural Dissociation of Speech and Music Processing
This repository contains the code and analysis pipeline for investigating the spectral and temporal dynamics of auditory processing using human intracranial EEG (iEEG) data. The project analyzes the Film Music Dataset (ds003688) to demonstrate a spectral double dissociation: speech perception is driven by high-gamma activity, while music perception recruits theta and alpha rhythms.
## Project Overview
The analysis explores how the human auditory cortex parses complex acoustic streams by matching its integration windows to the temporal statistics of the stimulus (Speech vs. Music). The pipeline covers raw data preprocessing, stationary spectral analysis, and dynamic time-frequency representations.

## Analysis Pipeline
#### Preprocessing:
- Artifact rejection and removal of noisy/flat-lining channels.
- 50 Hz line noise attenuation using a Blackman-windowed FIR Notch filter.
- Spatial re-referencing using a Common Average Reference (CAR).
- Standardization of variable sampling rates across subjects.
#### Spectral Analysis (PSD):
- Computation of Power Spectral Density using Welch's method.
- Isolation of true oscillatory peaks via 1/f aperiodic background normalization.
- Generation of individual and group-averaged PSD comparisons.
#### Time-Frequency Dynamics:
- Computation of Time-Frequency Representations (TFRs) using Morlet wavelets.
- Baseline correction using pre-task resting-state epochs to isolate stimulus-evoked responses.
- Statistical validation using permutation t-tests with False Discovery Rate (FDR) correction ($p < 0.05$).

## Tech StackLanguage: 
Python 3.x
Core Libraries: mne-python, numpy, scipy, matplotlib
