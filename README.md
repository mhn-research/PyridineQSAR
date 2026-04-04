# CuPyridineQSAR

This repository is supporting work used to derive Quantitative Structure-Activity relationship (QSAR) for Copper-Pyridine complexes. Quantitative Structure-Activity Relationship (QSAR) is a computational modeling method used in chemistry, pharmacology, and toxicology to predict the biological activity or property of a compound based on its molecular structure. This repository contains information about feature selection, model building, chosing best performing models, predicting pIC50 values along with confidence score.

Following diagram demonstrates end-to-end approach that we implemented for predicting **pIC50** value for unknown Copper-Pyridine Complexes.

<img width="1309" height="568" alt="image" src="https://github.com/user-attachments/assets/c331b932-4345-4ed3-9df3-be22f3c00f5e" />

## A. Describing the approach adopted during various phases

1. **Preparation**


From literature and research article, pIC50 values and other properties were extracted. curated raw data found in data folder. Example  inputs given in below table:

| Ligand 1     | Ligand 2 | Charge | Incubation Time | Cell Lines | IC50 | pIC50
| ----------- | ---------- | -------- | ------------ | ---- | --- | --- |
| c1ccnc(c1)c1nc(ccc1)c1ncccc1 | [H]O[H] | 1 | 24h | A2780 | 7.1 | 5.15

3. **Feature engineering**
4. **Model building**
5. **Model screening**
6. **Generate Virtual compounds**
7. **Predict pIC50**
8. **Screen potential candidates**
9. **Synthesis**

## B. Repository strcuture

## C. Models and Results

## D. How to use this repository

## E. License

## F. Contact

[@mhn-research](https://github.com/mhn-research)
