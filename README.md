# Trustworthy-AI-for-LOS-Prediction-in-Ortho

Trustworthy and explainable AI framework for predicting hospital length of stay (LOS) following orthopedic inpatient surgery.


## Table of Contents
- [Abstract](#abstract)
- [Directory Descriptions](#directory-descriptions)
- [The Proposed Computational Pipeline](#the-proposed-computational-pipeline)
- [Explainable AI: Clinical App Interface](#explainable-ai-clinical-app-interface)
- [Data Availability](#data-availability)
- [Publications](#publications)
- [Acknowledgments](#acknowledgments)
- [Citation](#citation)



### Abstract
<p align="justify">This GitHub repository contains the full implementation of a trustworthy, uncertainty-aware, and explainable artificial intelligence (AI) framework for predicting prolonged hospital length of stay (LOS) following orthopedic inpatient surgery.</p>

<p align="justify">Hospital LOS was formulated as a binary classification task using two clinically relevant thresholds (LOS ≤ 2 vs. LOS > 2 days and LOS ≤ 5 vs. LOS > 5 days), with primary emphasis on the 5-day cutoff due to its greater clinical interpretability and stability across orthopedic procedures.</p>

<p align="justify">The framework relies exclusively on preoperative patient demographics, comorbidities, laboratory values, and procedural characteristics derived from the American College of Surgeons National Surgical Quality Improvement Program (ACS-NSQIP) database (2021–2023).</p>

<p align="justify">The proposed approach integrates machine learning–based risk prediction with uncertainty quantification, calibration analysis, algorithmic fairness assessment across age, sex, and race subgroups, and explainability using SHapley Additive exPlanations (SHAP) and Local Interpretable Model-Agnostic Explanations (LIME). The resulting framework is designed to support transparent, equitable, and clinically actionable decision-making in orthopedic surgery.</p>



### Directory Descriptions
- <p align="justify"><strong>Code:</strong> Python scripts and Jupyter notebooks for data preprocessing, model training, cross-validation, performance evaluation, uncertainty analysis, fairness assessment, and explainability.</p>

- <p align="justify"><strong>Dataset:</strong> Description files documenting the structure and variables of the ACS-NSQIP dataset used in this study. Raw clinical data are not included due to data use restrictions.</p>

- <p align="justify"><strong>Figures:</strong> Figures and visualizations generated for the study, including SHAP summaries, local explainability plots (SHAP and LIME), cohort characteristics, and application screenshots.</p>

- <p align="justify"><strong>Models:</strong> Trained machine learning models (including the optimized XGBoost model) and related configuration files.</p>



### The Proposed Computational Pipeline
<p align="center">
  <img src="Figures/LOS_Cohort_5_2.png" alt="Study cohort and LOS outcome definition" width="700"/>
</p>


<p align="center"> 
  <img src="Figures/cutoff_5.png" alt="SHAP Summery for cutoff 5" width="400"/> 
  <img src="Figures/cutoff_2.png" alt="SHAP Summery for cutoff 2" width="400"/> 
</p>


<p align="justify">
The computational pipeline consists of cohort construction from the ACS-NSQIP registry (2021–2023), preoperative feature extraction, binary LOS outcome definition using two clinically relevant thresholds (LOS &gt; 2 days and LOS &gt; 5 days, with primary emphasis on the 5-day cutoff), supervised machine learning model training with five-fold stratified cross-validation, uncertainty quantification via bootstrap confidence intervals, probabilistic calibration analysis, subgroup-level fairness evaluation across age, sex, and race, and global and local explainability using SHAP and LIME.
</p>




### Explainable AI: Clinical App Interface
<p align="center">
  <img src="Figures/Local_SHAP.png" alt="Local SHAP Explanation" width="800"/>
</p>

<p align="center">
  <img src="Figures/Global_SHAP.png" alt="Global SHAP Feature Importance" width="400"/>
  <img src="Figures/Local_LIME.png" alt="Local LIME Explanation" width="400"/>
</p>

<p align="justify">
A clinician-facing decision-support interface was developed using Streamlit to enable interactive exploration of model predictions. The application displays the predicted probability of prolonged LOS together with global feature importance and patient-specific explanations.
</p>

<p align="justify">
The interface supports model selection, patient-level inspection, and visualization of contributing factors, facilitating preoperative risk stratification while preserving clinician oversight and judgment.
</p>



### Data Availability
<p align="justify">
The clinical data used in this study were obtained from the American College of Surgeons National Surgical Quality Improvement Program (ACS-NSQIP).
</p>

<p align="justify">
Due to data use agreements and patient privacy protections, the raw NSQIP dataset cannot be shared publicly. This repository provides all source code, trained models, and documentation necessary to reproduce the analyses for authorized users with appropriate data access.
</p>



### Publications<p align="justify">
<strong>Trustworthy AI Models to Predict Prolonged Hospital Length-of-Stay in Orthopedic Surgery</strong>, 
manuscript under review at 
<a href="https://www.nature.com/npjhealthsyst/" target="_blank">
<i>npj Health Systems</i>
</a>, 2026.
</p>


### Acknowledgments
<p align="justify">
The authors gratefully acknowledge the American College of Surgeons and the National Surgical Quality Improvement Program (ACS-NSQIP) for providing access to the clinical dataset used in this research.
</p>



### Citation
<p align="justify">
If you use this repository or any part of this work in your research, please cite:
</p>

<p align="justify">
Rezvani, Farnaz; Kann, Michael; Gao, Fengyi; Myers, Nicole; Kashefi, Armin; Visweswaran, Shyam; Wang, Yanshan; Hogan, MaCalus V.; Plate, Johannes F.; Tafti, Ahmad P.<br/>
<i>Trustworthy AI Models to Predict Prolonged Hospital Length-of-Stay in Orthopedic Surgery</i>, 2026.
</p>

<p align="center">
  <a href="https://pitthexai.github.io/index.html" target="_blank">
    <img src="Figures/Pitthexai_QR.jpg" alt="Pitt HexAI QR Code" width="200"/>
  </a><br/>
  <b>Pitt Health + Explainable AI (Pitt HexAI) Research Laboratory</b>
</p>
