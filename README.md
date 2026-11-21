# What Drives Order Value? An Analysis of Online Shopping Orders in India

Data analysis project in Python (pandas, NumPy, Matplotlib, Seaborn) on a synthetic online shopping dataset.

**Name:** Siddhant Chauhan  
**Admission No:** 2026B01010381  
**Branch / Section:** CSE / 13  
**Email:** siddhant.26b01010381@abes.ac.in

## Business Problem

An online store sells in five cities and five product categories, but its order values vary a lot (from ₹150 to ₹6,440). The sales and marketing team wants to know what drives order value and which orders are weak, so they can decide where to spend their promotion budget.

## Questions Answered

1. What does order value look like overall?
2. Do items in the cart and time on site affect order value?
3. Does order value differ by category, city, payment method or customer type?
4. Which orders need attention (Low Value: under ₹1,500)?

## Dataset

- File: `shopping_data.csv` (synthetic, created with an AI tool)
- 255 rows and 11 columns in the raw file, 250 rows after cleaning
- Outcome column: `Order_Value_INR`

## Cleaning Summary

| Problem | Fix |
|---|---|
| 5 duplicate rows | Removed |
| Missing values in `Time_On_Site_Min` (5) and `Delivery_Days` (4) | Filled with the median |
| Missing values in `Payment_Method` (6) and `Customer_Type` (6) | Filled with "Unknown" |
| 7 inconsistent `City` spellings | Stripped spaces, fixed the case |
| 2 impossible values in `Discount_Percent` | Replaced with the median |

New columns created: `Value_Per_Item`, `Order_Segment`, `Delivery_Speed`, `Value_Status`.

## Key Findings

- The average order is ₹2,598 and the median is ₹2,520.
- Order value rises with items per order (r = 0.52) and with time on site (r = 0.40). Discount and delivery days show almost no link.
- Electronics orders average ₹3,724, about 2.2 times Beauty (₹1,674).
- 63 orders (25.2%) are Low Value. Beauty (48.6%) and Grocery (46.2%) have the highest share.

## Recommendations

- Use bundles or free-shipping limits to add one more item per cart.
- Improve Beauty and Grocery first with combo deals.
- Do not rely on deeper discounts or faster delivery to raise order value.

## Project Structure

```
Online-Shopping-Project/
├── data/
│   ├── raw/          shopping_data.csv
│   └── processed/    shopping_data_cleaned.csv
├── notebooks/        analysis notebook
├── images/           charts
├── documents/        SRS and presentation
└── README.md
```

## How to Run

1. Clone the repository:
   `git clone https://github.com/siddhantchauhan26/Online-Shopping-Project.git`
2. Install the libraries: `pip install pandas numpy matplotlib seaborn jupyter`
3. Open the notebook in the `notebooks` folder and run all cells from top to bottom.

## Tools Used

Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, VS Code, GitHub


The dataset was created with an AI tool. The cleaning, analysis, charts and insights are my own work.

