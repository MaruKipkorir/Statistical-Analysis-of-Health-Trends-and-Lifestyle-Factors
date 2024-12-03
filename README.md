# Statistical Analysis of Health Trends and Lifestyle Factors  

## Project Overview  
This project investigates the relationships between health indicators and various socio-demographic factors using a public health dataset. The analysis explores the following three key questions:  

1. **Health Status by State**  
   - Examines differences in physical health status (number of days with poor physical health in the last 30 days) across three states: New York, New Jersey, and Connecticut.  

2. **Health Status and Home Ownership**  
   - Analyzes the relationship between physical health status and homeownership, comparing individuals who own their homes versus those who rent.  

3. **Chronic Sickness and Nicotine Use**  
   - Investigates the association between nicotine use and chronic illness, defined as having 15 or more days of poor physical health in the last 30 days.  

## Dataset  
The dataset includes various health-related variables, such as physical health, smoking behavior, and housing status. It also contains state-level information for New York, New Jersey, and Connecticut.  
It contains the following files: 
- **`case_study.csv`**: The primary dataset used for analysis.  
- **`data_dictionary.pdf`**: A document that explains the meaning of the dataset’s features and their coded values.  

Both files are located in the `data/` directory of this repository.  

## Methodology  

### 1. Health Status by State  
- **Data Cleaning**:  
   - Replaced invalid values (`88` as "None") with `0`.  
   - Removed rows with invalid responses (`77` and `99`).  
- **Analysis**:  
   - Visualized the distribution of physical health status (`PHYSHLTH`) by state.  
   - Used the Kolmogorov-Smirnov test and Q-Q plots to assess normality.  
   - Performed Levene's test for variance equality.  
   - Conducted a Kruskal-Wallis test to determine differences in health status across states.  
   - Performed post-hoc pairwise comparisons to identify specific state differences.  

### 2. Health Status and Home Ownership  
- **Data Cleaning**:  
   - Filtered data to include only homeownership statuses (`Own` and `Rent`).  
   - Mapped numeric codes to descriptive labels.  
- **Analysis**:  
   - Visualized health status by homeownership type.  
   - Assessed normality using Kolmogorov-Smirnov tests and variance equality using Levene's test.  
   - Conducted a Mann-Whitney U test to compare physical health between homeowners and renters.  

### 3. Chronic Sickness and Nicotine Use  
- **Data Cleaning**:  
   - Created a binary `NICOTINE_USE` variable based on smoking and nicotine product usage indicators.  
   - Defined chronic sickness as having 15 or more days of poor physical health, creating a binary `CHRONIC` variable.  
- **Analysis**:  
   - Generated a contingency table to summarize the relationship between nicotine use and chronic sickness.  
   - Visualized the prevalence of chronic sickness by nicotine use status.  
   - Used a Chi-Square test of independence to determine statistical significance.  

## Results  

### 1. Health Status by State  
- Significant differences in physical health were observed across states.  
- Post-hoc analysis revealed pairwise differences between all states.  

### 2. Health Status and Home Ownership  
- Renters reported significantly worse physical health compared to homeowners.  

### 3. Chronic Sickness and Nicotine Use  
- A significant association was found between nicotine use and chronic illness.  
