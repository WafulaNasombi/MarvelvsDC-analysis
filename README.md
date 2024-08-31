# Predicting Superhero Battle Outcomes
## Beginning
### Overview
This project aims to predict the outcomes of battles between superheroes and villains from Marvel and DC Comics. Using a dataset that includes character attributes such as strength, speed, intelligence, special abilities, and weaknesses, we build predictive models to forecast battle results. This analysis can assist Marvel Studios and DC in scripting their final showdown movie by identifying which characters are most likely to win.

## Business and Data Understanding
### Business Objective:
Marvel Studios and DC want to create an epic showdown movie between their characters. To script the most thrilling and believable battles, they need to predict which characters are most likely to win based on their attributes. This analysis will provide strategic insights into character selection and battle outcomes.

### Data Description:
The dataset is from Kaggle and contains various attributes of Marvel and DC characters, including:

  - Character: The name of the character.eg Spiderman, Superman, Thor,Captain America.
  - Universe: Marvel or DC.
  - Strength: A numerical representation of the   character's strength.(between 0 and 10)
  - Speed: A numerical representation of the character's speed.(between 0 and 10 )
  - Intelligence: A numerical representation of the character's intelligence.(between 0 and 10)
  - SpecialAbilities: Involves a range of abilities eg SuperStrength, Telekinesis,Flight,Invisibility.
  - Weaknesses: Involves Kryptonite, Wooden Stake, Magic, Silver.
  - BattleOutcome: The binary target variable indicating win (1) or loss (0).

### Modeling
After data cleaning data was scaled then split into training and testing data and afterwards, models were built.
To predict battle outcomes, we built four different models:

  1. Logistic Regression
  2. Decision Tree
  3. Random Forest
  4. Support Vector Machine (SVM)



Modeling was done before hyperparameter tuning and class balancing and after hyperparameter tuning and class balancing.

## Evaluation
### Model Evaluation Metrics:
Metrics used to evaluate the models were:
   *  **Accuracy:** Measures the percentage of correct predictions.
   * **F1 Score:** Considers both precision and recall, giving a balanced measure of a model's performance.
   * **Precision:** The proportion of positive identifications that were actually correct.
   * **Recall:** The proportion of actual positives that were identified correctly.
   * **ROC Curve and Area under Curve** : To see the percentage at which the top models can correctly differentiate between  the true positives and false positives.
- Before hyperparameter tuning and y class being imbalanced the results were:

| Model                   | Accuracy | Precision | Recall   | F1 Score |
|-------------------------|----------|-----------|----------|----------|
| Logistic Regression     | 0.768836 | 0.759247  | 0.768836 | 0.762934 |
| Decision Tree           | 0.666096 | 0.698378  | 0.666096 | 0.678596 |
| Random Forest           | 0.758562 | 0.755001  | 0.758562 | 0.756665 |
| Support Vector Machine  | 0.787671 | 0.773629  | 0.787671 | 0.776150 |

- SVM showing higher results compared to the other models.
- After hyperparameter tuning and class balancing using SMOTE algorithm:

| Model                   | Accuracy | Precision | Recall   | F1 Score |
|-------------------------|----------|-----------|----------|----------|
| Logistic Regression    | 0.669521 | 0.759375  | 0.669521 | 0.689787 |
| Decision Tree           | 0.683219 | 0.711643  | 0.683219 | 0.694281 |
| Random Forest           | 0.732877 | 0.753872  | 0.732877 | 0.740934 |
| Support Vector Machine  | 0.683219 | 0.761296  | 0.683219 | 0.702120 |

- Random forest showing better results compared to the other models. With it's ROC curve and AUC looking like this:
![alt text](images/roc%20curve%20rf.png)

- while the logistic regression roc curve and auc looked like this:
![alt text](images/roc%20curve%20logreg.png)

### Conclusion 
Based on the analysis, the Random Forest model emerged as the most robust model for predicting superhero battle outcomes. It provides a good balance of accuracy and other performance metrics, making it suitable for the project’s needs. This model can help Marvel Studios and DC in crafting realistic and engaging battle scenes by identifying which characters are likely to emerge victorious based on their attributes.


