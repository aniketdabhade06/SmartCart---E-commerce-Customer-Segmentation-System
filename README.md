# SmartCart---E-commerce-Customer-Segmentation-System
## Overview
This project focuses on analyzing and clustering the customer base for "SmartCart" using their purchasing behavior, demographics, and tenure. The primary goal is to segment the customers to better understand distinct consumer groups, enabling data-driven marketing strategies and personalized experiences.

## Dataset
The dataset used for this analysis is smartcart_customers.csv. It contains detailed information on customer demographics, spending habits across various product categories, and platform engagement (e.g., website visits, purchases).

## Dependencies
he project requires the following Python libraries:

pandas (for data manipulation and analysis)
matplotlib (for data visualization)
seaborn (for statistical data visualization)

## Methodology
1. Data Preprocessing
To ensure the dataset is ready for machine learning algorithms, the following data cleaning steps were performed:

Handling Missing Values: Missing values in the Income column were imputed using the median income of the dataset.
2. Feature Engineering
Several new features were created to extract better insights and simplify the modeling process:

Age: Calculated based on the Year_Birth (Reference year: 2026).
Customer Tenure (Customer_Tenure_Days): Calculated as the number of days since the customer joined, using the most recent joining date in the dataset as the reference point.
Total Spending (Total_Spending): Aggregated total amount spent across all product categories (Wines, Fruits, Meat, Fish, Sweets, and Gold).
Total Children (Total_Children): The sum of Kidhome and Teenhome.
Education Simplification: Grouped the Education column into three broader categories:
Undergraduate (Basic, 2n Cycle)
Graduate (Graduation)
Postgraduate (Master, PhD)
Living Arrangement (Living_With): Binned Marital_Status into two categories:
Partner (Married, Together)
Alone (Single, Divorced, Widow, Absurd, YOLO)
3. Data Cleaning
Redundant and obsolete columns that were already aggregated into new features were dropped from the dataset to reduce dimensionality. Dropped columns include:

ID, Year_Birth, Marital_Status, Kidhome, Teenhome, Dt_Customer
Individual spending columns (MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds)
4. Outlier Detection & Clustering
Visualizations: seaborn.PairGrid and other visualization techniques were used to detect outliers in the cleaned dataset.
Customer Segmentation: The cleaned data was grouped into distinct Clusters based on customer traits (Income, Spending, Living Arrangements, etc.) to identify actionable customer profiles."


## How to Use
1.Clone the repository and ensure the smartcart_customers.csv file is in the same directory as the notebook.
2.Install the required dependencies: pip install pandas matplotlib seaborn
3.Run the smartcart.ipynb notebook cell-by-cell to reproduce the data preprocessing, feature engineering, and cluster summaries.

## License
This project is open-source and available under the MIT License.
