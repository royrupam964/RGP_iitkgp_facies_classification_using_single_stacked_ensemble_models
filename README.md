# RGP_iitkgp_facies_classification_using_single_stacked_ensemble_models
## Overview
This repository contains code for a complete machine-learning workflow for developing single and ensemble classifiers to predict coal, carbonaceous shale, and non-coal lithofacies from high-resolution well-log data. Single classifiers show limited accuracy in distinguishing carbonaceous facies; however, ensemble approaches—particularly stacked, heterogeneous, and selected homogeneous ensembles—demonstrate substantial improvements in both class-wise and overall performance. The workflow relies extensively on built-in objects and utilities from [scikit-learn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning), and several plotting routines are adapted from the works of [Brendon Hall](https://github.com/brendonhall/facies_classification/blob/master/Facies%20Classification%20-%20SVM.ipynb) and [Ryan A. Mardani](https://www.linkedin.com/in/amardani/).

**_Note_**: _The raw source files (Excel) used for training and testing are confidential and
 therefore omitted; their directory paths are replaced with underscores. For illustration,
 the DataFrame corresponding to one representative training well is provided to
 demonstrate the structure and naming of input and output columns. To execute the
 notebook successfully, users must replace the placeholder underscores with appropriate
 file paths pointing to datasets that share identical variable names for all required input
 and output features._

## Notebook Contents
A couple of Jupyter notebooks, namely, [Source code (Part-1): Data variability], and [Source code (Part-2): The main code], implement the following components of the workflow: 

_Part 1_
1. **Library Imports:** Loading all required Python libraries and auxiliary functions.
2. **Data Loading:** Importing training and blind-testing datasets as pandas DataFrames.
3. **Data variability analysis:** Dataset overview, variability analyses, and outlier detection.


_Part 2_
1. **Library Imports:** Loading all required Python libraries and auxiliary functions.
2. **Data Loading:** Importing training and blind-testing datasets as pandas DataFrames.
3. **Data Description and Preprocessing:** Dataset overview (excluding variability analyses in Part 1), correlation matrix, feature selection, and preprocessing routines.
4. **Model Development:** Single Classifiers Training six individual classifiers and generating their classification reports.
5. **Model Validation:** Validation using internal validation sets, followed by blind-well testing.
6. **Litholog Comparisons Plotting:** True vs. predicted lithofacies logs for each classifier.
7. **Descriptive Visualizations:** Generating bar plots and related figures presented in the manuscript.
8. **Evaluation Metrics:** Computing confusion matrices, ROC curves, Jaccard indices, and F1-scores.
9. **Stacked Ensemble Construction:** Building and evaluating a stacked ensemble classifier.
10. **Heterogeneous Ensemble Construction:** Developing and assessing a heterogeneous ensemble model.
11. **Homogeneous Ensemble Construction:** Building homogeneous ensembles for each base classifier.
12. **Application to Blind Wells:** Applying four trained homogeneous ensembles to two blind wells (Well-4 and Well-5).
13. **Model Performance Summary:** Comparative evaluation of all models using accuracy and F1-score metrics.
14. **Secondary Blind Dataset Evaluation:** Applying all models to a second blind dataset (without a true litholog) and evaluating using similarity matrices based on Cohen’s kappa and accuracy heat maps.

</details>

### Dependencies
Install all dependencies using:<br>
`pip install -r requirements.txt`

### Key libraries include:
* [scikit-learn](https://scikit-learn.org/stable/supervised_learning.html#supervised-learning)
* **numpy, pandas, matplotlib, seaborn**
* **scipy,  mpl_toolkits.axes_grid1, sklearn**
* **itertools, imblearn**
* **Jupyter Notebook**

### Data Availability
The well-log datasets used for model training and testing are confidential and cannot be publicly released.
Accordingly:
* File paths are replaced with "___" placeholders
* The structure of one training DataFrame is shown in the notebook
* To execute the workflow, users must supply datasets with identical variable names for all input and output features

### Reproducibility
To reproduce results:

1. Clone the repository
2. Replace "___" file paths with valid dataset locations
3. Ensure feature names match the template DataFrame
4. Run the Jupyter notebook sequentially from top to bottom

### Requirements:
The entire notebook was executed under:
* Python 3.12.8

# Contact
For further questions or comments, feel free to email at: royrupam964@kgpian.iitkgp.ac.in or royrupam964@gmail.com
