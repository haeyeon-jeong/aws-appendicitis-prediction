# AWS Pediatric Appendicitis Prediction

## Authors

- Abirham Getie  
- Haeyeon Jeong  
- Yonathan Shimelis  

---

## Project Overview

This project builds an end-to-end cloud-based machine learning pipeline using AWS to predict pediatric appendicitis. The system integrates data storage, model training, and visualization using AWS services to enable collaborative and scalable machine learning workflows.

---

## Objective

- Predict pediatric appendicitis using clinical data  
- Build a fully cloud-based ML pipeline  
- Enable team collaboration using AWS services  

---

## Dataset

- Source: UCI Machine Learning Repository (Regensburg Pediatric Appendicitis Dataset)
  https://archive.ics.uci.edu/dataset/938/regensburg+pediatric+appendicitis 
- Size: 782 rows, 53 features  
- Target: Diagnosis (Appendicitis / No Appendicitis)  

### Key Features
- White Blood Cell (WBC)
- C-reactive protein (CRP)
- Appendix diameter
- Ultrasound findings  

---

## AWS Architecture

The project uses a cloud-based architecture for collaboration and scalability:

- **Amazon S3**  
  - Central storage for datasets, models, results, and visuals  

- **Amazon EC2 (Shared AMI + Jupyter Notebook)**  
  - Environment for preprocessing and model training  

- **IAM Policies**  
  - Enable secure cross-account access for team collaboration  

The pipeline follows:  
**Data Load → Preprocess → Model → Evaluate → Visualize**

---

## Workflow

### Data Engineer
- Upload dataset to S3  
- Configure IAM policies  
- Set up shared EC2 environment  

### Data Scientist
- Load data from S3  
- Preprocess data  
- Train models using AutoML  
- Save results to S3  

### Data Analyst
- Retrieve results from S3  
- Create visualizations  
- Upload outputs back to S3  

---

## Results & Key Findings

- Best model: **Histogram Gradient Boosting Classifier**  
- Performance: **F1 Macro ≈ 0.95** 

### Key Insights
- Appendix diameter, WBC, and CRP are strong predictors  
- AWS enables scalable and collaborative ML workflows  
- S3 replaces local file sharing for team-based work  

---

## How to Run

1. Open the notebooks inside:
- `Codes/`

2. Ensure AWS setup:
- Access to S3 bucket  
- EC2 instance with Jupyter  

3. Run notebooks in order:
- `1_data_prep.ipynb`  
- `2_Modeling.ipynb`  
- `CC-final-visualizationcode.ipynb`  

---

## Presentation

- [Presentation PDF](./report/aws-appendicitis-prediction.pdf)  
- [Presentation Slides](./report/aws-appendicitis-prediction.pptx)  

The PPT version includes embedded demo videos showcasing the workflow:
- Page 5: Data Engineer workflow  
- Page 6: Data Scientist workflow  
- Page 7: Data Analyst workflow
  
---

## Tools & Technologies

- AWS (S3, EC2, IAM)  
- Python  
- Jupyter Notebook  
- PyCaret (AutoML)  
- Pandas, NumPy, Matplotlib  

---

## Conclusion

- Successfully built an end-to-end AWS ML pipeline  
- Enabled collaborative machine learning using cloud infrastructure  
- Achieved high model performance with AutoML  
- Demonstrated scalable and reproducible workflow  



