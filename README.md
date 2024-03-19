# Health Care Data Augmentation
As an undergraduate research student in Dr.Bennett’s Lab, I had to augment 15 imbalanced health care datasets.

### Tests
These are the tests that I have tried to augment the data
1) A modified version of SMOTE, where some extra “variation” is added to each created synthetic sample by using the standard deviation of each feature
2) Based on Augmentation_1, added one more parameter 'skew'
3) Used "gaussian" sampling instead of "uniform" sampling for std_dev (altering how "gap" is calculated)
4) When synthesizing new data, 70% of new data are synthesized from 3 data that are close to the centorid. Rest 30% of new data are synthesized from data that are far from centroid.
5) When synthesizing new data, 70% of new data are synthesized from 3 data that are far from centorid. Rest 30% of new data are synthesized from data that are close to centroid.
6) Calculate std_dev from only the nn array, rather than all data
7) Custom Ensemble: Created a different synthesized dataset for each tree in the ensemble, using slightly different parameters.
8) SMOTE-OUT: Alleviate the problem of SMOTE creating meaninglss synthetic examples in dense distribution
9) Use Generative Adversarial Network to synthesize data

## File Description
1) dataset.csv is the original dataset. For more simple analysis, I created merged.csv which is the dataset that is same as original, except for the absence of modality (unnecessary modalities except for 'Petting')
2) Overall result.csv has all the results of ACC, AUC in Augmentation 1-9
