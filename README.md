# Health Risk Prediction Using Transformer Model

## Project Overview 📝

This project predicts various health risks like **Diabetes**, **Cardiovascular Disease**, **Stroke**, and others based on demographic and health-related data. The model uses a **Transformer architecture** to process the data and provides personalized health advice based on predicted risks. The results are visualized using an interactive **Power BI** dashboard for deeper analysis.

## Methodology 🔧

### 1. **Data Collection and Preparation** 📥

- **Dataset Source**: The dataset used is the **Diabetes Health Indicators Dataset** from [Kaggle](https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset).
- **Data Cleaning**: 
    - Categorical columns (e.g., **Smoker**, **Sex**, **Stroke**) were encoded using binary and ordinal mappings.
    - Numerical values were checked for missing data and outliers.
    - **Feature Engineering**: Health risks like **Diabetes**, **Cardiovascular Disease**, **Stroke**, etc., were computed based on various features (e.g., **BMI**, **Blood Pressure**).
  
### 2. **Model Development** 🧠

- **Model**: The **Transformer-based model** is used to predict health risks for each individual.
    - The model is trained on health-related features, including **BMI**, **Age**, **Blood Pressure**, and others.
    - Risk factors were derived using specific thresholds based on medical guidelines.
    - The model provides **Precision**, **Recall**, **F1 Score**, and **ROC AUC** metrics for performance evaluation.
  
### 3. **Power BI Visualization** 💡

- **Power BI Dashboard** was created to interactively visualize health risk data.
- Key visualizations include:
  - **Risk Distribution**: Proportion of diabetic vs non-diabetic individuals.
  - **BMI Distribution**: Visualizing BMI for diabetic vs non-diabetic.
  - **Correlation Analysis**: Exploring the relationships between health metrics like **BMI**, **Blood Pressure**, and **Cholesterol**.

---

## **Results** 🎯

The analysis provides the following insights:
1. **Risk Distribution**: Diabetic individuals are more likely to have **high BMI** and **high blood pressure**.
2. **Obesity Risk**: Individuals with BMI > 30 are at a higher risk for diabetes and cardiovascular diseases.
3. **Health Advice**: Based on the model predictions, personalized advice is generated for each individual.

## **Conclusion** 🏁

This project demonstrates how machine learning, particularly **Transformers**, can be used to predict health risks and provide actionable insights. The **interactive Power BI dashboard** allows users to explore the predictions and visualize key health metrics.

---

## **Dashboard For Summary** 📸

![Power BI Dashboard](https://example.com/your-dashboard-image)

---

## **Installation and Setup** 💻

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repository.git
    ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the preprocessing and training scripts:
    ```python
    data_preprocess().run()
    model = main()
    model.run()
    ```

## **Terminal Output Logs** 💻

Here is the output log after running the model:

```bash
...
Total Loss: 0.4554
Row 0 - Combined Risk: 0.620, Status: Diseased
...
