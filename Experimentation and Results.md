### Experimentation and Results: Logistic Regression (with and without LDA)

#### Overview of Experimentation and Results

The experimentation involved training and testing four machine learning models: Logistic Regression, AdaBoost Classifier, Decision Trees, and Neural Networks on a dataset of 7778 customer records from UAE commercial banks. The models were evaluated using different sets of attributes and their performance was measured before and after applying Linear Discriminant Analysis (LDA).

#### Attributes Used

The attributes used in the models were:
1. Resolving utilization of unsecured lines (P1)
2. Age (P2)
3. Number of times 30-59 days past due (P3)
4. Debt ratio (P4)

The models were tested with different combinations of these attributes:
- **2 attributes:** P1, P2
- **3 attributes:** P1, P2, P3
- **4 attributes:** P1, P2, P3, P4

**Layman Explanation:**
Imagine you're baking cookies and you decide to test different combinations of ingredients to see which one makes the best cookies. Here, the ingredients (attributes) are the financial factors like age and debt ratio, and the models are the recipes.

### Logistic Regression

#### Without LDA

**Summary:**
Logistic Regression, a linear model for binary classification, estimates the probability that a given input point belongs to a certain class using a logistic function. It was evaluated using the raw dataset without dimensionality reduction.

**Results:**
- With 2 attributes: 93.739% accuracy
- With 3 attributes: 92.115% accuracy
- With 4 attributes: 92.522% accuracy

**Layman Explanation:**
Logistic Regression is like drawing a line to separate apples from oranges. Without LDA, it directly uses the raw data to draw this line.

#### With LDA

**Summary:**
LDA was applied to reduce the dimensionality of the dataset, retaining the most important features while discarding the less significant ones. The transformed dataset was then used to train and test the Logistic Regression model.

**Results:**
- With 2 attributes: 95.026% accuracy
- With 3 attributes: 95.066% accuracy
- With 4 attributes: 95.144% accuracy

**Layman Explanation:**
Using LDA is like sorting the ingredients to find the best combination before making the cookies. This helps the model (recipe) focus on the most important features, leading to better performance.

### Importance and Context

**Importance:**
The application of LDA significantly improved the accuracy of the Logistic Regression model. This indicates that dimensionality reduction helps in simplifying the data and highlighting the most critical factors, leading to more accurate predictions.

**Context:**
In the context of credit risk assessment for UAE’s commercial banks, using LDA can help in efficiently identifying the most important financial attributes that determine a borrower’s creditworthiness. This results in better decision-making and reduces the risk of financial losses.

### Math Intuition and Terminologies

**Logistic Regression:**
- **Logistic Function:** A function that models the probability of a binary outcome. It outputs a value between 0 and 1, representing the probability of belonging to a certain class.
\[ \sigma(z) = \frac{1}{1 + e^{-z}} \]
- **Linear Model:** A model that makes predictions based on a linear combination of input features.

**Linear Discriminant Analysis (LDA):**
- **Dimensionality Reduction:** The process of reducing the number of input variables in a dataset, focusing on the most important ones.
- **Between-Class Scatter Matrix (S_B):** Measures the spread of the means of different classes.
- **Within-Class Scatter Matrix (S_W):** Measures the spread of samples within each class.
- **Transformation Matrix (W):** Projects the data onto a lower-dimensional space that best separates the classes.

### Experimentation and Results Table

| Model                | Accuracy Before LDA (%) | Accuracy After LDA (%) |
|----------------------|--------------------------|-------------------------|
|                      | 2 Attributes  | 3 Attributes  | 4 Attributes  | 2 Attributes  | 3 Attributes  | 4 Attributes  |
| Logistic Regression  | 93.739        | 92.115        | 92.522        | 95.026        | 95.066        | 95.144        |
| AdaBoost Classifier  | 92.204        | 92.638        | 93.154        | 95.009        | 95.023        | 95.200        |
| Decision Trees       | 92.488        | 92.455        | 93.451        | 94.921        | 94.918        | 95.042        |
| Neural Network       | 93.291        | 92.007        | 93.633        | 94.985        | 94.999        | 95.186        |

**Layman Explanation:**
This table is like a scoreboard showing how well each recipe (model) performed with different combinations of ingredients (attributes). The scores (accuracies) are higher after sorting the ingredients using LDA, indicating better performance.

### Conclusion

The results show that applying LDA improves the accuracy of credit risk assessment models. For Logistic Regression, the accuracy increased significantly with LDA, demonstrating the importance of dimensionality reduction in machine learning. By focusing on the most relevant features, banks can make better lending decisions, reducing the risk of defaults and financial losses.

By leveraging LDA, UAE’s commercial banks can enhance their credit risk assessment processes, leading to more accurate and reliable predictions. This ultimately helps in minimizing financial risks and improving the stability and profitability of the banking sector.

