## Credit Risk-Assessment Model for UAE's Commercial Banks: A Machine Learning Approach

---

### **Table of Contents:**

1. [Abstract](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach)
   
2. [Introduction](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Introduction.md) 

4. [Related Work](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Related%20Work.md) 

5. [Data Collection and Variable Definition](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Data%20Collection%20and%20Variable%20Definition.md) 

6. [Methodology](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Methodology.md)

7. [Data Reduction Using Linear Discriminant Analysis (LDA)](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Data%20Reduction%20Using%20Linear%20Discriminant%20Analysis%20(LDA).md)

8. [Experimentation and Results](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Experimentation%20and%20Results.md)

9. [Conclusion and Further Research](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Conclusion%20and%20Further%20Research.md)

### 1. Abstract
---
The paper explores the use of machine learning (ML) to improve credit risk assessment in UAE's commercial banks. 

Traditional credit rating systems classify credits as either "good" or "bad," which lacks precision. Machine learning models, specifically Linear Discriminant Analysis (LDA), can provide more accurate and efficient predictions. 

Credit risk assessment is crucial for banks because it determines whether they will get their money back when they lend it out. Accurate predictions help banks avoid losses and financial crises. 

The goal is to create and validate a credit risk model using LDA to differentiate between good and bad creditors, thereby helping banks avoid financial losses and crises.

#### 1.1 Challenges in Credit Risk Evaluation

One of the biggest challenges in banking management is accurately evaluating a customer's credit risk. The inability to precisely determine risk can negatively impact credit management, leading to poor financing decisions. 

Approved loans that cannot be repaid lead to financial losses, while rejecting potentially good borrowers results in lost opportunities.

To improve credit risk assessment, many studies suggest the use of data mining tools and machine learning models. These models, including genetic algorithms, support vector machines (SVM), decision trees, and hybrid models, have demonstrated better performance and accuracy compared to traditional statistical methods.

#### 1.2 Subjectivity in Traditional Credit Risk Assessments

In UAE's commercial banks, credit risk assessments are often done manually, making them subjective and prone to biases based on personal insights and intuition. 

While many banks worldwide have adopted data-driven credit risk analysis, some still rely on traditional methods, risking financial crises or distress.

### 2. Related Work
---

#### 2.1 Decision Tree Models

One study developed a prediction model using Decision Trees to assess the credibility of customers applying for bank loans. Decision Trees classify data by splitting it into branches based on feature values, ultimately leading to a decision about the applicant's creditworthiness.

Decision Trees are easy to understand and interpret, making them popular for credit risk assessment. However, they can be prone to overfitting, where the model performs well on training data but poorly on new, unseen data.

#### 2.2 Bayesian Networks and Naive Bayes

Another study compared three models: J48 (a type of Decision Tree), Bayes Net, and Naive Bayes. The J48 model showed the best accuracy. Bayesian Networks and Naive Bayes use probabilistic methods to predict credit risk based on the likelihood of different factors.

Bayesian models can handle uncertainty well and are useful when dealing with incomplete data. However, they may require strong assumptions about the independence of features, which is not always realistic.

#### 2.3 Clustering Algorithms

A study applied a multi-dimensional risk prediction clustering algorithm to identify bad loan applicants. Clustering groups similar data points together, helping to identify patterns and trends in borrower behavior.

Clustering algorithms can uncover hidden patterns in data, providing valuable insights for credit risk assessment. However, defining the optimal number of clusters can be challenging.

#### 2.4 Hybrid Models

A study proposed two credit scoring models using data mining techniques for Jordanian commercial banks. These models combined Logistic Regression, Radial Basis Neural Networks, Multi-layer Perceptron, and Support Vector Machines to improve credit risk assessment.

Hybrid models can achieve higher accuracy by leveraging the strengths of multiple algorithms. They are complex but often outperform single models in credit risk assessment.

### 3. Data Collection
---

The dataset used in this study comprises both accepted and rejected loan applications from different commercial banks in the UAE, collected from the years 2016 to 2018. The data consists of 7778 cases. 

Out of these, 4612 applications (59.3%) were deemed creditworthy, while 3166 applications (40.3%) were not.

The dataset includes 11 variables: 10 input variables and 1 output variable. 

#### 3.1 **Variable Definitions and Explanations:**

1. **Resolving the utilization of unsecured lines (P1)**
   - **Type:** Scale
   - **Definition:** Indicates the credit card limits of the borrower after excluding any current loan debt and real estate.
   - **Layman Explanation:** This shows how much credit is available on the borrower’s credit cards, excluding any other debts or mortgages. 💳

