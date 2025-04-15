<div style="text-align: center;">
  <img src="/images/hernan_hsu_healy.png" width="400" height="350">
</div>

*Source: [A Second Chance to Get
Causal Inference Right:
A Classification of Data
Science Tasks](https://content.sph.harvard.edu/wwwhsph/sites/1268/2019/04/hernan_chance19.pdf)*

# Traditional vs Causal Analytics

![License](https://img.shields.io/badge/license-MIT-blue.svg) <!-- Update the license badge as needed -->

Capstone research project for my M.Sc. in Data Analytics

The full research project report as submitted to my college is included [Here](Thesis_Milo_Moran.pdf)

---

## Table of Contents

- [Description](#description)
- [Methodology](#methodology)
- [Technologies](#technologies)
- [Repository_Contents](#repository_contents)
- [Acknowledgments](#acknowledgments)

---

## Description

My project  was motivated largely by [This Article](https://content.sph.harvard.edu/wwwhsph/sites/1268/2019/04/hernan_chance19.pdf), and investigates the intersection and divergence of causal inference and traditional(descriptive, predictive) analytics using a dataset of student grades and background information.
The goal was to determine whether causal inference methods could complement traditional predictive analytics by providing deeper insights into
the relationships between features (e.g., study habits, family background) and student performance outcomes.




This project serves as proof of concept for the use of causal inference to investigate educational attainment: Schools or universities could use this approach to identify actionable factors (e.g., study habits, parental education) that influence student performance and design targeted interventions. Policy makers could also leverage these causal insights to allocate resources more effectively.

The small size of the dataset may have introduced some limitations to the validity of the result, and the DAG was designed based primarily on untested assumptions, which also isn't conducive to the generalisability of the results, so it would be recommended not to assume the findings are true for other contexts.

For future research in the same vein, a larger dataset would greatly improve reliability of the results. Incorporating further causal inference techniques could also strengthen the results. Treatment of variables could also be revised to ensure interpretability and further increase validity

---
 
 ## Methodology
  - I explored the data extensively using statistical testing and visualisations, to measure correlations with the dependent variable and understand distributions of features respectively.
  - Performed sensitivity analysis to remove features unlikely to contribute to models or have causal effects, and then heavily engineered the remaining features to ensure they could be used for machine learning and interpreted.
  - Ran three different classifier models to predict student grades(DT, SVM, XGBoost), and used a range of different tuning methods on the models to maximise accuracy.
  - Used feature importance metrics to determine which features had the biggest influence on the models.
  - Created a DAG to describe any potential causal relationships I would expect between features.
  - Measured Average Treatment Effects for various features on the dependent variable, as suggested by the feature importance metrics and the correlational tests.
  - Performed statistical tests to compare the ATEs with the descriptive and predictive methods of investigation
  - Found that the addition of causal inference highlighted different features as being important compared to the traditional methods
  
---

## Technologies

The project uses the following technologies:

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- DoWhy
- Scipy
- Bayes_opt


---
## Repository_Contents

- notebooks - All the code for the project, as jupyter notebooks
- images - Any images that are part of the repository
- docs-appendices - Some documents where information about features and feature management decisions were tracked
- Thesis_Milo_Moran.pdf - The final research project submisssion made for the master's research project module
- README.md - This wonderful readme file
- LICENSE - MIT license

--- 

## Acknowledgments
I would like to thank James Garza for his supervision, support, and feedback throughout my project.  
