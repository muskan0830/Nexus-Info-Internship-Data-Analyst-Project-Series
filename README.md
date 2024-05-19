# Nexus Info Internship Projects
# PHASE 1:

# PROJECT 1: IRIS

## PYTHON EDA

**Introduction:**
In this, we conducted an Exploratory Data Analysis (EDA) on the famous Iris dataset using Python. The objective was to gain insights into the dataset, perform data cleaning, statistical summaries, and visualize patterns and distributions to understand the characteristics of different iris species.

**Skills Demonstrated:**
- Data cleaning: Checked for null and duplicated values, and trimmed column names.
- Statistical analysis: Calculated summary statistics such as mean, median, and range.
- Data visualization: Created charts and visualizations to explore patterns, distributions, and classifications within the dataset.
- Interpretation: Derived insights from the data analysis to understand the characteristics and differences among iris species.

**Data Cleaning:**
- Checked for null values, duplicated rows, and trimmed column names by removing white spaces to ensure data integrity and consistency.

**Statistical Summary and Basic EDA:**
- Utilized Python libraries such as warning, Pandas, NumPy, MatPlotLib and Seaborn to perform statistical summary and basic EDA on the Iris dataset.
- Calculated descriptive statistics including mean, median, minimum, maximum, and quartiles for each feature (sepal length, sepal width, petal length, and petal width).

**Charts and Visualizations:**
- Created visualizations to explore patterns, distributions, and relationships within the dataset.
- Visualized the distribution of sepal and petal dimensions across different iris species to identify any discernible patterns or trends.

**Insights:**
1. **Sepal and Petal Dimensions by Class:**
   - Identified variations in sepal and petal dimensions across different iris species.
   - Observed that "virginica" generally had longer and wider sepals and petals compared to "versicolor" and "setosa".

2. **Class Discrimination:**
   - Noted that the differences in sepal and petal dimensions among the classes could potentially be used for discriminating between different iris species.
   - Sepal and petal dimensions exhibited distinct patterns that could aid in species classification.

3. **Feature Importance:**
   - Recognized that petal length and width appeared to be more informative features for distinguishing between iris species compared to sepal dimensions.
   - Petal measurements showed more significant differences across classes, suggesting their importance in classification tasks.

**Classification Recommendations:**
Based on the analysis, we proposed the following classification guidelines:
1. **Setosa**: Characterized by smaller petal dimensions with a narrow range of values.
2. **Versicolor**: Exhibits moderate petal dimensions with a wider range compared to Setosa but narrower compared to Virginica.
3. **Virginica**: Features the largest petal dimensions among all classes with the widest range of values.


## POWER BI DASHBOARD

### 1. KPIs:
- Begin by defining key measures to display the maximum and minimum values of petal length, petal width, sepal length, and sepal width along with the corresponding species.
- Utilize DAX code to calculate these measures. For instance, to obtain the maximum petal length and its corresponding species:
    ```DAX
    MaxPetalLength_KPI = 
    VAR MaxPetalLength = MAX('iris-data'[petal-length])
    VAR MaxSpecies = CALCULATE(MAX('iris-data'[Species]), 'iris-data'[petal-length] = MaxPetalLength)
    RETURN
        MaxPetalLength & " (" & MaxSpecies & ")"
    ```
- Repeat the process to create measures for minimum values and for other characteristics.

### 2. Organizing the Display:
- Insert a textbox onto the dashboard and label it as "Petal Length".
- Add cards to display both maximum and minimum petal lengths.
- Group these elements to facilitate management and positioning by selecting the textbox and the two cards, then navigating to the 'Format' option and choosing 'Group'.

### 3. Charts and Navigator:
- Generate bar and column charts to visualize trends for both petal length and petal width, enhancing understanding of their distribution and comparison.
- Integrate a page navigator to enable seamless navigation between different sections of the dashboard, enhancing user experience and facilitating access to various insights and analyses.
- Duplicate the existing page to maintain consistency in design and layout.
- Repeat the steps, adjusting them as necessary, to showcase key measures and visualizations for sepal length and sepal width.

# Project 2: Weather

## PYTHON: EDA, CORRELATION AND PREDICTIVE ANALYSIS

**Introduction:**
In this, we performed data preparation, correlation analysis, and regression analysis on a weather dataset using Python. The objectives were to clean and preprocess the data, identify relationships between weather parameters through correlation analysis, and implement regression analysis to predict one weather parameter based on others.

