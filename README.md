# Urban Mobility: EDA of Bike-Sharing Demand

A Python data analysis project exploring bike-sharing patterns using real-world rental data from 2011–2012.

This project is part of my learning journey after completing the **[Google Data Analysis with Python Specialization](https://www.coursera.org/specializations/google-data-analysis-with-python)**. I wanted to take the concepts covered in the course and apply them to an actual dataset rather than just work through isolated exercises.

I chose the Bike Sharing Dataset because it offers an interesting way to explore how people use shared bicycles throughout the day, across different days of the week, and under different weather conditions.

---

## Project overview

The main goal of this project was to explore bike-sharing demand and understand the patterns hidden in the data.

While working on it, I practised using Python, NumPy, Pandas, datetime operations, Matplotlib and Seaborn. I also got more comfortable working through data-quality checks, grouping and aggregating data, interpreting statistical results, and creating visualisations.

**The entire analysis is documented in one Jupyter Notebook.**

[**Open the Jupyter Notebook →**](notebook.ipynb)

## Questions I wanted to explore

- How are rentals distributed between casual and registered users?
- Which hours of the day have the highest and lowest rental activity?
- Is there a noticeable difference between weekday and weekend demand?
- How are weather conditions associated with bike rental demand?
- Are there unusually high or low rental observations in the dataset?

## Dataset

I used the **UCI Bike Sharing Dataset**, which contains hourly and daily bike rental records from 2011 and 2012.

For this analysis, I primarily used `hour.csv` because it provides the hourly information needed to explore demand throughout the day.

The dataset includes information such as:

- Date and hour of rental
- Season and weather conditions
- Temperature and humidity
- Casual and registered user rentals
- Total rental count

The weather measurements in the original dataset are normalised values, so they should not be interpreted directly as Celsius temperatures or humidity percentages.

**Original dataset:** [UCI Machine Learning Repository – Bike Sharing Dataset](https://doi.org/10.24432/C5W894)

## What I worked on

The notebook follows a complete exploratory data analysis workflow:

| Area | What I practised |
|---|---|
| Data loading | Reading CSV files using Pandas |
| Data inspection | Checking dimensions, columns, data types and statistics |
| Data cleaning | Checking missing values, duplicates and data consistency |
| Datetime | Extracting year, month, day and hour information |
| NumPy | Numerical calculations, arrays and statistical operations |
| Pandas | Filtering, grouping, aggregation and correlation |
| Matplotlib | Creating and customising charts |
| Seaborn | Statistical visualisations and heatmaps |
| Outlier detection | Applying the Interquartile Range (IQR) method |

## Visualisations

I created the following charts to make the patterns easier to understand.

### 1. Average rental demand by hour

![Hourly Demand](outputs/charts/hourly_demand.png)

This chart shows how rental activity changes throughout the day. The evening has the strongest average demand, while activity is lowest during the early morning hours.

### 2. Casual vs registered users

![User Distribution](outputs/charts/user_distribution.png)

Registered users account for the majority of rentals, while casual users make up a smaller share.

### 3. Weekday vs weekend demand

![Weekday vs Weekend](outputs/charts/weekday_vs_weekend.png)

A comparison of average hourly rental demand between weekdays and weekends. The weekday average is slightly higher in this dataset.

### 4. Weather and rental correlation

![Correlation Heatmap](outputs/charts/correlation_heatmap.png)

This heatmap helped me explore how weather variables relate to total bike rentals. Temperature has a positive correlation with rental demand, while humidity has a negative correlation.

### 5. Hourly demand across days of the week

![Weekday Hour Heatmap](outputs/charts/weekday_hour_heatmap.png)

This was one of the more interesting visualisations to explore. It makes it easier to compare hourly rental patterns across all seven days of the week.

---

## A few findings

Here are some of the observations from my analysis:

- **3,292,679 total rentals** were recorded across the dataset.
- Registered users accounted for approximately **81.17%** of all rentals.
- The average rental demand peaked at **17:00 (5 PM)**, with approximately 461 rentals per hour.
- The lowest average demand occurred at **04:00 (4 AM)**, with approximately 6 rentals per hour.
- Weekday average hourly demand was approximately **4.29% higher** than weekend demand.
- Temperature showed a positive correlation with rental demand (approximately **0.405**), while humidity showed a negative correlation (approximately **-0.323**).

These are descriptive observations from the dataset. Correlation does not establish causation, and the results should not automatically be generalised to other bike-sharing systems or current usage patterns.

## What I learned

This project gave me an opportunity to connect several concepts from the course and use them together in one workflow.

I became more comfortable with Pandas operations, numerical calculations using NumPy, working with dates and times, and building visualisations. I also learned that analysing data is not just about generating charts—it involves checking the quality of the data, understanding what the numbers represent, and being careful about the conclusions we draw.

There were also errors and small problems along the way, which gave me a chance to understand the code rather than simply focus on getting an output.

## Running the project

If you want to explore the notebook or run the analysis yourself, follow these steps.

**1. Clone the repository**

```bash
git clone https://github.com/KevinSiddhpura/urban-mobility-data-analysis.git
cd urban-mobility-data-analysis
```

**2. Install the required libraries**

```bash
pip install -r requirements.txt
```

**3. Start Jupyter**

```bash
jupyter notebook
```

Open `notebook.ipynb` and run the cells from top to bottom.

The notebook expects `hour.csv` to be available inside the `data/` directory. The charts will be generated automatically inside `outputs/`.

## Use of AI

I used AI as a learning assistant for understanding concepts, troubleshooting code, planning analysis, and preparing project documentation. I reviewed the suggestions, ran the code, and examined the results while building the notebook.

## Acknowledgements

- **Dataset:** [UCI Machine Learning Repository – Bike Sharing Dataset](https://doi.org/10.24432/C5W894)
- **Learning:** [Google Data Analysis with Python Specialization – Coursera](https://www.coursera.org/specializations/google-data-analysis-with-python)
- **Tools:** Python, Jupyter Notebook, NumPy, Pandas, Matplotlib and Seaborn.

---

*This is a learning project, and a practical step in developing my data analysis skills. There is still plenty more to explore, but this was a good opportunity to take what I learned and apply it to real data.*