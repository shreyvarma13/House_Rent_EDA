# House_Rent_EDA

Exploratory Data Analysis of the House Rent Dataset using Python.

## Dataset

The dataset contains **4,746 entries** with the following columns:
- Posted On
- BHK
- Rent
- Size
- Floor
- Area Type
- Area Locality
- City
- Furnishing Status
- Tenant Preferred
- Bathroom
- Point of Contact

## Libraries Used

- **numpy** (1.26.4)
- **pandas** (2.2.2)
- **matplotlib** (3.8.4)
- **seaborn** (0.13.2)
- **plotly** (via plotly.express)

## Data Preprocessing

1. **Data Type Conversion**: Converted 'Posted On' column from object to datetime format
2. **Feature Extraction**: Extracted numerical values from 'Floor' column:
   - Created 'Floor Number' column (handles ground floor, upper/lower basement, and numeric floors)
   - Created 'Total Floors' column
3. **Column Removal**: Dropped irrelevant columns ('Floor', 'Point of Contact')
4. **Feature Engineering**: Created 'Rent_per_sqft_in(K)' feature - rent per square foot in thousands
5. **Missing Values**: Verified no missing values in the dataset

## Visualizations

### 1. Average Rent Across Cities
Bar plot showing average rent prices by city using seaborn. Identifies Mumbai as the most expensive city for renting apartments.

### 2. Average Rent by BHK across Cities
Interactive bar chart using Plotly showing average rent grouped by number of BHKs (bedrooms) across different cities.

### 3. Share of Total Rent by City
Pie chart using Plotly displaying the contribution of each city to the total rental market. Shows Mumbai contributes the majority share.

### 4. Rent Distribution by Furnishing Status, BHK, and City
Faceted visualizations comparing rents across:
- Furnishing Status (Unfurnished, Semi-Furnished, Furnished)
- Number of BHKs
- Cities

Created using both seaborn catplot and Plotly bar charts for interactive exploration.

## Key Insights

- Mumbai is the most expensive city for renting apartments
- Mumbai contributes the majority share to India's rental market
- Mumbai tops the chart for all 3 categories 
- The Top Grossing category is Semi-Furnished which is most popular in Mumbai city followed by Bangalore and Delhi

## Files

- `House Rent Dataset EDA.ipynb` - Jupyter notebook containing the analysis
- `House_Rent_Dataset.csv` - Dataset file

