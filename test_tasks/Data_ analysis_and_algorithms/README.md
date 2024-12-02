# Python Tasks for Data Analysis and Algorithms

This repository contains solutions for various Python-based tasks, including data analysis, mathematical calculations, and handling user inputs. Each task focuses on solving specific real-world problems through coding, using basic and advanced Python concepts.

## Task 1: Calculate Average Daily Sales

Given sales data and stock levels for a product over a certain period, this task calculates the average daily sales for the last 30 days, considering only the days when the stock level is greater than zero. The solution involves processing time-series data and performing simple aggregation to compute the desired metric.

### Steps:
1. Filter days where the stock level is greater than zero.
2. Calculate the average sales per day over the last 30 days.

## Task 2: Seasonal Coefficients Calculation

This task involves calculating the seasonal coefficients for different product categories. By analyzing daily sales data for the year 2019, the goal is to calculate the seasonality for each category and classify the seasonality type based on the observed patterns. This analysis is supported by generating visualizations for better understanding.

### Steps:
1. Calculate the seasonality coefficient for each product category for every month.
2. Classify the products into different seasonal types (e.g., strong seasonality, moderate seasonality).
3. Group products by their seasonality type and display them separately.
4. Plot the seasonal coefficients for the top 5 product categories within each seasonality type.

## Task 3: Color Mixing Program

This program accepts three standard color inputs (blue, red, green) and outputs the result of mixing two of them. It ensures proper error handling to prevent invalid color combinations and produces the corresponding mixed color result.

### Example:
- Input: `blue` + `red`
- Output: `purple`

The program can handle invalid or unexpected inputs and provides clear error messages.

## Task 4: Factorial Program with Odd Digit Output

This program calculates the factorial of a user-provided natural number and outputs only the odd digits of the resulting value. The program includes error handling to manage all possible input errors.

### Example:
- Input: `6`
- Output: `720` → `70` (only odd digits are displayed).

The program will handle invalid inputs gracefully and ensure that only valid natural numbers are processed.

## Libraries Used
- **Python Standard Library**: For basic operations, file handling, and error management.
- **Pandas** (if applicable): For data processing and analysis
