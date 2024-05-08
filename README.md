# Nexus Info Internship Projects
# PHASE 1:

# PROJECT 1: IRIS

## PYTHON EDA

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

## Project 2: Weather

### PYTHON EDA, CORRELATION AND PREDICTIVE ANALYSIS

### POWER BI DASHBOARD

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
