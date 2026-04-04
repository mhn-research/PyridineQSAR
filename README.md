# PyridineQSAR

This repository is supporting Quantitative Structure-Activity relationship (QSAR) for Pyridine compounds. Quantitative Structure-Activity Relationship (QSAR) is a computational modeling method used in chemistry, pharmacology, and toxicology to predict the biological activity or property of a compound based on its molecular structure.

Following diagram demonstrates end-to-end approach that we implemented for predicting **pIC50** of [XYZ]

<img width="654" height="287" alt="image" src="https://github.com/user-attachments/assets/e3dcc048-82e4-4f4e-8a63-ab2c37e7f935" />


## Describing the approach adopted during various phases

1. **Preparation**


From literature and research article, pIC50 values and other properties were extracted. Example data given as below:

| Ligand 1     | Ligand 2                          | Ligand 3 | Charge | Incubation Time | Cell Lines | IC50 | pIC50
| ----------- | ------------------------------------ | ---------- | -------- | ------------ | ---- | --- | --- |
| c1ccnc(c1)c1nc(ccc1)c1ncccc1 | C1(=C(C(=O)c2c(C1=O)cccc2)CC=C(C)C)O           | [H]O[H] | 1 | 24h | A2780 | 7.1 | 5.15
 
3. **Feature engineering**
4. **Model building**
5. **Model screening**
6. **Generate Virtual compounds**
7. **Predict pIC50**
8. **Screen potential candidates**
9. **Synthesis**
