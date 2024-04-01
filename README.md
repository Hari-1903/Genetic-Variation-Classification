# Genetic-Variation-Classification
The presence of conflicting classifications among genetic variants in ClinVar presents a significant challenge for accurate interpretation by clinicians and researchers. This study addresses this issue by developing a predictive model to differentiate variants with conflicting classifications from those with consistent classifications. Leveraging a dataset containing annotations on human genetic variants, the 'CLASS' target variable denotes the presence (1) or absence (0) of conflicting classifications. Through the utilization of four classifier models (RandomForest, KNN, Decision Tree, logistic regression), trained and evaluated based on metrics such as accuracy and F1-score, the study aims to identify the best-performing algorithm to improve variant interpretation in both clinical and research settings. 
<br>
<br>The Dataset for this File is taken from https://www.kaggle.com/datasets/kevinarvai/clinvarconflicting

## Approach
- **Data Exploration**: The dataset, obtained from Kaggle and originating from ClinVar, is explored to understand its structure, features, and target variable distribution.
- **Data Preprocessing**: Preprocessing steps are performed to handle missing values, encode categorical variables, and prepare features for model training.
- **Model Selection**: Four classifier models—K-Nearest Neighbors (KNN), Random Forest, Logistic Regression and Decision Tree-are selected to predict conflicting classifications. Each model is trained, evaluated, and compared based on performance metrics.
- **Model Evaluation**: Model performance is assessed using metrics such as accuracy, precision, recall, and F1-score. Confusion matrices are analyzed to understand the models' predictive capabilities.
- **Model Optimization**: Hyperparameter tuning techniques, such as grid search or random search, are applied to optimize the selected models for improved performance.
- **Final Model Selection**: Based on evaluation results, the best-performing algorithm is identified to accurately predict the presence of conflicting classifications in ClinVar variants, facilitating informed decision-making in clinical and research settings.

## Results
Looking at the results, the **Random Forest (RF)** model demonstrates the highest precision (0.782) and recall (0.249), indicating its ability to make accurate **positive predictions** and capture positive instances effectively. Additionally, the F1-score for RF (0.842) is relatively high, indicating a good balance between precision and recall. Comparatively, logistic regression (LR) shows relatively high precision (0.748) but very low recall (0.001), resulting in a low F1-score (0.856). Decision Tree (DT) and K-nearest neighbors (KNN) also exhibit lower F1-scores
compared to RF.
Therefore, based on these metrics, the Random Forest model appears to be the most suitable for genetic variation detection, as it achieves a good balance between precision and recall,
resulting in a high F1-score.

## Future Developments
Future developments for this project could include exploring more advanced machine learning algorithms, such as gradient boosting machines or neural networks, to potentially improve model performance. Additionally, incorporating domain-specific features or leveraging external datasets could enhance the predictive power of the models. Furthermore, implementing techniques like **ensemble** learning or model **stacking** could be beneficial for combining the strengths of multiple models. Finally, continuous monitoring and updating of the models with new data could ensure that they remain accurate and relevant over time.
