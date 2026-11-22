# Historical E-commerce Sales Analysis and Forecasting

An exploratory data analysis project focused on understanding e-commerce sales performance, product and category revenue, discount patterns, customer orders, cancellations, returns and near-term sales trends.

## 1. Project Overview

This project analyses historical e-commerce transaction data to identify business trends and generate actionable recommendations.

The analysis combines order records with product information to investigate sales performance over time and answer important business questions.

## 2. Dataset

The project uses two CSV files:

| Dataset | Records | Columns |
|---|---:|---:|
| Orders | 50,120 | 8 |
| Products | 20 | 4 |

**Dataset source:** [Kaggle – E-commerce Sales Data Analysis and EDA](https://www.kaggle.com/datasets/erfan4524/e-commerce-sales-data-analysis-and-eda/data)

The CSV files are not included in this repository and must be downloaded separately.

## 3. Data Preparation

The notebook covers:

- Missing-value identification and treatment.
- Duplicate record removal.
- Invalid and negative quantity checks.
- Date conversion and data type handling.
- Integration of orders and product datasets using `ProductID`.
- Feature engineering for gross sales, net sales, year, quarter and month.

Net sales are calculated using the percentage discount:

`NetSale = GrossSale × (1 − Discount)`

The corrected calculation is applied in the notebook.

After cleaning, the orders dataset contains 49,866 records, which are combined with product information for the analysis.

## 4. Business Questions

The project investigates eight areas:

1. How has sales performance changed over time?
2. Which product category generates the most revenue?
3. How does discount level relate to net sales?
4. Which categories have the highest return and cancellation counts?
5. Which products are purchased most frequently?
6. Are there seasonal patterns across months or quarters?
7. What does the recent sales trend suggest about near-term performance?
8. How significant are cancellations and returns, and how do they change over time?

## 5. Key Findings

The following figures are from the corrected notebook outputs.

| Finding | Result |
|---|---:|
| Cleaned orders | 49,866 |
| Completed orders | 45,873 |
| Cancelled orders | 2,463 |
| Returned orders | 1,530 |
| Highest monthly net sales | 120,891.70 (March 2024) |
| Lowest monthly net sales | 68,927.60 (February 2026) |
| Electronics category net sales | 1,624,610.50 |
| July 2026 moving-average estimate | 78,849.62 |

Electronics was the strongest revenue-generating category.

The analysis also identified a substantial decline in monthly sales during 2026 compared with the preceding two years.

## 6. Forecasting Approach

A simple three-month moving average is used to examine recent sales trends and estimate near-term performance.

The July 2026 estimate is 78,849.62, based on the average of the previous three months.

This is a basic baseline forecasting approach. It does not explicitly model seasonality, external economic conditions or other business factors.

## 7. Technologies Used

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Exploratory Data Analysis (EDA)
- Data Cleaning and Preprocessing
- Data Visualization
- Time-Series Analysis
- Moving-Average Forecasting

## 8. How to Run the Project

### Clone the repository

```bash
git clone https://github.com/KamranAzmat126/Historical-Ecom-Sales-Analysis-and-Forecasting.git
cd Historical-Ecom-Sales-Analysis-and-Forecasting
```

### Install dependencies

```bash
pip install pandas matplotlib jupyter
```

### Download the datasets

Download `orders.csv` and `products.csv` from the Kaggle dataset.


### Update the notebook paths

The notebook currently contains local Windows file paths. Replace the two dataset-loading paths.


### Run the notebook

```bash
jupyter notebook
```

Open `Historical_Sales_Analysis_and_Forecasting.ipynb` and execute the cells.

## 9. Business Recommendations

Based on the findings, the project recommends:

- Investigating the underlying causes of the 2026 sales decline.
- Prioritising high-performing products and categories.
- Evaluating discounts against profitability.
- Monitoring cancellations, returns and net sales regularly.
- Incorporating additional business data to improve future forecasting.

