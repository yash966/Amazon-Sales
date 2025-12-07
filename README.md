## Amazon Sales Dataset Analysis Notebook

This Colab notebook provides a step-by-step analysis of the Amazon Sales Dataset, which contains detailed information on products sold on Amazon. The data includes product details (name, category, prices, discount, ratings), user reviews, review content, reviewer information, and product images/links. The dataset is valuable for understanding consumer preferences, sales trends, characteristics driving purchases, and for generating actionable recommendations to optimize product development and marketing strategies.

### Dataset Overview

- **Rows:** 1,465 (each corresponding to a product)
- **Columns:** 16, including `product_id`, `product_name`, `category`, `discounted_price`, `actual_price`, `discount_percentage`, `rating`, `rating_count`, `about_product`, `user_id`, `user_name`, `review_id`, `review_title`, `review_content`, `img_link`, and `product_link`.
- All columns are initially of type `object` with some columns containing currency (`₹`) or percentage (`%`) symbols.

### Approach

1. **Objectives:**  
   The notebook begins by outlining the objectives for the analysis — to explore product categories, prices, ratings, and sales patterns; extract insights to inform business strategies; and recommend ways to improve products and communication with customers.

2. **Data Import:**  
   The dataset is imported from Kaggle using `kagglehub`. The files are loaded and displayed for verification.

3. **Data Loading:**  
   The main CSV, `amazon.csv`, is loaded into a pandas DataFrame, referred to as `df`.

4. **Initial Data Exploration:**  
   - The first five rows are displayed to get a snapshot of the data.
   - Columns' names, their data types, and the overall shape of the dataset are checked.
   - Missing values are identified (with only 2 missing entries in `rating_count`).

5. **Data Cleaning & Preprocessing:**  
   - Currency symbols (`₹`) and commas are stripped from price columns (`discounted_price` and `actual_price`).
   - Percentage symbols (`%`) are removed from the `discount_percentage` column.
   - These columns are converted to appropriate numerical types (`float`).
   - The discount percentage is normalized to a 0-1 scale (by dividing by 100).
   - The DataFrame is prepared for further exploratory data analysis and modeling.

### Usage

You can use this notebook to understand the workflow for analyzing sales and review data from Amazon, including:
- Preparing and cleaning data for analysis.
- Identifying key data points and missing values.
- Converting categorical and textual data into useful formats.
- Visualizing and uncovering actionable trends for business strategy.

This notebook serves as a foundation for deeper analysis, such as product rating trends, price sensitivity, category performance, and reviewer sentiment exploration.
