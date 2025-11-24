# FIN 550: Big Data Analytics – Final Project

## What Is It Worth? Property Assessment Challenge for Cook County, Illinois

**Authors:** Riley League  
**Updated:** Fall 2025  
**Prepared for:** FIN 550 Big Data Analytics  

> This document and associated data files are authorized for learning use only by students
> enrolled in FIN 550 Big Data Analytics, Fall 2024/2025. Copying or posting externally is
> an infringement of copyright.

---

## 1. Case Background

Property taxes account for a large portion of revenue for local governments, funding police,
schools, pension liabilities, and many other services provided to citizens. In the United States,
property taxes are collected at the county level. Owners pay a sum based on tax rates and levies
for their locale, multiplied by the estimated (assessed) value of their property.

It is the role of a government entity, commonly known as the **Assessor**, to determine the fair
market value of each property.

For this project, we use the example of the **Cook County Assessor’s Office (CCAO)**, which is
responsible for the second most populous county in the United States, home to the City of Chicago
and over 130 other municipalities.

- In FY 2019, CCAO was in charge of valuing **over 1.8 million properties**,  
  generating **$15.58 billion in taxes**.

Determining fair market value for this diverse set of parcels spread across 130+ municipalities is
one of the most complex valuation tasks in the United States.

Historically:

- Prior to 2018, CCAO’s valuation process was **obscure and inaccurate**.  
- Combined with unusually high tax rates and a flawed modeling process, the office faced intense
  public and political pressure.  
- This led to the surprising but decisive 2018 election of **Fritz Kaegi**, who campaigned on
  reforming and making the CCAO more transparent.

Reforms since 2018 include:

- Investments in **technology**  
- Increased **transparency of data**  
- Formation and expansion of the **data science team**  
- Migration of modeling from older SPSS-based processes to a more capable implementation in **R**  
- Public documentation of **modeling and data decisions**

For additional background and context on the data science efforts at CCAO, students are directed to:

- CCAO data documentation on GitLab  
- A video presentation by CCAO data scientist **Dan Snow** on their valuation methods, models, and results (YouTube)

---

## 2. Case Description

You have been recruited to join the **CCAO data science team**.

Your first assignment is to **assess residential property value** – i.e., to predict the market
price of a home if it were to sell – given a set of features.

You are provided with three data files (in `data.zip`):

1. `predict_property_data.csv`  
   - Contains data on **10,000 properties** whose values you are to assess.  
   - Each row is a property.  
   - `pid` is a unique identifier for each property.

2. `historic_property_data.csv`  
   - Contains data on **50,000 other properties** that have **recently sold**.  
   - Includes their sales price (`sale_price`).  
   - Each row is a property.

3. `codebook.csv`  
   - Describes the variables included in each property file.

### Objective

Your objective is to **predict the value of each home** in `predict_property_data.csv` as closely
as possible to its actual value.

You will produce and submit a data file that contains:

- `pid` (property ID)  
- Your assessed value for each property

The quality of your work will be evaluated by comparing your predictions to the actual sales prices
when these homes sell and computing the **Mean Squared Error (MSE)** of your predictions.

> **Your goal:** minimize the MSE of your predictions.

### Approach

You may use data in `historic_property_data.csv` to build models relating property characteristics
to value (as reflected in sale prices).

All analysis – including training and selecting models and making predictions – **must be performed
in R**, and the code should be placed into a **single script**.

You will submit this script as supporting documentation to your written report.

### Tips

- You are encouraged to use **any modeling methods covered in the class**.  
- You may use additional methods not covered in class, but:  
  - This is not expected.  
  - The instructional team may not be able to help with technical issues for these methods.  
- Grading emphasizes how well you **explain and justify** your approach, not how exotic your
  algorithms are. Methods from class are **sufficient** for full credit.

Additional guidance:

- Start with **simple models** using a few predictors.  
- Adding many predictors can improve predictions, but may introduce technical challenges
  (especially with many-level categorical variables).  
- Avoid starting with “kitchen sink” models that include all predictors.  
- Use the **codebook** to understand variables before including them in models.  
- Take care when handling **missing values** and other data-quality issues.

---

## 3. Case Deliverables

You must submit **three files** as your final project:

### 3.1 Executive Summary (PDF)

Using the Word template posted to Canvas (the Executive Summary template), produce an **Executive Summary** in **PDF** format.

Requirements:

- Include a **team name** that can be reported publicly in class (preserving anonymity).  
- The document should have three sections:
  1. **Case Overview & Objectives**  
  2. **Methodology**  
  3. **Conclusion & Recommendations** (including an estimate of model accuracy)

Formatting constraints:

- No more than **3 double-spaced pages**, **12-point font**.  
- Tables and figures should be placed at the **end** in an appendix.  
- The appendix **does not** count toward the page limit.

### 3.2 R Script

Turn in the **R script** used to perform your analysis.

Requirements:

- The script should be runnable **as-is** if the data files are in the same folder.  
- It should regenerate **all results** documented in your Executive Summary.  
- Set a **random seed** where appropriate to ensure replicability.  
- Include code to load necessary packages.  
- Turn in a `.R` or `.Rmd` file (not `.html`).  
- Annotate code with **brief comments** and follow good R style practices.  
- At the top of the script, include a comment with how long a **full run** takes.  
- The script should **not exceed one hour** of runtime.

### 3.3 Assessment File (`assessed_value.csv`)

Export your property assessment values to a CSV named:

```text
assessed_value.csv
```

This file should contain **one row per property** in `predict_property_data.csv` and only two columns:

1. `pid` – property ID, identical to the `pid` column in `predict_property_data.csv`  
   - These should be consecutive integers from 1 to 10,000.

2. `assessed_value` – your **predicted property value**  
   - Numeric format only (e.g., `100000`, **not** `$100,000`).  
   - All values must be **non-missing** and **non-negative**.

Example (values illustrative only):

```text
pid,assessed_value
1,156787.00
2,2879298.00
3,365198.00
...
```

The instructor will compile all teams’ files and report to the class the **predictions vs. actual values**
and the **MSE** for each team.

---

## 4. Case Grading

Your grade has three components:

### 4.1 Executive Summary – 60 points

Assessed on:

- Clarity of objectives, methodologies, and results  
- Avoidance of unnecessary jargon  
- Grammar, sentence structure, and professional tone

### 4.2 R Script – 60 points

Assessed on:

1. **Readability** – Are comments and variable names clear and informative?  
2. **Replicability** – Can the script be run without modification to reproduce your results?  
3. **Efficiency** – Does the code run in a reasonable amount of time (≤ 1 hour)?

### 4.3 Assessment File – 30 points

Assessed on:

- **Valid formatting** of `assessed_value.csv`  
- **Completeness** (10,000 records with non-missing, non-negative values)  
- **Predictive performance** measured by MSE

Notes:

- If your file is properly formatted and complete, the **minimum** score on this component is
  **20 points**, even if your MSE is relatively high.

---

_End of FIN 550 Final Project Instructions._
