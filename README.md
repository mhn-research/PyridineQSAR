# CuPyridineQSAR

This repository is supporting work used to derive Quantitative Structure-Activity relationship (QSAR) for Copper-Pyridine complexes. Quantitative Structure-Activity Relationship (QSAR) is a computational modeling method used in chemistry, pharmacology, and toxicology to predict the biological activity or property of a compound based on its molecular structure. This repository contains information about feature selection, model building, chosing best performing models, predicting pIC50 values along with confidence score.

Following diagram demonstrates end-to-end approach that we implemented for predicting **pIC50** value for unknown Copper-Pyridine Complexes.

<img width="1300" height="560" alt="image" src="https://github.com/user-attachments/assets/11ac2f07-5b5b-4c17-ac20-18abc81cb05e" />

## A. Describing the approach adopted during various phases

1. **Preparation**


From literature and research article, pIC50 values and other properties were extracted. curated raw data found in data folder. Example  inputs given in below table:

| Ligand 1     | Ligand 2 | Charge | Incubation Time | Cell Lines | IC50 | pIC50
| ----------- | ---------- | -------- | ------------ | ---- | --- | --- |
| c1ccnc(c1)c1nc(ccc1)c1ncccc1 | [H]O[H] | 1 | 24h | A2780 | 7.1 | 5.15

3. **Feature engineering**

Data derived from publicly available libraries such as RdKit and MorganDescriptors Fingerprint, along with suitable/associted chemical properties are taken into consideration for feature engineering. All possible combinations feature selection is listed below: 

<img width="1274" height="583" alt="image" src="https://github.com/user-attachments/assets/3cd64bf7-99cb-4eff-bf58-f75017e98f69" />


5. **Model building**
6. **Model screening**
7. **Generate Virtual compounds**
8. **Predict pIC50**
9. **Screen potential candidates**
10. **Synthesis**

## B. Best performing Models and Results

## C. How to use this repository

## D. License

## E. Contact

[@mhn-research](https://github.com/mhn-research)
