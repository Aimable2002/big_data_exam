## 📊 Power BI Dashboard

You can view the Power BI report here:  
[Power BI Dashboard on Google Drive](https://drive.google.com/file/d/1f9tJoaxXQJvSwOdzeFRTG5yaW2eIgIad/view?usp=sharing)


# Health Risk Prediction Using Transformer Model

## Project Overview 📝

This project predicts various health risks like **Diabetes**, **Cardiovascular Disease**, **Stroke**, and others based on demographic and health-related data. The model uses a **Transformer architecture** to process the data and provides personalized health advice based on predicted risks. The results are visualized using an interactive **Power BI** dashboard for deeper analysis.

## Methodology 🔧

### 1. **Data Collection and Preparation** 📥

- **Dataset Source**: The dataset used is the **Diabetes Health Indicators Dataset** from [UCI Machine Learning](https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators)
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

![Smokers](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/smokers.png)

*This chart visualizes the average of smokers*

![Diabets_binary](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/Diabetes_binary.png)

*This chart visualizes the diabets binary contributions*

![High blood pressure](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/HighBP.png)

*This chart visualizes average of High blood pressure*

![BMI](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/BMI.png)

*This chart visualizes average of BMI*

![BMI](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/Diabets_binary.png)

*This chart visualizes average of diabets_binary by both male and female and BMI by diabet*

![BMI](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/Heart.png)

*This chart visualizes average of heartAttack by income and age*

![correletion_heatmap](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/Correlation_Heatmap.png)

*This chart visualizes the relationship by correlation-heatmap*

![Dashboard](https://raw.githubusercontent.com/Aimable2002/big_data_exam/main/dashboard.png)

*This chart visualizes dashboard summary*

---

## **Installation and Setup** 💻

1. Clone the repository:
    ```bash
    https://github.com/Aimable2002/big_data_exam.git
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
Successfully save the powerBI csv file
torch.Size([300])
train predictions
 tensor([[0.7234, 0.5000, 0.5000,  ..., 0.5954, 0.5000, 0.6135],
        [0.7391, 0.3602, 0.5086,  ..., 0.5000, 0.4557, 0.5980],
        [0.7864, 0.5000, 0.5324,  ..., 0.4298, 0.5000, 0.6405],
        ...,
        [0.7463, 0.3252, 0.5420,  ..., 0.4159, 0.3485, 0.5775],
        [0.7148, 0.3564, 0.5347,  ..., 0.5000, 0.4200, 0.5000],
        [0.7181, 0.2808, 0.5273,  ..., 0.4098, 0.5000, 0.6364]],
       grad_fn=<SqueezeBackward1>)
output reached in metrics tensor([[0.7234, 0.5000, 0.5000,  ..., 0.5954, 0.5000, 0.6135],
        [0.7391, 0.3602, 0.5086,  ..., 0.5000, 0.4557, 0.5980],
        [0.7864, 0.5000, 0.5324,  ..., 0.4298, 0.5000, 0.6405],
        ...,
        [0.7463, 0.3252, 0.5420,  ..., 0.4159, 0.3485, 0.5775],
        [0.7148, 0.3564, 0.5347,  ..., 0.5000, 0.4200, 0.5000],
        [0.7181, 0.2808, 0.5273,  ..., 0.4098, 0.5000, 0.6364]],
       grad_fn=<SqueezeBackward1>)
target reached in metrics tensor([[0., 0., 0.,  ..., 0., 0., 0.],
        [0., 0., 0.,  ..., 0., 0., 0.],
        [0., 0., 0.,  ..., 0., 0., 0.],
        ...,
        [0., 0., 0.,  ..., 0., 0., 0.],
        [0., 0., 0.,  ..., 0., 0., 0.],
        [0., 0., 0.,  ..., 0., 0., 0.]])
====================================================================================================

Last risk dictionary:

{'row_risk': {'target': 0.7180678844451904, 'diabetes_risk': 0.28078845143318176, 'heart_disease_risk': 0.5273335576057434, 'cancer_risk': 0.8171169757843018, 'ckd_risk': 0.28835317492485046, 'stroke_risk': 0.4325588345527649, 'obesity_risk': 0.4098053574562073, 'mental_health_risk': 0.5, 'liver_disease_risk': 0.6364028453826904}, 'combined_risk': 0.5122696757316589, 'status': 1, 'precision': 0.5, 'recall': 0.3333333333333333, 'f1_score': 0.4}
Training Summary:
Total Loss: 0.1431

Health Advice for Last Patient:
heart_disease_risk: Keep good health congz
cancer_risk: Reduce smoking and alcohol, get regular screenings.
mental_health_risk: Seek mental health support and manage stress.
liver_disease_risk: Keep good health congz
...
