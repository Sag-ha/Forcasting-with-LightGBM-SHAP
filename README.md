

This role is for a **Demand Forecasting Data Scientist** responsible for **model stack optimisation**. The current forecasting stack consists of multiple algorithms, including the one you will be working with in this case study: **LightGBM (LGBM)**.

The interview assessment will be weighted as follows:

* **Case study optimisation outcome: 50%**
* **Coding test: 30%**
* **Communication & Motivation: 20%**

The outcome of the case study will mainly be assessed on two aspects:

1. **Confidence index improvement**
   How many `ForecastItem`s are classified as `dark_green` or `green` after your optimisation.

2. **Forecast quality by visual inspection**
   Whether the forecasts for items classified as `dark_green` or `green` are genuinely meaningful when inspected visually. You can use `inspection.py` for this.

   Sometimes a model may perform well statistically on the holdout set, but the future forecast may still look poor or unrealistic. We are interested in both the metric performance and the practical quality of the forecast. As for the business point of view, the factories only care about if the numbers we tell them to produce is accurate or not.

For the optimisation process, I encourage you to use Excel or any other tracking method to document the experiments you have run. During the interview, we will discuss not only your final results, but also the process you followed, the decisions you made, and your reasoning.

You may focus first on:

* Feature engineering
* Feature selection
* Hyperparameter tuning

If you have additional capacity and would like to explore further improvements, you are welcome to do so.

### Data briefing

The input file is located at:

`data/HistoricalSales.csv`

The columns are mostly self-explanatory:

* `ForecastItem`
* `SKU_Type`
* `Segment`
* `WeekStartDate`
* `CalendarWeek`
* `TotalWeeklySales`

A few points to highlight:

* `TotalWeeklySales` is the target column.
* `Segment` is another way of describing the SKU type at a more granular level.
* `CalendarWeek` is capped at 52 weeks per year.

