
# Cybersecurity Incident Triage Classification Model

## Problem Statement:
Imagine you are working as a data scientist at **Microsoft**, tasked with enhancing the efficiency of **Security Operation Centers (SOCs)** by developing a machine learning model that can accurately predict the triage grade of cybersecurity incidents. Utilizing the comprehensive **GUIDE dataset**, your goal is to create a classification model that categorizes incidents as **true positive (TP)**, **benign positive (BP)**, or **false positive (FP)** based on historical evidence and customer responses. 

The model should be robust enough to support guided response systems in providing SOC analysts with precise, context-rich recommendations, ultimately improving the overall security posture of enterprise environments.

The model will be trained using the `train.csv` dataset, and the performance will be evaluated based on **macro-F1 score**, **precision**, and **recall** using the `test.csv` dataset. This will ensure that the model generalizes effectively to unseen data and remains reliable for real-world applications.

## Table of Contents:
1. [Installation](#installation)
2. [Dataset](#dataset)
3. [Modeling Process](#modeling-process)
4. [Evaluation Metrics](#evaluation-metrics)
5. [Business Use Cases](#business-use-cases)
6. [Conclusion](#conclusion)

---

## Installation:
To run the project and train the model, you will need to install the following Python libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Dataset:
The model is trained using the **train.csv** dataset, which contains historical cybersecurity incident data, including features related to the incident's characteristics and customer responses. The **test.csv** dataset will be used to evaluate the model's performance on unseen data.

- **train.csv**: The training data with features and the corresponding incident triage grades.
- **test.csv**: The test data used to evaluate the performance of the trained model.

---

## Modeling Process:
1. **Data Preprocessing**: Clean the dataset by handling missing values, encoding categorical variables, and scaling numeric features as necessary.
2. **Feature Selection**: Identify and select the most relevant features for training the model.
3. **Model Training**: Implement a machine learning classification algorithm (e.g., Random Forest, XGBoost, etc.) to predict the triage grade (TP, BP, or FP).
4. **Hyperparameter Tuning**: Optimize the model by fine-tuning its hyperparameters for improved performance.
5. **Model Evaluation**: Evaluate the model using precision, recall, and macro-F1 score on the test dataset.

---

## Evaluation Metrics:
The following evaluation metrics will be used to assess the model's performance:

- **Macro-F1 Score**: The harmonic mean of precision and recall, calculated for each class and then averaged. This metric is useful in imbalanced classification problems.
- **Precision**: The proportion of true positives (TP) out of all instances predicted as positive.
- **Recall**: The proportion of true positives (TP) out of all actual positive instances.

---

## Business Use Cases:
The solution developed in this project can be implemented in various business scenarios, particularly in the field of **cybersecurity**. Some potential applications include:

1. **Security Operation Centers (SOCs)**: Automating the triage process by accurately classifying cybersecurity incidents, allowing SOC analysts to prioritize their efforts and respond to critical threats more efficiently.
   
2. **Incident Response Automation**: Enabling guided response systems to automatically suggest appropriate actions for different types of incidents, leading to quicker mitigation of potential threats.
   
3. **Threat Intelligence**: Enhancing threat detection capabilities by incorporating historical evidence and customer responses into the triage process, which can lead to more accurate identification of true and false positives.
   
4. **Enterprise Security Management**: Improving the overall security posture of enterprise environments by reducing the number of false positives and ensuring that true threats are addressed promptly.

---

## Features Description:

AlertTitle: Descriptive title of the security alert.

Category: Classification of the alert based on the type of incident.

IncidentGrade: Severity level of the security incident.

EntityType: The type of entity affected (e.g., user, device, network, application).

EvidenceRole: Role of the evidence in the investigation.

Sha256: Unique hash value for file identification.

IpAddress: IP address associated with the incident.

Url: Web address related to the alert.

AccountUpn: User principal name associated with the account.

AccountName: Name of the account involved in the incident.

DeviceName: Name of the device involved in the alert.

RegistryKey: Registry key related to the alert (for Windows-based incidents).

RegistryValueName: Name of the registry value modified.

RegistryValueData: Data contained in the registry value.

ApplicationName: Name of the application involved in the incident.

FileName: Name of the file related to the alert.

FolderPath: Path of the folder containing the affected file.

OSFamily: Operating system family (Windows, Linux, macOS, etc.).

OSVersion: Specific version of the operating system.

CountryCode: Country code of the device's location.

State: State/Region of the device’s location.

City: City where the device is located.

Year: Year of the recorded incident.

Month: Month of the recorded incident.

Day: Day of the recorded incident.

## Conclusion:
This project demonstrates the potential of machine learning in improving the efficiency and accuracy of cybersecurity incident triage in Security Operation Centers (SOCs). By automating the classification of cybersecurity incidents into true positives, benign positives, or false positives, organizations can ensure faster, more accurate responses to threats, improving overall enterprise security.

---
