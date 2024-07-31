### Data Collection and Variable Definition

The Data Collection and Variable Definition section is crucial in setting up the framework for any machine learning model, including the credit risk assessment model for UAE’s commercial banks. This section outlines how data is gathered and the specific variables that are used to predict credit risk. Here is a detailed breakdown with layman explanations, the importance and context, and explanations of relevant terminologies.

#### Data Collection

**Summary:**
The dataset used in this study comprises both accepted and rejected loan applications from different commercial banks in the UAE, collected from the years 2016 to 2018. The data consists of 7778 cases. Out of these, 292 applications (59.3%) were deemed creditworthy, while 200 applications (40.3%) were not.

**Layman Explanation:**
Imagine you are collecting report cards from different schools to find out which students passed or failed over three years. Similarly, the researchers collected loan applications from various banks over three years to see which ones were approved (passed) and which ones were rejected (failed). 📄🏦

**Importance and Context:**
Collecting a diverse and comprehensive dataset is essential for building a robust machine learning model. The data must represent various scenarios to ensure the model can generalize well to new, unseen data. In this context, having data from multiple banks over several years helps capture different economic conditions and lending practices, making the model more reliable.

#### Variables Definition

**Summary:**
The dataset includes 11 variables: 10 input variables and 1 output variable. These variables are defined, coded, and described in detail to ensure clarity in the model-building process.

**Layman Explanation:**
Think of the variables as different pieces of information you gather about each student, like their age, grades in different subjects, and attendance record. In the same way, these variables provide information about each loan applicant. 📊📋

**Variable Definitions and Explanations:**

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

**Math Intuition:**

- **Scale Variables:** These are continuous variables that can take any value within a range. They provide detailed information about the borrower’s financial status.
- **Binary Variables:** These are categorical variables with two possible outcomes (good or bad creditor). They simplify the classification task for the machine learning model.

### Importance and Context

**Data Collection:**
Gathering data from multiple banks over several years ensures the model is trained on a variety of scenarios, improving its ability to generalize and make accurate predictions on new data. This comprehensive dataset is crucial for building a robust model that can handle different economic conditions and lending practices. 📅🏦

**Variable Definition:**
Clearly defining and coding variables helps ensure that the data is consistently interpreted and used in the model. This clarity is essential for the model to understand and learn from the data effectively. Properly defined variables also make it easier to preprocess the data and implement machine learning algorithms. 📊🛠️

### Terminologies

- **Debt Ratio:** A measure of a borrower’s debt compared to their income, indicating their ability to manage additional debt.
- **Log-Transformation:** A mathematical transformation applied to data to manage wide variations and make patterns more evident.
- **EMI (Equated Monthly Installment):** A fixed payment amount made by a borrower to a lender at a specified date each calendar month.

By understanding the data collection process and the definition of variables, we can ensure that the machine learning model is built on a solid foundation. This leads to more accurate predictions, helping banks make better lending decisions and reduce financial risk. 🏦🤖📈4

## **Table of Contents:**
---
1. [Abstract](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach)
   
2. [Introduction](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Introduction.md) 

4. [Related Work](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Related%20Work.md) 

5. [Data Collection and Variable Definition](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Data%20Collection%20and%20Variable%20Definition.md) 

6. [Methodology](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Methodology.md)

7. [Data Reduction Using Linear Discriminant Analysis (LDA)](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Data%20Reduction%20Using%20Linear%20Discriminant%20Analysis%20(LDA).md)

8. [Experimentation and Results](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Experimentation%20and%20Results.md)

9. [Conclusion and Further Research](https://github.com/aditya-saxena-7/Credit-Risk-Assessment-Model-for-UAE-s-Commercial-Banks-A-Machine-Learning-Approach/blob/main/Conclusion%20and%20Further%20Research.md)
