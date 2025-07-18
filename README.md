# Electric Vehicle Population Analysis 📊⚡

This project analyzes electric vehicle (EV) population data by county to identify patterns, handle missing values, and manage outliers in percentage-based EV metrics. It was developed as part of an internship project and focuses on data cleaning and preparation as a foundation for future predictive modeling.

---

## 📁 Dataset

**Source:** `Electric_Vehicle_Population_By_County.csv`

This dataset contains information about electric vehicles registered across different counties, including metrics such as:

- `Date`
- `County`
- `State`
- `Electric Vehicle (EV) Total`
- `Percent Electric Vehicles`

---

## 🔧 Project Workflow

The code performs the following key steps:

1. **Data Import and Inspection**
   - Loads the dataset and checks structure, data types, and missing values.

2. **Outlier Detection and Handling**
   - Uses Interquartile Range (IQR) method to detect and cap outliers in the `Percent Electric Vehicles` column.
   - Ensures that extreme values do not skew analysis.

3. **Missing Value Treatment**
   - Converts the `Date` column to a valid datetime format and removes rows with invalid or missing dates.
   - Removes rows with missing `Electric Vehicle (EV) Total` values.
   - Fills missing categorical data (`County` and `State`) with `"Unknown"`.

4. **Post-Cleaning Validation**
   - Re-checks for missing data and confirms that outliers have been capped successfully.

---

## 💼 Use Case

This cleaned and preprocessed dataset can be used for:

- Time series analysis of EV adoption trends.
- Building predictive models to estimate future EV population growth.
- Geospatial visualizations to identify high EV-density regions.

---

