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

2. **Feature engineering**

Data derived from publicly available libraries such as RdKit and MorganDescriptors Fingerprint, along with suitable/associted chemical properties are taken into consideration for feature engineering. All possible combinations feature selection is listed below: 

<img width="1274" height="583" alt="image" src="https://github.com/user-attachments/assets/3cd64bf7-99cb-4eff-bf58-f75017e98f69" />

  ***Data normalization techniques***
  
  Descriptors values tends to vary in nature. Hence different normalization technique applied for each dataset based on its unique statistic distribution

  | Properties | Normalization Technique | Justification |
  | ---------- | ----------------------- | ------------- |
  | MolWt, MolLogP, TPSA, FractionCSP3 | Robust Scaling | skewed distribution,  and ahaving outliers |
  | NumHDonors | Binary Transform | Sparse count data where presence/absence is taken into consideration |
  | NumHAcceptors, NumRotatableBonds, NumAromaticRings, NumAliphaticRings | One-hot | low cardinal count data |
  | HeavyAtomCount | Z-Score | values clustered around the center |

   ***Other considerations:***
   1. Ligand Synergy Index (LSI)
   2. Chemical Diversity Score (CDS)
      CDS = 1 - avg(similarity)
   4. Applicability Confidence Score (ACS)

3. **Model building**

A comprehensive list of supervised ML techniques used for modeling. Listed below:

| ML Techniques | Advantage | Code available (Yes/No) |
| ------------- | --------- | ----------------------- |
| Linear Regression | Baseline model, helping to interpret feature importance | No |
| Ridge Regression | x | No |
| Lasso Regression | x | No |
| Elastic Net | Best for small data | No |
| Support Vector Regression | Good for non-linear QSAR | No |
| K-Nearest Neighbor | Good in similarity | No |
| Random Forest | x | No |
| XGBoost | x | No |
| LightGBM | x | No |
| Gaussian Process Regression | For uncertainty estimatation | No |
| Multilayer perception | use only if heavy regularization | No |
| GNN using DeepChem | Message passing networks | No |

4. **Model screening**

Best perfoming model is chosoen based on multiple dependant results as tablulated below:

| Feature variation | Model | R2(CV) | RMSE | MAE | Std. Dev | Rank |
| ----------------- | ----- | ------ | ---- | --- | -------- | ---- |

   Selection logic is:
   1. Remove models with Low R2
   2. Remove models with high Variance
   3. Consistent across n-Folds
   4. External test-set
   5. Y-Randomization
   6. Top-K Ranking accuracy

5. **Generate Virtual compounds**

While generating virtual checmical compounds, conventional permutations/combination may give deviations, untrusted, non-synthesizable inputs. Considerations to overcome:
   1. Scaffaold based generation
   2. Library based expansion
   3. Fragmented recombination

6. **Predict pIC50**

Apply best performing model and derive results

7. **Screen potential candidates**

   Refer:
   1. Drug likeliness rules
   2. ADMET Filtering
   3. Synthetic Fesibility
   
8. **Synthesis**

Lab experiments, and recently updated reasarch articles

## B. Best performing Models and Results

## C. How to use this repository

## D. License

## E. Contact

[@mhn-research](https://github.com/mhn-research)
