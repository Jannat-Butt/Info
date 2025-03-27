# README: URL Classification with Machine Learning

## Project Overview
This project applies **machine learning models** to classify URLs into categories such as **benign, phishing, defacement, malware, and spam**. The dataset is preprocessed, and multiple models, including **Random Forest (RF), XGBoost (XGB), and LSTM**, are trained and evaluated.

## Dataset and Preprocessing
- The dataset contains **665,670 URLs** with extracted features.
- Labels include:
  - **Benign**: 428,103
  - **Defacement**: 96,457
  - **Phishing**: 94,111
  - **Malware**: 32,520
  - **Spam**: 14,479
- Data imbalance is handled using **SMOTETomek**.

## Models Applied
1. **Random Forest (RF)**
2. **XGBoost (XGB)**
3. **Long Short-Term Memory (LSTM)**

## Performance Analysis
### Random Forest (RF):
- **Classification Report:**
  - Achieved the **highest F1-score** across all classes, making it the best-balanced model in terms of precision and recall.
  - Handled class imbalance well, offering **better generalization** compared to XGBoost and LSTM.
- **AUC-ROC Analysis:**
  - **Outperformed both XGBoost and LSTM** across all classes except for one, where XGBoost and RF were equal.
  - Demonstrated **better discriminatory ability** for classifying URLs.

### XGBoost (XGB):
- **Classification Report:**
  - Showed competitive performance but had **lower F1-scores than RF** in most classes.
  - Had slightly better precision but at the cost of recall, impacting the overall balance.
- **AUC-ROC Analysis:**
  - While XGBoost performed well, RF surpassed it in most cases, making RF the better choice overall.

### LSTM:
- **Classification Report:**
  - Performed less than both RF and XGBoost in terms of F1-score and precision.
  - Struggled with training time and computational efficiency.
- **AUC-ROC Analysis:**
  - Had the **lowest AUC-ROC scores across all classes**, making it the least effective model.

## Best Performing Model
**Random Forest (RF) was the best model overall**, as it achieved **higher AUC-ROC values in most cases** and had the **highest F1-score**, making it the most reliable classifier for URL classification. While XGBoost performed well in some cases, RF was the superior model in general. LSTM, despite its sequential learning capabilities, was outperformed by both RF and XGBoost.

## Challenges Faced
- **Class Imbalance**: Addressed using **SMOTETomek**, but some minority classes still had lower performance.
- **Feature Engineering**: Feature importance analysis was needed for further optimization.
- **Hyperparameter Tuning**: Further tuning could improve performance.
- **Computational Cost**: LSTM required significant resources compared to RF and XGBoost.

## Future Improvements
- **Fine-tune hyperparameters** for better model optimization.
- **Explore advanced deep learning architectures** to improve sequential analysis.
- **Optimize LSTM training** to reduce computational overhead.

## Conclusion
This project successfully compared RF, XGB, and LSTM models for URL classification. **Random Forest was the best performer**, consistently achieving **higher AUC-ROC and F1-scores** than XGBoost and significantly outperforming LSTM. Future work can focus on **further tuning RF and exploring lightweight deep learning alternatives** to improve efficiency without compromising accuracy.

