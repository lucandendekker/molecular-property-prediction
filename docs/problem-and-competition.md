# Problem and competition context

## Research motivation

The brief describes the need to find suitable organic molecules for photovoltaic applications. Experimental synthesis, energy-level measurement and stability testing are resource-intensive. Structure-based prediction is a way to narrow a candidate list before further experiments, rather than replace those experiments.

The broader assignment covered three kinds of machine learning: HOMO/LUMO regression, stability classification and clustering. This portfolio entry presents the problem, the approach and both Kaggle competition results; the included notebooks cover the energy-level regression pipelines.

## What was supplied

The molecular structures originate from the public Harvard Organic Photovoltaic Dataset (HOPV15, Lopez et al., 2016, *Scientific Data* 3, 160086). For the course, the lecturers simulated the HOMO, LUMO and stability target values. The task also used additional records accessed through a PostgreSQL database and a Kaggle test set of 200 molecules. Some molecular structures overlap between the source datasets, making deduplication and consistent preparation important.

The simulated targets are not the publicly available HOMO/LUMO values for the same structures, and they are not published here. Neither are the course datasets, the database's connection details or any extracts.

## What was submitted

For regression, the task required a training pipeline, an inference pipeline accepting molecular SMILES and a submission containing HOMO/LUMO predictions in the expected CSV format. The private leaderboard MAE was the assessment criterion, with a stated client target below 0.1.

## Recorded evidence

The private-leaderboard screenshots show two separate competition results for Lucan den Dekker:

| Competition | Final rank | Private score |
|---|---:|---|
| Energy Level Prediction (HOMO/LUMO) | **6th** | **MAE 0.0704** |
| Molecular Stability Prediction | **13th** | **Macro F1 0.5907** |

The classification task description identifies macro F1 as its metric. No total participant count, public-leaderboard score or separate private score for each orbital is inferred.

## What the result means

The energy-level score is below the task's 0.1 MAE threshold. The stability result uses a different metric and should not be compared numerically with the regression MAE. Both describe educational benchmarks on simulated targets, not laboratory accuracy, full OPV device performance or generalisation to arbitrary molecular structures.

## Public scope

This repository contains the project case study and three notebooks with my own training and inference code, with all outputs cleared. Trained models, training and competition datasets, school database access details and competition submissions are excluded, so that the simulated target values cannot be recovered from this repository.
