# Phishing Website Detection Using Machine Learning

## Project Overview

**Project Title:** Phishing Website Detection Using Machine Learning: A Comparative Analysis of Four Classification Algorithms

This project develops a machine learning classification system to identify phishing websites using numerical website features. Four classification algorithms are trained and evaluated to compare their performance in distinguishing between phishing and legitimate websites.

The project also investigates how changing the regularization parameter `C` affects the performance of a Support Vector Machine (SVM) classifier.

## Objectives

- Load and explore a publicly available phishing website dataset.
- Perform data inspection and preprocessing.
- Explore the distribution of target classes and numerical features.
- Train four machine learning classification algorithms.
- Evaluate the models using accuracy, precision, recall, F1-score, and execution time.
- Compare model performance using tables and confusion matrices.
- Conduct an SVM parameter experiment.
- Identify the strongest model among the tested algorithms.

## Dataset

**Dataset name:** Phishing Websites

**Source:** UCI Machine Learning Repository

**Dataset ID:** 327

**Dataset link:** https://archive.ics.uci.edu/dataset/327/phishing+websites

The dataset contains website-related features and target labels used to train a phishing website classifier.

The exact number of records, feature names, target labels, and data characteristics should be verified from the downloaded dataset and executed notebook.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- UCI Machine Learning Repository dataset access library

## Machine Learning Algorithms

### 1. Decision Tree Classifier

A tree-based classification algorithm that learns decision rules from the input features.

### 2. K-Nearest Neighbors (KNN)

A classification algorithm that predicts the class of a sample using the classes of its nearest training examples. Feature scaling is used in the preprocessing pipeline.

### 3. Support Vector Machine (SVM)

A classification algorithm that learns a decision boundary between classes. StandardScaler is used in the preprocessing pipeline.

### 4. Gaussian Naive Bayes

A probabilistic classification algorithm based on Bayes' theorem. Its suitability should be assessed against the actual feature representation.

## Project Workflow

1. Download the UCI dataset.
2. Inspect the dataset dimensions, feature names, data types, and target labels.
3. Check missing values and duplicate records.
4. Perform exploratory data analysis.
5. Prepare the features and target labels.
6. Split the data into training and testing sets using an 80:20 stratified split.
7. Prepare preprocessing pipelines.
8. Train the four classification algorithms.
9. Evaluate their performance.
10. Generate confusion matrices and comparison plots.
11. Experiment with different SVM `C` values.
12. Save evaluation results and prepare the final report.

## Evaluation Metrics

The following metrics are used to compare the classification algorithms:

- **Accuracy:** Proportion of correctly classified samples.
- **Precision:** Proportion of predicted positive samples that are actually positive.
- **Recall:** Proportion of actual positive samples correctly identified.
- **F1-score:** Harmonic mean of precision and recall.
- **Training time:** Time required to fit the model.
- **Prediction time:** Time required to predict labels for the test dataset.

The positive target label must be verified before interpreting precision, recall, and F1-score specifically as phishing-detection metrics.

## SVM What-If Experiment

The SVM classifier was evaluated with three regularization parameter values:

- `C = 0.1`
- `C = 1`
- `C = 10`

### Observed Results

The following values were obtained from the executed Google Colab experiment.

| C | Accuracy | Precision | Recall | F1-score |
|---:|---:|---:|---:|---:|
| 0.1 | 0.9358 | 0.9264 | 0.9610 | 0.9434 |
| 1 | 0.9516 | 0.9418 | 0.9732 | 0.9573 |
| 10 | 0.9692 | 0.9633 | 0.9821 | 0.9726 |

Among the three tested configurations, `C = 10` achieved the highest observed F1-score of approximately `0.9726`.

These results apply to the particular train-test split and experiment used in this project. They do not establish that `C = 10` will always perform best on other datasets.

## Project Files

The repository should contain the following files:

```text
Phishing-Website-Detection-ML/
│
├── phishing_website_detection.ipynb
├── model_comparison_results.csv
├── svm_what_if_results.csv
├── project_summary.txt
├── Phishing_Website_Detection_Report.docx
└── README.md
```

The filenames above are suggested names. Use the actual filenames of the files you upload.

## How to Run the Project

1. Download or clone this repository.
2. Open the Jupyter notebook in Google Colab.
3. Run the notebook cells in order.
4. Allow the dataset to download.
5. Execute the preprocessing, training, evaluation, and experiment cells.
6. Review the generated tables, graphs, and confusion matrices.
7. Download the generated CSV files and final report.

**Note:** An internet connection is required to download the dataset when it is not already available in the notebook environment.

## Results

The final comparison of Decision Tree, KNN, SVM, and Gaussian Naive Bayes is recorded in:

`model_comparison_results.csv`

The SVM parameter experiment is recorded in:

`svm_what_if_results.csv`

The best-performing classification algorithm should be identified using the actual model comparison results, considering precision, recall, F1-score, and the confusion matrix in addition to accuracy.

## Limitations

- The evaluation uses a particular train-test split.
- Performance may vary with different datasets and data distributions.
- The suitability of the Naive Bayes variant depends on the actual feature representation.
- The target-label meanings must be verified before interpreting positive-class metrics as phishing-detection performance.
- The experiment does not establish real-world deployment readiness.
- Further validation on independent and current website data would be necessary before practical deployment.

## Conclusion

This project compares four supervised machine learning algorithms for phishing website classification. It evaluates model performance using standard classification metrics and investigates the effect of SVM regularization on the observed results.

The findings provide a basis for comparing the tested models. The final model selection should be supported by the executed notebook's results, confusion matrices, and the project's evaluation objectives.

## References

1. UCI Machine Learning Repository. *Phishing Websites Dataset*. https://archive.ics.uci.edu/dataset/327/phishing+websites
2. Pedregosa, F., et al. (2011). *Scikit-learn: Machine Learning in Python*. Journal of Machine Learning Research, 12, 2825–2830. https://jmlr.org/papers/v12/pedregosa11a.html

**Institution:** [Enter your college or university]

**Academic Year:** [Enter your academic year]
