# UNSW-NB15-Network-Intrusion-Detection-

This project explores machine learning techniques to classify network traffic as "Normal" or "Attack" using the UNSW-NB15 dataset. The highlight of this project is a custom implementation of a Decision Tree Classifier (CART algorithm) built from scratch without the use of standard machine learning libraries like Scikit-Learn for the core logic.





Project Overview
Modern network security relies on Intrusion Detection Systems (IDS) to automatically identify malicious activity. This project involves:



EDA: Comprehensive analysis of class imbalances and feature correlations.





Custom Algorithm: Building a CART Decision Tree from scratch using Gini Impurity.



Benchmarking: Comparing the custom model against standard library implementations like Scikit-Learn’s Random Forest and Logistic Regression.


Dataset
The UNSW-NB15 dataset was created by the Australian Centre for Cyber Security (ACCS). It contains approximately 2.5 million records with 49 features including protocol type, service, and TTL values.





Target: label (0 for normal, 1 for attack).



Attack Categories: Includes Fuzzers, Backdoors, DoS, and more.

Key Findings

Subnet Analysis: Our EDA discovered that a significant portion of attack traffic originated from a specific subnet (175.45.176.0/24).




Feature Correlation: Features like sttl (Source Time to Live) showed high correlation with attack labels.
