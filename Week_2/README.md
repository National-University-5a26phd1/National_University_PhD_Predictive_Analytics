# Predictive Analytics - Week 2 Assignment

> By: **Todd DeLozier, MBA, Data+**
> Course: **DDS-8555 : Predictive Analysis**
> School: **National University PhD Data Science**

### Personal Note on Assignment Structure and Approach

The structure of this assignment reflects a hybrid evaluation design that integrates conceptual understanding, applied statistical modeling, and practical implementation within a competitive data science context. While each component independently targets a distinct competency, the overall organization may appear fragmented due to the absence of a single unifying analytical workflow.

Specifically, the assignment combines theoretical questions from *An Introduction to Statistical Learning with Applications in Python* (James et al., 2023), applied regression modeling using the Carseats dataset, and a real-world modeling exercise through the Kaggle Abalone competition. These elements represent progressively increasing levels of abstraction, moving from interpretation of predefined models to independent model construction and evaluation.

To address this structural dispersion, a deliberate separation of concerns was implemented. All computational work, including data preprocessing, model development, assumption testing, and evaluation, is presented within a Jupyter Notebook. This format allows for reproducibility, transparency, and alignment with modern data science workflows. 

In parallel, a written document was developed to explicitly present the conceptual and applied questions, along with their corresponding answers and interpretations. This document focuses on articulating statistical reasoning, interpreting model outputs, and connecting findings to theoretical foundations.

This bifurcated approach ensures that both technical execution and analytical interpretation are clearly communicated, while maintaining coherence across the assignment’s diverse requirements.

## Assignment Instructions

# Assignment 2: Build Regression Models

**Course:** DDS-8555 v1: Predictive Analysis  
**Student:** Todd DeLozier, MBA, Data+  
**Due Date:** February 22, 2026, 11:59 PM  
**Submission:** Turnitin Enabled  

---

## Background

This week, you will build regression models using various types of variables. You are required to interpret the output of the models and provide references supporting your interpretation.

Specifically, you must investigate the typical assumptions of regression, including:

- Linearity  
- Independence of errors  
- Collinearity of variables  
- Distribution of residuals  

---

## Instructions

### Part 1: Conceptual
- Complete **Conceptual Question #3** on pages **128–129** of *ISLR Python*.

### Part 2: Applied
- Complete **Applied Question #10** on page **130** of *ISLR Python*.

### Part 3: Kaggle Competition
- Participate in the **Regression with Abalone Dataset** competition on Kaggle.
- Build **at least two regression models** and submit them for evaluation.
- Requirements:
  - Interpret regression model outputs  
  - Provide your code  
  - Provide evidence of successful submission to Kaggle  
  - Investigate regression assumptions  
  - Interpret all findings  

---

## Length Requirement

- **1-page written document**
- **Python Notebook must be included and shared**

---

## References

Include **3 scholarly resources** that address:

1. Previous and recent work on the topic  
2. Theoretical considerations  
3. Applications  

---

## Grading

- Total Points: **10**
- Refer to rubric below for detailed grading criteria

---

## Rubric: Assignment 2 Grading Rubric

| Criteria                                      | Meets Requirement (1 pt) | Partially Meets (0.5 pt) | Does Not Meet (0 pts) |
|----------------------------------------------|--------------------------|--------------------------|------------------------|
| Completes Conceptual Question                | 1                        | 0.5                      | 0                      |
| Completes Applied Question                  | 1                        | 0.5                      | 0                      |
| Submits First Model to Kaggle               | 1                        | 0.5                      | 0                      |
| Submits Second Model to Kaggle              | 1                        | 0.5                      | 0                      |
| Provides Evidence of Submissions            | 1                        | 0.5                      | 0                      |
| Investigates All Assumptions                | 1                        | 0.5                      | 0                      |
| Posts Code to GitHub                       | 1                        | 0.5                      | 0                      |
| Provides 3 References (Methods/Content)     | 1                        | 0.5                      | 0                      |
| Discussion is Generally Free of Errors      | 1                        | 0.5                      | 0                      |
| APA Formatting + Required Length           | 1                        | 0.5                      | 0                      |

**Total Possible Score:** 10 points

## Submission Instructions

- Upload all required files
- Click **Submit** to finalize submission

---

## Notes

- Ensure Kaggle submission evidence is included
- Ensure GitHub repository is accessible
- Ensure notebook runs without errors

## Assignment 2: Conceptual Question 3 and 10

The inclusion of Conceptual Question 3 and Applied Question 10 from An Introduction to Statistical Learning with Applications in Python (James, Witten, Hastie, and Tibshirani, 2023) reflects the structured requirements of this assignment and serves to demonstrate both theoretical understanding and applied competency in regression analysis. These questions were intentionally incorporated into this report to align with the instructional objectives of reinforcing core statistical principles while also validating the practical application of regression techniques in controlled and empirical contexts. By addressing both conceptual interpretation and applied modeling, the analysis presented herein provides a comprehensive evaluation of regression methodology, bridging foundational theory with implementation and interpretation in a manner consistent with graduate-level expectations.

### Conceptual Question #3

Suppose we have a data set with five predictors:

- \( X_1 = \) GPA  
- \( X_2 = \) IQ  
- \( X_3 = \) Level (1 for College and 0 for High School)  
- \( X_4 = \) Interaction between GPA and IQ  
- \( X_5 = \) Interaction between GPA and Level  

The response is starting salary after graduation (in thousands of dollars).

Suppose we use least squares to fit the model, and obtain the following estimates:

- \( \hat{\beta}_0 = 50 \)  
- \( \hat{\beta}_1 = 20 \)  
- \( \hat{\beta}_2 = 0.07 \)  
- \( \hat{\beta}_3 = 35 \)  
- \( \hat{\beta}_4 = 0.01 \)  
- \( \hat{\beta}_5 = -10 \)  

---

#### (a) Interpretation

Which answer is correct, and why?

i. For a fixed value of IQ and GPA, high school graduates earn more, on average, than college graduates.  

ii. For a fixed value of IQ and GPA, college graduates earn more, on average, than high school graduates.  

iii. For a fixed value of IQ and GPA, high school graduates earn more, on average, than college graduates provided that the GPA is high enough.  

iv. For a fixed value of IQ and GPA, college graduates earn more, on average, than high school graduates provided that the GPA is high enough.  

---

#### (b) Prediction

Predict the salary of a college graduate with an IQ of 110 and a GPA of 4.0.

---

#### (c) Interaction Effect

True or false:

> Since the coefficient for the GPA/IQ interaction term is very small, there is very little evidence of an interaction effect.

Justify your answer.

### Part 2: Applied Question #10 (Carseats Dataset)

This question should be answered using the **Carseats** dataset.

**(a)** Fit a multiple regression model to predict `Sales` using `Price`, `Urban`, and `US`.

**(b)** Provide an interpretation of each coefficient in the model. Be careful, some of the variables in the model are qualitative.

**(c)** Write out the model in equation form, being careful to handle the qualitative variables properly.

**(d)** For which of the predictors can you reject the null hypothesis \( H_0: \beta_j = 0 \)?

**(e)** Based on your response to part (d), fit a smaller model that includes only the predictors for which there is evidence of association with the outcome.

**(f)** How well do the models in parts (a) and (e) fit the data?

**(g)** Using the model from part (e), obtain 95% confidence intervals for the coefficient(s).

**(h)** Is there evidence of outliers or high-leverage observations in the model from part (e)?

# References

James, G., Witten, D., Hastie, T., & Tibshirani, R. (2023). *An introduction to statistical learning with applications in Python*. Springer. https://doi.org/10.1007/978-3-031-38747-0