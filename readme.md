
# Predicting Customer Book Purchases

## Project Description

This project aims to predict whether customers will purchase books in June, based on their purchasing behavior from April and May. The data includes information about book purchases, customer demographics, and purchase locations.

## Dataset

1. **Book Sales Data**:
    - Monthly sales data for April, May, and June.
    - Contains details about each book purchase, including the customer ID, book price, and purchase date.

2. **Customer Data**:
    - Information about customers such as demographic data and family status.

## Data Preparation

### Steps

1. **Data Integration**:
    - Combined April, May, and June sales into a single DataFrame.
    - Joined sales data with customer data using `Customer ID` as the key.

2. **Customer-Level Aggregation**:
    - Reformatted the data to have one row per customer, summarizing their purchasing activity across April and May.
    - Calculated key metrics:
        - **Total Spend**: Total amount spent by the customer in April and May.
        - **June Purchases**: Number of books purchased in June.

3. **Feature Engineering**:
    - Encoded text-based fields like `Audience` (e.g., Adult, Children, Teen) into numeric dummy variables.
    - Created new features to enhance prediction capabilities:
        - Count of books purchased for each `Audience` type (Adult, Children, Teen).
        - Indicator for whether the customer has school-aged children.
        - Purchase location breakdown (percent of purchases made in person).

4. **Final Dataset**:
    - A modeling-ready DataFrame with the following columns:
        - `June Purchases`: Target variable (to predict).
        - `Total Spend`, `Adults`, `Children`, `Teens`: Predictor variables.
        - `Has Kids`: Binary feature indicating whether a customer has children.
        - `Percent in Person`: Percentage of purchases made in person.

## Usage

The final dataset is ready to be used for machine learning models to predict `June Purchases`. The feature set is clean, numeric, and optimized for input into predictive models.

### Key Concepts

- **Feature Engineering**: Transforming raw data into meaningful features that enhance model performance.
- **Data Aggregation**: Summarizing transaction-level data into customer-level insights.
- **Dummy Variables**: Converting categorical fields into numeric representations.
- **Predictive Modeling**: Using historical data to predict future behavior.

## File Structure

- **Data Files**: Raw input files (not included due to privacy considerations).
- **Final Dataset**: The cleaned and processed data for modeling.
- **Code Files**: Python scripts for data processing and feature engineering.

## Tools and Libraries

- **Pandas**: Data manipulation and aggregation.
- **NumPy**: Numeric calculations.
- **Seaborn**: Data visualization.
- **Jupyter Notebook**: Interactive environment for data analysis.

---

### Author

This project was developed as part of a data analytics initiative to improve customer targeting strategies.
