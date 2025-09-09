# Deforestation Issue Analysis Using Support Vector Machine (SVM)

## Overview
This project analyzes deforestation patterns using a Support Vector Machine (SVM) regression model on a dataset spanning multiple countries and decades. The analysis aims to identify key drivers of deforestation and provide actionable insights for policymakers to mitigate forest loss.

## Dataset
The dataset contains records from countries including Indonesia, Brazil, Russia, Australia, and India covering roughly the mid-20th century to early 21st century. Key features include environmental, demographic, economic, governance, and conservation-related variables.

### Key Variables
- **Demographic:** Population
- **Economic:** GDP (Billion USD), Agriculture Land Percent
- **Environmental:** Rainfall (mm), CO2 Emission (Mt)
- **Governance/Policy:** Deforestation Policy Strictness, Corruption Index, International Aid (Million USD)
- **Logging Activity:** Illegal Lumbering Incidents
- **Conservation:** Protected Areas Percent
- **Outcome Variable:** Forest Loss Area (km²)

## Project Phases

### Phase 1: Data Preprocessing
- **Loading Data:** Imported dataset (`deforestation_dataset.csv`) containing 100 records.
- **Data Cleaning:** Handled missing values by filling numeric columns with medians and categorical columns with modes. Applied one-hot encoding for categorical variables like 'Country'.
- **Feature Scaling:** Standardized numerical features using `StandardScaler`.
- **Train-Test Split:** Divided the data into training (80%) and testing (20%) sets for unbiased model evaluation.

### Phase 2: Model Building and Evaluation
- **Model Training:** Trained an SVM regression model with a linear kernel to predict forest loss area.
- **Model Evaluation:** Used metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² score to assess performance.
- **Hyperparameter Tuning:** Performed grid search over `kernel`, `C`, `gamma`, and `degree` to improve model predictions using 5-fold cross-validation.

### Phase 3: Feature Analysis and Interpretation
- **Feature Importance:** Extracted feature coefficients from the linear SVM to interpret their influence on deforestation.
- **Key Findings:** 
  - Positive impact on deforestation: Population growth, GDP, Illegal Lumbering Incidents, and Corruption Index.
  - Negative impact: Rainfall, CO2 Emissions, Policy Strictness, International Aid, and Protected Areas Percent.
  - Anomalies such as a negative coefficient for illegal lumbering incidents indicate complexities requiring further analysis.

### Phase 4: Reporting and Recommendations
- **Visualization:** Created various plots such as scatter plots, bar charts, correlation heatmaps, histograms, and violin plots to understand relationships and model results.
- **Comprehensive Report:** Prepared a detailed report explaining data processing, model building, feature interpretation, and policy implications.
- **Recommendations:** Proposed multi-faceted actions including strengthening environmental policies, enhancing enforcement, promoting sustainable development, engaging communities, expanding protected areas, leveraging international cooperation, and improving monitoring and adaptive management.

## Installation and Usage
1. Install required Python libraries:
2. Prepare the dataset file `deforestation_dataset.csv` in the working directory.
3. Run the Jupyter notebook or Python scripts for:
- Data preprocessing
- Model training and evaluation
- Hyperparameter tuning
- Feature interpretation
- Visualization

## Summary of Key Insights
| Feature                      | Impact Direction | Interpretation                                                                                   |
|------------------------------|------------------|-------------------------------------------------------------------------------------------------|
| Population                   | Positive         | Higher population drives increased deforestation due to land and resource demands.              |
| GDP (Billion USD)            | Positive         | Economic growth correlates with increased deforestation.                                        |
| Illegal Lumbering Incidents  | Unexpected Negative | Indicates potential data or enforcement complexity; requires further study.                      |
| Rainfall (mm)                | Negative         | More rainfall supports forest health, reducing loss.                                           |
| CO2 Emission (Mt)            | Negative         | Higher emissions correlate with less deforestation, possibly due to industrial land use.        |
| Deforestation Policy Strictness | Negative      | Stricter policies reduce forest loss, emphasizing enforcement importance.                       |
| International Aid (Million USD) | Negative      | Aid supports conservation efforts.                                                             |
| Protected Areas Percent      | Negative         | Greater protected areas help curb deforestation.                                               |
| Corruption Index             | Positive         | Higher corruption slightly increases deforestation through weakened enforcement.               |

## Recommendations for Mitigation
- **Policy and Governance:** Enforce robust legal frameworks, enhance transparency, and strengthen monitoring using satellite and local patrols.
- **Sustainable Economic Development:** Incentivize sustainable land use, support indigenous stewardship, and diversify local economies.
- **Community Engagement:** Strengthen education, participatory management, and local capacity building.
- **Environmental Protection:** Expand protected areas, restore degraded land, and conserve water and soil resources.
- **International Cooperation:** Utilize climate finance, coordinate across borders, and adopt sustainable supply chain policies.
- **Research & Adaptive Management:** Improve data, share analytics publicly, and use machine learning to continually adapt policies.

---

This README summarizes the analytical approach, results, and actionable recommendations derived from applying SVM regression to deforestation data, supporting informed decisions to address forest loss effectively.

