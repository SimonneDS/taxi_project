
````markdown
# 🚕 Chicago Taxi Trip Analysis and Weather Correlation

## 📝 Project Description
This project aims to analyze taxi trip data within the city of Chicago. The primary focus is on identifying the most popular taxi companies, the areas with the highest drop-off demand, and the influence of **weather conditions** (specifically rain/bad weather) on trip duration.

The analysis includes applying inferential statistics techniques, such as the **Mann-Whitney U Test**, to determine if there is a statistically significant difference in the average trip duration between days with good weather and rainy days for a specific route (Loop to O'Hare International Airport).

## 💾 Data
The following datasets (provided as CSV files), extracted from a SQL database, were used for this analysis:

* **`moved_project_sql_result_01.csv`**: Contains the total number of trips (`trips_amount`) per taxi company (`company_name`).
* **`moved_project_sql_result_04.csv`**: Contains the average number of trips (`average_trips`) to different drop-off locations (`dropoff_location_name`).
* **`moved_project_sql_result_07.csv`**: Contains detailed trip data, including start time, weather conditions, and duration in seconds (`duration_seconds`), used for the weather-duration statistical analysis.

## 📊 Analysis and Objectives

The main objectives and findings of the project include:

1.  **Top Taxi Companies:** Identify and rank the taxi companies with the highest number of recorded trips.
2.  **Popular Drop-off Points:** Determine the areas in Chicago with the highest average drop-off volume.
3.  **Impact of Weather on Trip Duration:**
    * Focusing on trips between the **Loop** and **O'Hare International Airport (ORD)**.
    * Using the **Mann-Whitney U Test** to contrast the null hypothesis that trip duration is the same on rainy Saturdays compared to non-rainy Saturdays.

## 🛠️ Technologies and Libraries

* **Programming Language:** Python
* **Data Analysis:** Pandas, NumPy
* **Statistics:** SciPy (for the Mann-Whitney U test)
* **Visualization:** Matplotlib, Seaborn
* **Development Environment:** Jupyter Notebook (`notebook.ipynb`)

## 🚀 How to Run the Project

1.  **Install Python dependencies:**
    ```bash
    # Example of key library installation
    pip install pandas numpy scipy jupyter matplotlib seaborn
    ```
2.  **Open the Notebook:** Execute the `notebook.ipynb` file in a Jupyter or JupyterLab environment.
3.  **Run the cells:** Follow the notebook's flow to replicate the complete analysis and view the visualizations.

### Business Implications & Recommendations
* The statistical findings provide concrete evidence for improving operational strategy:

* ETA Modeling: Transportation companies must integrate real-time weather data as a primary feature in their Estimated Time of      Arrival (ETA) algorithms to manage customer expectations and prevent service dissatisfaction on rainy days.

* Dynamic Pricing Strategy: The validated increase in trip time justifies implementing a dynamic pricing mechanism during inclement weather, compensating for the increased operational duration and maintaining driver fleet viability.

* Proactive Fleet Management: Adopt predictive scheduling to preemptively allocate more drivers to high-traffic areas (Loop, Airport) ahead of forecasted poor weather, mitigating the impact of reduced vehicle speed and increased travel time.

## Key Conclusions

Based on the data analysis performed, the key conclusions are:

* The company **Flash Cab** registered the highest number of trips overall, with 19,558 trips.
* The areas with the highest average number of drop-offs are **Loop** (10,727.47 trips), **River North** (9,523.67 trips), and **Streeterville** (6,664.67 trips).
* **Statistical Test Result (Mann-Whitney U):** The statistical analysis (testing the route from the Loop to O'Hare) led to the **rejection of the null hypothesis**.
* This suggests that the average duration of trips **does change** on rainy Saturdays compared to Saturdays with good weather. In other words, **adverse weather conditions appear to have a statistically significant effect on the travel time.**
````
