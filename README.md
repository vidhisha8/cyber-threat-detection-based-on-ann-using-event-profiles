# Cyber Threat Detection Based on ANN Using Event Profiles

## About the Project

This project explores the use of Machine Learning and Deep Learning for cybersecurity threat detection.

Traditional security monitoring systems can generate large numbers of alerts, making it challenging to identify potentially malicious activity. The project investigates an AI-assisted Security Information and Event Management (SIEM) approach that processes security event data and applies classification techniques to distinguish between different event categories.

The main objective is to explore how event profiling, text-based feature extraction, and neural network models can support automated cyber threat detection.

## Project Objectives

- Process security event data into structured numerical representations.
- Apply TF-IDF-based feature extraction to prepare event data for classification.
- Explore traditional Machine Learning and Deep Learning approaches to threat detection.
- Compare classification approaches using metrics such as accuracy, precision, recall, and F-measure.
- Investigate the use of Artificial Neural Networks (ANNs) and LSTM networks for security event classification.

## Technologies Used

The project presentation identifies the following technologies and tools:

- **Programming Language:** Python
- **Web Framework:** Django
- **Frontend:** HTML, CSS, JavaScript
- **Data Processing:** Pandas, NumPy
- **Feature Extraction:** TF-IDF
- **Machine Learning:** Scikit-learn
- **Deep Learning:** TensorFlow / Keras
- **Visualization:** Matplotlib
- **Database:** MySQL (listed in the project presentation)

The actual implementation of each component should be confirmed against the source code before treating the complete stack as verified.

## Methodology

### 1. Security Event Data

The project presentation describes a dataset named `kdd_train.csv` containing approximately 10,000 security event records.

The dataset is used as the basis for preprocessing, event representation, and classification experiments.

### 2. Data Preprocessing and Feature Extraction

The documented workflow uses TF-IDF (Term Frequency–Inverse Document Frequency) to convert text-based event information into numerical feature representations suitable for classification.

These representations provide input features for the evaluated Machine Learning and Deep Learning approaches.

### 3. Model Evaluation

The project explores the following classification approaches.

**Traditional Machine Learning**

- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Decision Tree

**Deep Learning**

- Artificial Neural Network (ANN) / Fully Connected Neural Network (FCNN)
- Long Short-Term Memory (LSTM)

The project presentation discusses comparing these approaches using accuracy, precision, recall, and F-measure.

## Dataset and Evaluation Setup

| Item | Details reported in the presentation |
|---|---|
| Dataset | `kdd_train.csv` |
| Number of records | 9,999 |
| Training records | 7,999 |
| Testing records | 2,000 |
| Approximate split | 80% training / 20% testing |

The record counts above are taken from the project presentation. The exact preprocessing procedure and whether the split was stratified should be verified against the implementation.

## Reported Results

The project presentation reports an LSTM accuracy of approximately **94% during training**.

This is a reported training result, not an independently reproduced result or a confirmed held-out test accuracy. A complete comparison of the models would require the corresponding evaluation outputs for each model.

Accuracy, precision, recall, and F-measure are relevant metrics for evaluating classification performance, particularly when the dataset contains imbalanced classes.

## Challenges and Considerations

- Preparing security event data for numerical feature extraction.
- Representing event information in a form suitable for classification.
- Comparing conventional Machine Learning algorithms with neural network approaches.
- Evaluating classification results using multiple performance metrics.
- Avoiding conclusions based on accuracy alone when class distributions may be imbalanced.

## Limitations

- The reported results have not been independently reproduced here.
- The presentation's reported LSTM training accuracy does not establish its performance on unseen data.
- The effectiveness of the models depends on the quality, labels, and distribution of the dataset.
- The available project documents do not independently establish the performance of every listed model.
- The complete implementation of the Django interface, database integration, and model-training workflow should be verified against the source code.

## Future Improvements

- Evaluate every model on the same held-out test dataset.
- Report per-model accuracy, precision, recall, and F1-score.
- Use confusion matrices to examine false positives and false negatives.
- Validate the approach on additional security datasets.
- Improve preprocessing and event representation where needed.
- Further investigate neural network architectures for security event classification.
- Improve the usability and reporting of the application interface.

## About

This project was developed as part of my third-year B.Tech academic work, exploring the application of Machine Learning and Deep Learning to cybersecurity.

**Author:** Mantravadi Vidhisha

