# UNSW-NB15 Network Intrusion Detection System

This repository contains a comprehensive machine learning pipeline for detecting network intrusions using the **UNSW-NB15 dataset**. The project features a **custom Decision Tree Classifier (CART algorithm)** built from scratch using NumPy, along with an extensive Exploratory Data Analysis (EDA) of 2.5 million network flow records.

## Project Overview

Network Intrusion Detection Systems (NIDS) are vital for modern cybersecurity. This project demonstrates the ability to handle massive datasets and implement core machine learning algorithms without relying on high-level libraries like Scikit-Learn for the primary logic.

### Key Highlights:

- **Custom Algorithm:** Implementation of a CART Decision Tree using Gini Impurity and recursive splitting.
    
- **Big Data EDA:** Analysis of ~2.5 million records, identifying class imbalances and specific attack patterns.
    
- **Geospatial Insights:** Discovered that a significant portion of attack traffic originated from a specific subnet in Pyongyang, North Korea.
    
- **Performance Benchmarking:** Comparative analysis between the custom model and Scikit-Learn’s Random Forest, Gradient Boosting, and Logistic Regression.
    

---

## Implementation Details

### The Custom Decision Tree

The model follows the **Classification and Regression Tree (CART)** logic. It recursively partitions the feature space to minimize the Gini Impurity at each node.

The Gini Impurity $G$ is calculated as:

$$G = 1 - \sum_{i=1}^{n} p_i^2$$

Where $p_i$ is the probability of a sample belonging to class $i$.

### Data Preprocessing

- **Handling Class Imbalance:** The dataset is highly skewed (12.6% Attack vs 87.4% Normal).
    
- **Feature Engineering:** Managed 49 features including nominal IP addresses and integer port numbers.
    
- **Data Leakage Prevention:** Ensured strict separation between training and testing sets during the normalization and encoding phases.
    

---

##  Results & Benchmarks

The custom model was benchmarked against standard industry models to validate its mathematical accuracy.

|**Model**|**Accuracy**|**F1-Score**|
|---|---|---|
|**DecisionTreeScratch (Ours)**|**88.4%**|**0.86**|
|Scikit-Learn Random Forest|91.2%|0.89|
|Logistic Regression|82.1%|0.78|
