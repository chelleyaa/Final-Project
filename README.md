# ARRHYTHMIA CLASSIFICATION IN ELECTROCARDIOGRAM SIGNALS USING ENSEMBLE MACHINE LEARNING WITH BOOSTING FRAMEWORK
Arhythmia classification system based on the AAMI standard using Python on the Jupyter platform and employed Decision Tree and various ensemble machine learning focused on boosting algorithms, including AdaBoost, Gradient Boosting, XGBoost, CatBoost, and LightGBM.

# About The Project
This project aims to develop and evaluate several machine learning models for the automatic classification of heartbeats. The classification adheres to the standard set by the Association for the Advancement of Medical Instrumentation (AAMI).
The analysis and model implementation are conducted within a Jupyter Notebook to facilitate interactive data exploration, visualization, and model evaluation. The data used is the MIT-BIH Arrhythmia Database.

Key Features
1. AAMI Standard-Based Classification: Groups heartbeats into 5 main classes (N, S, V, F, Q).
2. Standardized Dataset Usage: Utilizes the widely recognized MIT-BIH dataset.
3. Diverse Model Implementation: Implements a Decision Tree as a baseline and compares it with advanced boosting algorithms:
   a. AdaBoost
   b. Gradient Boosting
   c. XGBoost
   d. LightGBM
   e. CatBoost
4. Comparative Analysis: Evaluates and compares the performance of each model based on standard metrics like accuracy, precision, recall, AUC, F1-score, and testing time.

# Dataset
This project uses the MIT-BIH Arrhythmia Database from PhysioNet. The dataset contains 48 half-hour ambulatory ECG recordings, obtained from 47 subjects studied by the BIH Arrhythmia Laboratory between 1975 and 1979. The recordings were digitized at 360 samples per second per channel with 11-bit resolution over a 10 mV range.

# References
1. Moody GB, Mark RG. The impact of the MIT-BIH Arrhythmia Database. IEEE Eng in Med and Biol 20(3):45-50 (May-June 2001). (PMID: 11446209)
2. Goldberger, A., Amaral, L., Glass, L., Hausdorff, J., Ivanov, P. C., Mark, R., ... & Stanley, H. E. (2000). PhysioBank, PhysioToolkit, and PhysioNet: Components of a new research resource for complex physiologic signals. Circulation [Online]. 101 (23), pp. e215–e220. RRID:SCR_007345.