2. **Age (P2)**
   - **Type:** Scale
   - **Definition:** Applicant’s age.
   - **Layman Explanation:** Simply the age of the person applying for the loan. 🎂

3. **Number of Times 30-59 Days Past Due Not Worse (P3)**
   - **Type:** Scale
   - **Definition:** The number of times borrowers have paid their EMIs late but within 30 to 59 days.
   - **Layman Explanation:** This tracks how often the borrower was late on payments but not by more than 59 days. ⏳

4. **Debt Ratio (P4)**
   - **Type:** Scale (0 – 1)
   - **Definition:** Ratio of monthly debt payments to monthly income.
   - **Layman Explanation:** If someone earns $1000 a month and spends $700 on debts, their debt ratio is 0.7 ($700/$1000). 💸➗

5. **Monthly Income (P5)**
   - **Type:** Scale
   - **Definition:** Total monthly income of the borrower, log-transformed.
   - **Layman Explanation:** How much money the borrower makes every month, adjusted to a logarithmic scale to manage wide variations. 💰📈

6. **Number of Open Credit Lines and Loans (P6)**
   - **Type:** Scale
   - **Definition:** Number of open loans and credit cards the borrower holds.
   - **Layman Explanation:** Total number of active loans and credit cards the borrower has. 💳🏠

7. **Number of Times 90 Days Late (P7)**
   - **Type:** Scale
   - **Definition:** Number of times a borrower has paid their dues 90 days after the due date.
   - **Layman Explanation:** How often the borrower was very late (90 days) on their payments. 🕰️

8. **Number Real Estate Loans or Lines (P8)**
   - **Type:** Scale
   - **Definition:** Number of loans the borrower holds for real estate.
   - **Layman Explanation:** Number of mortgages or home loans the borrower has. 🏠

9. **Number of Times 60-89 Days Past Due Not Worse (P9)**
   - **Type:** Scale
   - **Definition:** Number of times borrowers have paid their EMIs late but within 60 to 89 days.
   - **Layman Explanation:** This shows how often the borrower was late by up to 89 days on payments. ⏲️

10. **Number of Dependents (P10)**
    - **Type:** Scale
    - **Definition:** Number of dependent family members the borrower has, excluding the borrower.
    - **Layman Explanation:** How many people depend financially on the borrower (like children or elderly parents). 👨‍👩‍👧‍👦

11. **Outcome (Output)**
    - **Type:** Binary
    - **Definition:** Indicates whether the creditor is a good or bad creditor.
    - **Layman Explanation:** The final result showing if the borrower is likely to repay the loan (good) or not (bad). ✅❌

### 4. Methodology
---

#### 4.1 Data Preprocessing
Data preprocessing includes cleaning the data, handling missing values, normalizing the data, and reducing its dimensionality using LDA. This step prepares the data for machine learning algorithms.

#### 4.2 Data Cleaning
Data cleaning involves identifying and correcting errors, filling in missing values, and removing irrelevant data. This step ensures the dataset is accurate and complete.

#### 4.3 Data Transformation
Data transformation involves converting data into a suitable format for analysis. This includes scaling the data so that different features are comparable and applying logarithmic transformations to manage wide variations.

### 5. Data Reduction Using Linear Discriminant Analysis (LDA)
---

Linear Discriminant Analysis (LDA) is a linear machine learning algorithm used for multi-class classification. It seeks to separate (or discriminate) samples in the training dataset by their class value (e.g., good or bad creditor). The model aims to find a linear combination of input variables that maximizes the separation between classes.

#### 5.1 **Math Intuition:**

LDA works by projecting the data onto a lower-dimensional space. It calculates the mean vectors for each class and the overall mean vector for all classes. The goal is to maximize the distance between the means of different classes (between-class scatter) while minimizing the spread within each class (within-class scatter).

- **Between-class scatter matrix (S_B):** Measures the spread of the means of different classes.
- **Within-class scatter matrix (S_W):** Measures the spread of samples within each class.

