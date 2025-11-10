# Obesity in West Virginia: Socioeconomic Factors and Geographic Disparities

## Overview

Comprehensive analysis of adult obesity in West Virginia examining the relationships between socioeconomic factors (income, education, healthcare access), geographic location (rural vs. urban), and obesity outcomes. Using 2023 BRFSS data, this study identifies key predictors of obesity risk and provides evidence-based recommendations for targeted public health interventions.

## Problem Statement

West Virginia consistently ranks among states with highest adult obesity rates. This analysis addresses: **How do income, education, and healthcare access influence adult obesity in rural versus urban West Virginia?**

## Dataset

- **Source:** 2023 Behavioral Risk Factor Surveillance System (BRFSS) - CDC
- **Focus:** West Virginia residents
- **Sample Size:** 1,490 adults (ages 45-64)
- **Geographic Distribution:** 353 rural (23.7%), 1,137 urban (76.3%)
- **Survey Method:** Landline and cellular telephone interviews with survey weights applied

**Key Variables:**
- Obesity status (BMI ≥ 30)
- Income group (Low, Mid, High)
- Education level (4-level scale)
- Healthcare access (insured/uninsured)
- Physical activity (meets guidelines or inactive)
- Geographic location (rural/urban)

## Methodology

### Analysis Approach
1. **Descriptive Analysis:** Weighted prevalence calculations and cross-tabulations
2. **Bivariate Analysis:** Chi-square tests for categorical associations
3. **Stratified Analysis:** Effect modification by geographic location
4. **Visualization:** Heat maps, bar charts, and correlation matrices

### Data Preparation
- Filtered to West Virginia residents only
- Age-restricted to adults 45-64 years
- Handled missing values (<5% of records)
- Applied BRFSS survey weights for population representativeness

**Key Finding:** Rural mid-income residents show highest obesity rates (88.1%), contradicting traditional socioeconomic protective effects.

### Physical Activity Impact
- **Rural Active Benefit:** 13.6 percentage point reduction
- **Urban Active Benefit:** 9.2 percentage point reduction
- **Finding:** Physical activity is strongest predictor of obesity outcomes across all groups

### Healthcare Access
- Overall coverage rate: 96.5%
- Limited variation by income/location
- Physical activity outperforms healthcare access as obesity predictor

### Education Relationship
- Level 1 (Lowest): 71.2% obesity
- Level 3 (Some College): Highest rates
- Level 4 (College Grad): 77.8% obesity
- **Finding:** Non-linear relationship suggesting multiple pathways

## Technologies

- **Language:** Python
- **Data Analysis:** Pandas, NumPy, Scikit-learn
- **Statistical Tests:** Chi-square, correlation analysis
- **Visualization:** Matplotlib, Seaborn
- **Data Source:** CDC BRFSS API

## Getting Started

### Prerequisites
- Python 3.8+
- CDC BRFSS data access

## Key Insights

**Rural-Urban Gap is Minimal** - 2.1 percentage point difference challenges conventional assumptions
**Physical Activity is Primary Driver** - Strongest predictor despite high healthcare coverage (96.5%)
**Rural Mid-Income Paradox** - Highest obesity rates (88.1%) suggest location-specific economic mechanisms
**Rural Environmental Advantage** - Active rural residents outperform urban counterparts (13.6 pp benefit vs. 9.2 pp)
**Education Shows Complex Pathway** - Both lowest and highest education levels show better outcomes

## Recommendations

**Immediate:**
- Launch statewide physical activity initiative
- Target rural mid-income populations with specialized interventions
- Invest in activity-promoting infrastructure

**Medium-Term:**
- Establish location-specific community activity programs
- Implement workplace interventions for sedentary occupations
- Integrate physical activity across all education levels

**Long-Term:**
- Establish longitudinal tracking systems
- Align transportation and economic development policies with health goals
- Share successful rural models across similar communities

## Study Limitations

- Cross-sectional design limits causal inference
- Self-reported BMI may introduce measurement bias
- Binary rural/urban classification may obscure sub-regional variations
- Single time-point analysis cannot capture seasonal variations

**Contact:** Extern/Trubridge (Summer 2025)

## References

- Centers for Disease Control and Prevention. (2023). Behavioral Risk Factor Surveillance System Annual Survey Data. Retrieved from https://www.cdc.gov/brfss/annual_data/annual_2023.html
