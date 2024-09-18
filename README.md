# Data Privacy in Big Data: A Theoretical Exploration of Frameworks and Challenges

### Overview

This project explores the application of several privacy-preserving frameworks on the **Adult Census Income Dataset** using **Google Colab** and **PySpark**. The frameworks implemented include **K-Anonymity**, **L-Diversity**, **T-Closeness**, **Differential Privacy**, **Federated Learning**, **Homomorphic Encryption**, and **Secure Multi-Party Computation (SMPC)**.

---

## Project Description

This project demonstrates the implementation of privacy frameworks on the **Adult Census Income Dataset**. Privacy frameworks were applied to preserve data privacy while evaluating the performance impact on machine learning models (e.g., Logistic Regression). We visualize the effect of each privacy framework on both data utility and privacy.

### Key Steps:

1. **Implementing privacy-preserving frameworks** such as K-Anonymity, L-Diversity, T-Closeness, Differential Privacy, etc.
2. **Evaluating model accuracy** on privacy-enhanced datasets using Logistic Regression.
3. **Visualizing privacy-utility trade-offs**.

---

## Privacy Frameworks

### 1. **K-Anonymity**:
   - **Objective**: Ensure that each record in the dataset cannot be distinguished from at least `k` other records based on quasi-identifiers.
   - **Method**: Generalizing quasi-identifiers like `age`, `workclass`, and `education_num` into broader categories.

### 2. **L-Diversity**:
   - **Objective**: Extend K-Anonymity by ensuring sensitive attributes (like income) remain diverse within each group.
   - **Method**: Creating groups where sensitive attributes, such as income, maintain sufficient diversity.

### 3. **T-Closeness**:
   - **Objective**: Ensure that the distribution of sensitive attributes in each group is close to the overall distribution.
   - **Method**: Applying a threshold (`T`) to limit how much the distribution within each group can differ from the original dataset.

### 4. **Differential Privacy**:
   - **Objective**: Add random noise to data or query results to protect individual privacy.
   - **Method**: Adding Laplace noise to sensitive data such as age, income, and capital gain.

### 5. **Federated Learning**:
   - **Objective**: Train machine learning models across multiple decentralized datasets without sharing the actual data.
   - **Method**: Simulating Federated Learning using multiple dataset partitions.

### 6. **Homomorphic Encryption**:
   - **Objective**: Perform computations directly on encrypted data without decrypting it, ensuring privacy throughout the computation.
   - **Method**: Encrypting sensitive attributes and simulating computations on the encrypted values.

### 7. **SMPC (Secure Multi-Party Computation)**:
   - **Objective**: Allow multiple parties to compute their data without revealing their private inputs.
   - **Method**: Splitting data into secret shares and combining results securely.

---

## Datasets

We used the **Adult Census Income Dataset** from the UCI Machine Learning Repository. The dataset contains personal information about individuals, making it ideal for exploring privacy frameworks.

- **Attributes**: Age, workclass, education, marital status, occupation, relationship, race, sex, capital gain, capital loss, hours per week, and income.
- **Sensitive Attributes**: Income, capital gain, capital loss.
- **Quasi-identifiers**: Age, workclass, education level.
### [Dataset URL](https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data)
---

## Results and Visualizations

The following visualizations compare the data distributions and model accuracy before and after applying privacy frameworks:

### 1. **Age Distribution Before and After K-Anonymity**:
   - We generalized the age attribute to anonymize the data.

### 2. **Income Distribution Before and After L-Diversity**:
   - Visualizes how income diversity is preserved in anonymized groups.

### 3. **Capital Gain Distribution Before and After T-Closeness**:
   - Shows how T-Closeness impacts the distribution of sensitive attributes.

### 4. **Privacy vs Utility Trade-Off**:
   - A bar chart that compares the model accuracy across different privacy frameworks.

---

## How to Run in Google Colab

### Step 1: **Open Google Colab**

- Go to [Google Colab](https://colab.research.google.com/).
- Upload the provided **notebooks** or use the pre-defined **Google Colab code snippets**.

### Step 2: **Clone the GitHub Repository**

In the Colab notebook, run the following code to clone the repository:

```python
!git clone https://github.com/mairoky/data-privacy-frameworks-evaluation.git
!cd data-privacy-frameworks-evaluation
```

### Step 3: **Install Required Libraries**

- PySpark,
- pycryptodome,
- matplotlib

### Step 4: **Load Dataset**

Use the code provided in the notebook to automatically download the dataset

### Step 5: **Run data privacy frameworks**

Each privacy framework has a dedicated section in the notebook

## Requirements
- Google Colab or Jupyter Notebook
- PySpark for big data processing
- PyCryptodome for Homomorphic Encryption
- Matplotlib for visualizations