[Link for LDA](https://www.notion.so/343a3b1684a5480b968121afe6c3a709?v=d6b08dbd6485489a8825444053600879)

#### 5.2 Results from LDA

After applying LDA, the features are ranked based on their correlation with the output (creditworthiness). The attributes with the highest correlation are selected for further modeling.

**Results:**
The attributes in decreasing order of correlation with the output are:
1. Resolving utilization of unsecured lines
2. Age
3. Number of times 30-59 days past due
4. Debt ratio
5. Monthly income
6. Number of open credit lines and loans
7. Number of times 90 days late
8. Number of real estate loans or lines
9. Number of times 60-89 days past due
10. Number of dependents

The results from LDA highlight the most influential factors in determining credit risk. By focusing on these key attributes, the model becomes more efficient and accurate in predicting creditworthiness.

### 6. Logistic Regression
---

Logistic Regression is a linear model used for binary classification. It estimates the probability that a given input point belongs to a certain class (e.g., good or bad creditor) using a logistic function.

#### 6.1 **Math Intuition:**
Logistic Regression uses a logistic function to model the probability of the default event, ensuring the output is between 0 and 1.

[Link for Logistic Regression](https://www.notion.so/78b29f96413c49a48ae3440b44849871?v=65df3ed276124b33862fa00250bd1029)

### 7. Experimentation and Results
---

The experimentation involved training and testing four machine learning models: Logistic Regression and Decision Trees on a dataset of 7778 customer records from UAE commercial banks. 

The models were evaluated using different sets of attributes and their performance was measured before and after applying Linear Discriminant Analysis (LDA).

#### 7.2 Attributes Used

The attributes used in the models were:
1. Resolving utilization of unsecured lines (P1)
2. Age (P2)
3. Number of times 30-59 days past due (P3)
4. Debt ratio (P4)

The models were tested with different combinations of these attributes:
- **2 attributes:** P1, P2
- **3 attributes:** P1, P2, P3
- **4 attributes:** P1, P2, P3, P4

#### 7.3 Logistic Regression

#### 7.3.1 Without LDA

Logistic Regression, a linear model for binary classification, estimates the probability that a given input point belongs to a certain class using a logistic function. It was evaluated using the raw dataset without dimensionality reduction.

**Results:**
- With 2 attributes: 93.739% accuracy
- With 3 attributes: 92.115% accuracy
- With 4 attributes: 92.522% accuracy

#### 7.3.2 With LDA

**Summary:**
LDA was applied to reduce the dimensionality of the dataset, retaining the most important features while discarding the less significant ones. The transformed dataset was then used to train and test the Logistic Regression model.

**Results:**
- With 2 attributes: 95.026% accuracy
- With 3 attributes: 95.066% accuracy
- With 4 attributes: 95.144% accuracy

### 8. Experimentation and Results Table
---

| Model                | Accuracy Before LDA (%) | Accuracy After LDA (%) |
|----------------------|--------------------------|-------------------------|
|                      | 2 Attributes  | 3 Attributes  | 4 Attributes  | 2 Attributes  | 3 Attributes  | 4 Attributes  |
| Logistic Regression  | 93.739        | 92.115        | 92.522        | 95.026        | 95.066        | 95.144        |
| AdaBoost Classifier  | 92.204        | 92.638        | 93.154        | 95.009        | 95.023        | 95.200        |
| Decision Trees       | 92.488        | 92.455        | 93.451        | 94.921        | 94.918        | 95.042        |
| Neural Network       | 93.291        | 92.007        | 93.633        | 94.985        | 94.999        | 95.186        |

### 9. Conclusion and Further Research
---

The paper investigated the performance of various machine learning models, including Logistic Regression, with and without Linear Discriminant Analysis (LDA) for credit risk assessment. 

It was found that LDA significantly improved the accuracy of the models by reducing the dimensionality of the data and highlighting the most critical attributes.

The attributes used in the models were:
1. **Resolving utilization of unsecured lines (P1):** How much credit is available on credit cards after excluding other debts.
2. **Age (P2):** The age of the borrower.
3. **Number of times 30-59 days past due (P3):** How often payments were late by 30-59 days.
4. **Debt ratio (P4):** The ratio of monthly debt payments to monthly income.

**Results:**
- **Without LDA:**
  - Logistic Regression achieved a maximum accuracy of 93.739% using 2 attributes.
- **With LDA:**
  - Logistic Regression achieved a maximum accuracy of 95.144% using 4 attributes.

| Model                | Accuracy Before LDA (%) | Accuracy After LDA (%) |
|----------------------|--------------------------|-------------------------|
|                      | 2 Attributes  | 3 Attributes  | 4 Attributes  | 2 Attributes  | 3 Attributes  | 4 Attributes  |
| Logistic Regression  | 93.739        | 92.115        | 92.522        | 95.026        | 95.066        | 95.144        |

### 10. Further Research
---

**Exploration of Other Models:**
Future research could explore other advanced machine learning models and compare their performance with and without LDA.

**Real-World Implementation:**
Implementing these models in real-world banking environments could provide further validation and help refine the models based on practical insights.

**Layman Explanation:**
Future studies could test different recipes (models) and see how they perform in a real kitchen (banks). This would help in finding the best approach to make accurate predictions. 👩‍🍳🔬
