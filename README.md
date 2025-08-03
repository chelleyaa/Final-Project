# ARRHYTHMIA CLASSIFICATION IN ELECTROCARDIOGRAM SIGNALS USING ENSEMBLE MACHINE LEARNING WITH BOOSTING FRAMEWORK
A research project focused on the classification of electrocardiogram (ECG) signals to identify arrhythmia. This study implements and evaluates a suite of boosting-based ensemble machine learning models, optimized with the Optuna framework, to achieve high-accuracy, beat-by-beat classification according to the AAMI standard.

# About The Project
Arrhythmia is a cardiac condition characterized by deviations from the normal heart rhythm, including abnormalities in rate, regularity, or impulse origin. Early and accurate detection is critical. This project aims to identify the optimal boosting-based ensemble architecture for classifying arrhythmia types from ECG signals.

The study conducts a comparative analysis of five prominent boosting algorithms: 
AdaBoost, GradientBoost, XGBoost, LightGBM, and CatBoost. Their performance is benchmarked against a single Decision Tree model, as well as bagging and stacking ensemble methods. A key objective is the systematic optimization of model hyperparameters using the Optuna framework to maximize classification efficacy. The project uses the well-known MIT-BIH Arrhythmia Database and classifies heartbeats according to the Association for the Advancement of Medical Instrumentation (AAMI) standard.

Classification Classes (AAMI Standard)
The models classify heartbeats into five standard categories:

1. N: Normal Beat

2. S: Supraventricular Abnormalities

3. V: Ventricular Escape

4. F: Fusion Heartbeat

5. Q: Unknown Beat

# Key Features
1. Comparative Analysis: In-depth evaluation of five major boosting algorithms to determine the most effective model for arrhythmia classification.
2. Advanced Hyperparameter Optimization: Utilizes the Optuna framework to efficiently search the hyperparameter space and identify the optimal configuration for each algorithm.
3. Rich Feature Engineering: Employs the Time Series Feature Extraction Library (TSFEL) to automatically extract 314 distinct features from the statistical, temporal, and spectral domains of each ECG heartbeat.
4. Comprehensive Signal Processing: Implements a robust preprocessing pipeline including wavelet filtering (db6 DWT), polynomial detrending, and Savitzky-Golay smoothing to enhance signal quality.
5. Performance Benchmarking: Provides a detailed comparison of boosting methods against other ensemble techniques like bagging and stacking, based on a wide range of evaluation metrics

# Methodology & Workflow
The project follows a structured pipeline from data acquisition to model evaluation.
1. Data Acquisition: The study uses the public MIT-BIH Arrhythmia Database from Physionet, which contains 48 half-hour ECG recordings from 47 subjects.
2. Exploratory Data Analysis (EDA): Initial analysis was performed to understand the distribution of arrhythmia classes across patients and identify the dataset's imbalanced nature.


3. Preprocessing:
   a. Balancing: The imbalanced dataset was handled using Random Undersampling to create a balanced set of 500 samples per class.
   b.Filtering: A multi-stage filtering process was applied: db6 Discrete Wavelet Transform (DWT) to reduce noise, polynomial detrend to remove baseline drift, Savitzky-Golay filter to smooth the signal while preserving morphological features.
4. Segmentation: R-peaks were detected using the find_peaks function from the SciPy library, and the signal was segmented around each peak to isolate individual heartbeats.
5. Feature Extraction: The TSFEL library was used to automatically generate 314 features for each heartbeat segment, covering statistical, temporal, and spectral domains.
6. Model Training & Optimization:
a. The dataset was split into 80% for training and 20% for validation.
b. The five boosting models were trained first with default parameters and then optimized using Optuna.
7. Evaluation: Models were evaluated on the validation data using accuracy, precision, recall, F1-score, AUC, confusion matrices, and testing time.

# Technology Stack
a. Primary Language: Python 3 
b. Environment: Jupyter 
c. Core ML Libraries: AdaBoost, GradientBoost, XGBoost, LightGBM, CatBoost
d. Data Handling: Pandas, NumPy
e. Signal Processing: SciPy
f. Feature Extraction: TSFEL
g. Hyperparameter Optimization: Optuna

# Conclusion
Based on a comprehensive evaluation, XGBoost is the most optimal boosting architecture for this arrhythmia classification task, delivering a superior balance of accuracy (92.40%), AUC (0.9894), and F1 Score (92.80%). The effectiveness of XGBoost is attributed to its advanced regularization mechanisms (L1 & L2), its iterative approach to correcting errors via gradient boosting, and its ability to handle complex, non-linear feature interactions provided by the TSFEL library.


The study also confirms that hyperparameter optimization is critical, with the  Optuna framework proving to be an effective tool for systematically enhancing model performance. While methods like Bayesian Bagging may offer higher recall, the overall performance and efficiency of optimized boosting models like XGBoost present a compelling case for their use in developing automated ECG analysis systems.


# References
1. Moody GB, Mark RG. The impact of the MIT-BIH Arrhythmia Database. IEEE Eng in Med and Biol 20(3):45-50 (May-June 2001). (PMID: 11446209)
2. Goldberger, A., Amaral, L., Glass, L., Hausdorff, J., Ivanov, P. C., Mark, R., ... & Stanley, H. E. (2000). PhysioBank, PhysioToolkit, and PhysioNet: Components of a new research resource for complex physiologic signals. Circulation [Online]. 101 (23), pp. e215–e220. RRID:SCR_007345.
