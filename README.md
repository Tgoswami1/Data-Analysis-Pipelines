# Data-Analysis-Pipelines
This project analyzes user and order data to derive meaningful insights, such as the average orders by meal type, the most popular dishes, and other data relationships. The project involves data cleaning, merging, visualization, and exporting a processed dataset.

The following steps are included in the pipeline:

Data Loading
Data Cleaning
Data Merging
Data Analysis
Visualization
Exporting Results

# Project Structure

├── Assignment.xlsx                # Input Excel file (data source)
├── output/                        # Folder where output files are saved
│   ├── average_orders_by_meal.png # Barplot: Avg orders by meal type
│   ├── popular_dishes.png         # Barplot: Top 10 most popular dishes
│   └── merged_data.csv            # Cleaned and merged dataset
├── data_analysis_pipeline.py      # Python script for the pipeline
└── README.md                      # Project documentation

### Data Sources
The input file Assignment.xlsx consists of the following sheets:

UserDetails

Contains user information such as User ID, Total Orders, and Favorite Meal.
CookingSessions

Contains session details, including Session ID, Session Start, and Session End.
OrderDetails

Contains order-specific information such as Order Date and Dish Name.

## Steps in the Pipeline
1. Load Data
The data is loaded from multiple sheets in the Excel file.

2. Data Cleaning
Missing values are handled:
Total Orders is filled with 0 for missing values.
Rows with missing Dish Name or Order Date are dropped.
Dates are converted to datetime format.
Duplicate columns are removed.

3. Merge Datasets
The three datasets are merged using the User ID and Session ID as keys.

5. Analyze Relationships
Average total orders are grouped by Favorite Meal.
Most popular dishes are identified based on order counts.4

5. Visualizations
Barplot 1: Average total orders by favorite meal type.
Barplot 2: Top 10 most popular dishes based on order count.
Barplot 3: Average orders by age group.

7. Save Results
The final cleaned and merged dataset is saved as merged_data.csv in the output/ folder.

8.Business Recommendations:
1. Focus on promoting the most popular dishes to drive further engagement.
2. Enhance meal options that show high average orders (e.g., specific favorite meals).

