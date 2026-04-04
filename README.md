# PyridineQSAR

This repository is supporting Quantitative Structure-Activity relationship (QSAR) for Pyridine compounds. Quantitative Structure-Activity Relationship (QSAR) is a computational modeling method used in chemistry, pharmacology, and toxicology to predict the biological activity or property of a compound based on its molecular structure.

Following diagram demonstrates end-to-end approach that we implemented for predicting **pIC50** of [XYZ]

<img width="654" height="287" alt="image" src="https://github.com/user-attachments/assets/e3dcc048-82e4-4f4e-8a63-ab2c37e7f935" />


1. **Preparation**

From literature and research article, pIC50 values and other properties were extracted.

S.No	L1	L2	L3	charge	Incubation Time (hours)	Cell Lines	IC50	pIC50
1	c1ccnc(c1)c1nc(ccc1)c1ncccc1	C1(=NC=CC=C1)C2=CC=CC=N2		2	72 h	A2780	0.89	6.05
2	c1ccnc(c1)c1nc(ccc1)c1ncccc1	C1(=NC=CC=C1)C2=CC=CC=N2		2	72 h	A2780cisR	2.05	5.69
<img width="649" height="61" alt="image" src="https://github.com/user-attachments/assets/a165de5b-59aa-475e-8a3e-e082294ed8f2" />
   
3. **Feature engineering**
4. **Model building**
5. **Model screening**
6. **Generate Virtual compounds**
7. **Predict pIC50**
8. **Screen potential candidates**
9. **Synthesis**
