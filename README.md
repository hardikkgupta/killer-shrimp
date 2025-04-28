# killer-shrimp

Predicts the presence of *Dikerogammarus villosus* using five environmental variables.

## Method in 4 Steps
1. **Missing-value imputation** – `IterativeImputer` (10 iters, random_state = 0).  
2. **Feature engineering** – 15 new features:  
   * Ocean-density physics  
   * 9 EUNIS exposure dummies + “Min Very Exposed” flag  
   * Temperature-risk polynomial  
   * Bounded-box outlier flag  
3. **Model** – XGBoost (`learning_rate 0.3`, `max_depth 5`, `reg_lambda 0.5`).  
4. **Evaluation** – Stratified 5-fold CV + leaderboard submission; predictions saved to `preds.csv`.

## Quick start
Run the notebook

(Recently imported from my Kaggle)