**Skills Demonstrated:**
- Data cleaning and preprocessing: Handled missing values, outliers, and inconsistencies in the dataset using Pandas and NumPy libraries.
- Statistical analysis: Conducted statistical summary and basic exploratory data analysis to understand the dataset's characteristics.
- Data visualization: Created visualizations using Seaborn and Matplotlib libraries to explore patterns and distributions in the data.
- Correlation analysis: Identified relationships between different weather parameters using correlation coefficients.
- Regression analysis: Implemented linear regression to predict one weather parameter based on others and interpreted the regression coefficients.

**Data Preparation:**
- Cleaned the weather dataset by handling missing values, outliers, and whitespaces in column names.
- Changed the data type of the timestamp column and extracted month and day of the week from the timestamp.
- Conducted statistical summary and created visualizations to understand the dataset's characteristics.

**Correlation Analysis:**
- Identified relationships between different weather parameters through correlation analysis.
- Analyzed the correlation coefficients between wind speeds, heights above ground, roughness length, solar radiation, temperature, air density, and pressure.
- Visualized the correlation matrix using heatmaps to visualize the strength and direction of correlations.

**Regression Analysis:**
- Implemented linear regression to predict wind speed ('v1') based on other weather parameters.
- Evaluated the model's performance using cross-validation scores and interpreted the regression coefficients.
- Derived insights into the predictors' influence on predicted wind speed and discussed limitations and considerations.

**Summary of Results:**
1. **Seasonal Variations:** Identified seasonal trends in wind speeds, solar radiation, and temperature, with higher values observed during summer months.
2. **Height Above Ground and Roughness Length:** Found consistent values for heights above ground and roughness length throughout the year, indicating stable measurement conditions.
3. **Correlation Analysis:** Discovered strong positive correlations between wind speeds at different heights above ground and between solar radiation variables. Moderate correlations were observed between temperature, air density, and latitude.
4. **Regression Analysis:** The regression model demonstrated strong performance with high cross-validation scores. Predictor variables such as wind speed at 10 meters above displacement height ('v2') and air density ('rho') had significant positive coefficients, indicating their influence on predicted wind speed.

**Conclusion:**
Through this project, we gained insights into the relationships between weather parameters and developed a predictive model for wind speed. The analysis provides valuable information for understanding weather patterns and predicting wind speeds based on other environmental factors. Further refinement of the model and consideration of additional variables could enhance its predictive accuracy in future iterations.

## POWER BI DASHBOARD

[View My Weather Power BI dashboard Here!](https://app.powerbi.com/groups/me/reports/9b497d1e-935a-4c07-8dd3-983a190899e1/ReportSectionef39925040db42878834?ctid=e14e73eb-5251-4388-8d67-8f9f2e2d5a46&experience=power-bi)

**1. Data Manipulation and Transformation:**

a. **Changing Data Types:** Adjusted all column data types for consistency.

b. **Extracting Additional Information:**
   - Created new columns for:
     - Month Name (as "month_extracted").
     - Month Number.
     - Day of the Week Name (as "week_day_extracted").
     - Day of the Week Number (as "week_day_number").
   - This step ensures proper ordering even if month and day names are not consistently arranged.

**2. Data Visualization:**

a. **Average Wind Speed Over Months:**
   - Utilized a line chart to visualize average wind speeds.
   - Placed "month_extracted" on the x-axis.
   - Sorted months correctly by selecting "sort by column" and choosing the "month number".

b. **Similar Visualization for Other Parameters:** Employed line charts for other metrics following the same process.

c. **Key Performance Indicators (KPIs):**
   - Configured KPIs by:
     - Adding "cumulated hours" to values.
     - Averaging the values.
     - Setting "month_extracted" as the trend axis.
     - Utilizing the minimum of "cumulated hours" as the target for comparison.

d. **Buttons for Navigation:** Inserted page navigation buttons under the "insert" tab, then "navigator", and finally "page navigator".

e. **Slicers for Filtering:** Incorporated slicers for filtering data by month and week days.

f. **Week Days Dashboard:** Duplicated the current page and replaced "month_extracted" with "week_day_extracted" to create a dashboard focused on weekdays.

g. **Slicer Sync Across Dashboards:** Ensured slicers are synchronized across both dashboards for seamless filtering by navigating to "view" and selecting "sync slicers". Then, selected all pages to apply the synchronization.



# PHASE 2:

# TWITTER SENTIMENT ANALYSIS

