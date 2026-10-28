# British Airways Data Science Job Simulation

A data science project completed as part of the British Airways Job Simulation on [Forage](https://www.theforage.com/). This project explores flight schedule analysis, lounge eligibility, and customer booking behaviour using Python, data analysis, and machine learning.

## Table of Contents

- [Project Overview](#project-overview)
- [Business Objectives](#business-objectives)
- [Task 1: Flight Schedule and Lounge Eligibility Analysis](#task-1-flight-schedule-and-lounge-eligibility-analysis)
- [Task 2: Predicting Customer Booking Behaviour](#task-2-predicting-customer-booking-behaviour)
- [Datasets](#datasets)
- [Technologies Used](#technologies-used)
- [Repository Structure](#repository-structure)
- [Installation and Setup](#installation-and-setup)
- [How to Run](#how-to-run)
- [Key Learnings](#key-learnings)
- [Future Improvements](#future-improvements)
- [Acknowledgements](#acknowledgements)

## Project Overview

The British Airways Data Science Job Simulation focuses on applying data science techniques to business problems in the airline industry.

This repository covers two analytical tasks:

1. **Flight Schedule and Lounge Eligibility Analysis:** Exploring flight schedules, categorising flights, and analysing passenger eligibility across different tiers.
2. **Predicting Customer Booking Behaviour:** Analysing customer booking data and developing a machine learning workflow to predict whether a booking is completed.

The project demonstrates practical skills in data preparation, exploratory data analysis, feature engineering, data visualisation, and predictive modelling.

## Business Objectives

The main objectives of this project are to:

- Analyse flight schedules and identify meaningful flight categories.
- Examine passenger eligibility across different tiers.
- Explore customer booking patterns and purchasing behaviour.
- Identify features that may help explain booking completion.
- Apply data preprocessing and machine learning techniques to a classification problem.
- Translate analytical findings into insights that can support business decisions.

## Task 1: Flight Schedule and Lounge Eligibility Analysis

**Notebook:** `British_Airways_Task1.ipynb`

### Objective

Analyse flight schedule data and passenger eligibility information to organise flights into meaningful categories and support lounge-planning analysis.

### Analytical Approach

- Load and inspect the flight schedule dataset.
- Examine column names, data types, and data quality.
- Explore flight characteristics, including flight dates, times, routes, and flight duration categories.
- Categorise flights according to relevant operational conditions.
- Identify long-haul morning flights where applicable.
- Analyse passenger eligibility across Tier 1, Tier 2, and Tier 3 categories.
- Organise the results into an analytical table for comparison.

### Business Relevance

Understanding flight schedules and passenger eligibility can help structure information for lounge capacity planning and operational decision-making.

The conclusions should be based on the calculations and assumptions documented in the notebook.

## Task 2: Predicting Customer Booking Behaviour

**Notebook:** `British_Airways_Task2.ipynb`

### Objective

Explore customer booking data and develop a classification workflow to predict whether a customer booking is completed.

### Target Variable

The target variable is `booking_complete`.

- `0` — Booking not completed.
- `1` — Booking completed.

### Analytical Workflow

#### 1. Data Loading and Inspection

- Load the customer booking dataset using pandas.
- Examine the dataset structure, dimensions, and data types.
- Inspect missing values and duplicate records.
- Review the distribution of the target variable.

#### 2. Exploratory Data Analysis

Explore booking behaviour using variables such as:

- Number of passengers.
- Sales channel.
- Trip type.
- Purchase lead time.
- Length of stay.
- Flight hour and flight day.
- Route and booking origin.
- Extra baggage preferences.
- Preferred seating preferences.
- In-flight meal preferences.
- Flight duration.

<img width="1008" height="763" alt="image" src="https://github.com/user-attachments/assets/6f3bbad6-1246-4c12-aaf8-6897b959d3cc" />



The purpose is to understand the data and identify potentially useful patterns before modelling.

#### 3. Data Preprocessing

Prepare the dataset for machine learning by:

- Separating input features from the target variable.
- Reviewing missing values and data types.
- Encoding categorical features where required.
- Preparing numerical and categorical features for modelling.

Categorical variables such as `sales_channel`, `trip_type`, `flight_day`, `route`, and `booking_origin` may require encoding before being used by a classification algorithm.

#### 4. Feature Selection

Explore which features provide useful information about booking completion.

Techniques such as mutual information can help rank features according to their statistical relationship with the classification target.

Feature selection should be performed using training data only to avoid information leakage from the test set.

#### 5. Model Development

- Split the dataset into training and testing sets.
- Use stratified splitting where appropriate to preserve the target class distribution.
- Apply suitable preprocessing to numerical and categorical features.
- Train a classification model to predict booking completion.
- Compare the model against a simple baseline where appropriate.

#### 6. Model Evaluation

Evaluate the model using suitable classification metrics, including:

- Precision.
- Recall.
- F1-score.
- Confusion matrix.
- ROC-AUC.
- Precision-recall analysis.

Since completed bookings may represent a minority of the observations, accuracy alone may not adequately describe model performance.

The final evaluation should consider how effectively the model identifies completed bookings and the trade-offs between false positives and false negatives.

### Business Relevance

Predicting booking completion can help identify customer and booking characteristics associated with conversion. These findings may support further analysis of customer journeys, booking channels, and opportunities to improve conversion.

Model predictions should be validated before being used to guide real business decisions.

<img width="1646" height="911" alt="image" src="https://github.com/user-attachments/assets/c6067c26-cc07-4ad0-9d64-3f3044a9d96b" />


## Datasets

This repository contains two datasets.

### 1. `flight_schedule.xlsx`

An Excel dataset used for Task 1.

It contains flight schedule and passenger eligibility information used to analyse flight characteristics and tier-based eligibility.

Relevant fields in the analysis include flight dates and times, airline and flight identifiers, route information, flight characteristics, seat information, and passenger eligibility categories.

### 2. `customer_booking.csv`

A CSV dataset used for Task 2.

The dataset contains customer booking information, travel characteristics, booking preferences, and the booking completion outcome.

| Feature | Description |
|---|---|
| `num_passengers` | Number of passengers associated with the booking |
| `sales_channel` | Channel through which the booking was made |
| `trip_type` | Type of trip |
| `purchase_lead` | Time between booking and the scheduled flight |
| `length_of_stay` | Length of the customer's stay |
| `flight_hour` | Scheduled flight hour |
| `flight_day` | Day of the week of the flight |
| `route` | Flight route |
| `booking_origin` | Country associated with the booking origin |
| `wants_extra_baggage` | Indicates whether extra baggage was requested |
| `wants_preferred_seat` | Indicates whether a preferred seat was requested |
| `wants_in_flight_meals` | Indicates whether in-flight meals were requested |
| `flight_duration` | Flight duration |
| `booking_complete` | Target variable indicating booking completion |

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Jupyter Notebook | Interactive analysis and experimentation |
| pandas | Data manipulation and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualisation |
| Seaborn | Statistical data visualisation |
| scikit-learn | Data preprocessing, feature selection, classification, and evaluation |
| openpyxl | Reading Excel files |

## Repository Structure

```text
British-Airways-Job-Simulation/
│
├── British_Airways_Task1.ipynb
├── British_Airways_Task2.ipynb
├── customer_booking.csv
├── flight_schedule.xlsx
└── README.md
```

## Installation and Setup

### Prerequisites

- Python 3.10 or another compatible Python version.
- Jupyter Notebook or JupyterLab.
- Git.

### Step 1: Clone the Repository

```bash
git clone https://github.com/Pranavbhawane7/British-Airways-Job-Simulation.git
```

### Step 2: Navigate to the Project Directory

```bash
cd British-Airways-Job-Simulation
```

### Step 3: Create a Virtual Environment

```bash
python -m venv .venv
```

Activate the environment on Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### Step 4: Install Dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

If the notebooks require additional packages, install them as needed.

## How to Run

Start Jupyter Notebook from the project directory:

```bash
jupyter notebook
```

Open and execute the notebooks:

1. `British_Airways_Task1.ipynb` — Flight schedule and lounge eligibility analysis.
2. `British_Airways_Task2.ipynb` — Customer booking behaviour analysis and predictive modelling.

Run the notebook cells sequentially to ensure that variables, data transformations, and intermediate results are created in the correct order.

Keep both datasets in the project directory unless the notebook file paths have been configured differently.

## Key Learnings

This project provides practical experience with:

- Loading and inspecting structured datasets.
- Cleaning and transforming data using pandas.
- Applying conditional logic and creating analytical categories.
- Performing exploratory data analysis.
- Working with numerical and categorical variables.
- Understanding categorical encoding techniques.
- Exploring feature selection using mutual information.
- Preparing data for classification models.
- Evaluating classification performance using multiple metrics.
- Connecting data analysis to operational and customer-related business problems.

## Future Improvements

Potential extensions include:

- Adding visual summaries of flight categories and passenger eligibility.
- Comparing different approaches to encoding high-cardinality categorical features.
- Establishing a baseline classifier and comparing alternative models.
- Applying cross-validation and hyperparameter tuning.
- Analysing feature importance and model interpretability.
- Investigating duplicate records and potential data leakage.
- Documenting verified model metrics and actionable business recommendations.
- Improving the reproducibility of the analysis with a documented dependency file.

## Acknowledgements

This project was completed as part of the **British Airways Job Simulation** offered through [Forage](https://www.theforage.com/).

The project is intended for educational purposes and demonstrates the application of data science techniques to airline-related business problems.

## Repository

[British Airways Data Science Job Simulation — GitHub](https://github.com/Pranavbhawane7/British-Airways-Job-Simulation)
