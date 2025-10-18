# Project Title: Hotel Booking Cancellation Analysis | Revenue Optimization 🏨

Analyzing historical booking data to identify key cancellation drivers and provide strategic advice for pricing and marketing to increase hotel revenue and occupancy.

---

## Table of Contents
- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset & Assumptions</a>
- <a href="#tools-technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning-preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA) & Key Insights</a>
- <a href="#research-questions-key-findings">Research Questions & Key Findings</a>
- <a href="#final-recommendations">Final Recommendations</a>
- <a href="#future-work">Future Work</a>
- <a href="#how-to-run-this-project">How to Run this Project?</a>
- <a href="#author-contact">Author & Contact</a>

---

<h2 id="overview">Overview</h2>

This project is a detailed analysis of high cancellation rates at **City Hotel** and **Resort Hotel**. We evaluate factors like price, booking channel, and time of year using Python and its data science libraries. The goal is to provide **thorough business advice** to lower cancellations, thereby boosting room occupancy and revenue generation efficiency.

---

<h2 id="business-problem">Business Problem</h2>

High cancellation rates have resulted in **fewer revenues** and less than ideal hotel room use for both hotels. The core business challenge is to understand the variables driving these cancellations—with a core hypothesis that **price is the major factor**—to implement more effective and proactive operational and marketing decisions.

---

<h2 id="dataset">Dataset & Assumptions</h2>

The analysis uses historical hotel booking data from **2015 to 2017**.

* **Assumption 1:** No unusual occurrences between 2015 and 2017 will have a substantial impact on the data used.
* **Assumption 2:** The information is still current and can be used efficiently for planning.
* **Assumption 3:** The hotels are not currently using any of the suggested solutions.

---

<h2 id="tools-technologies">Tools & Technologies</h2>

* **Programming:** **Python**
* **Libraries:** **Pandas** (for data manipulation), **Matplotlib** and **Seaborn** (for visualization).
* **Tools:** Jupyter Notebook or similar Python environment.

---

<h2 id="project-structure">Project Structure</h2>

* `hotel_bookings.csv`: The raw dataset file.
* `hotel_booking_cancelation-data_analysis.ipynb`: The primary analysis notebook containing the code provided.
* `Business Problem and Report`: Final presentation and summary report (output).
* `README.md`: Project summary.

---

<h2 id="data-cleaning-preparation">Data Cleaning & Preparation</h2>

This phase, as executed in the code, ensures data quality:
1.  Converted the `reservation_status_date` column to the correct **datetime** format.
2.  Dropped the **highly sparse** columns: `company` and `agent`.
3.  Removed all remaining **NaN values** (e.g., in `country`, `children`).
4.  Outliers were handled by filtering records where `children` $\ge 10$ and `babies` $\ge 8$.
5.  A new column, `month`, was extracted from the `reservation_status_date` for time-series analysis.

---

<h2 id="exploratory-data-analysis-eda">Exploratory Data Analysis (EDA) & Key Insights</h2>

EDA confirms the project's hypotheses and focuses on visualizing cancellation distributions across key variables.

* **Overall Cancellation:** Approximately **37.04%** of reservations are canceled.
* **Price Correlation (Hypothesis Confirmed):** The average daily rate (ADR) for **canceled bookings is consistently higher** than for not-canceled bookings, strongly confirming that **higher price leads to higher cancellation**.
* **Hotel Type:** **Resort Hotel** has a slightly higher cancellation rate (**39.95%**) than City Hotel (**37.49%**).
* **Time:** **January** has the highest raw count of canceled bookings, confirming it as a critical month for revenue loss.
* **Origin:** **Portugal (PRT)** accounts for the largest share of total cancellations among all countries.
* **Market Segment:** The **Online Travel Agents (OTA)** segment contributes the highest volume of total bookings, and consequently, a high percentage of cancellations.

---

<h2 id="research-questions-key-findings">Research Questions & Key Findings</h2>

**Q1: What are the variables that affect hotel reservation cancellations?**
* **Primary Variable:** The **Average Daily Rate (ADR)** is the strongest factor.
* **Secondary Factors:** Hotel Type (**Resort**), Booking Channel (**OTA**), and Arrival Month (**January**).

**Q2: How can we make hotel reservations cancellations better?**
* By using price recommendations to proactively reduce cancellation risk.

**Q3: How will hotels be assisted in making pricing and promotional decisions?**
* By providing time-specific (January) and hotel-type-specific (Resort Hotel weekends/holidays) advice for targeted discounting.

---

<h2 id="final-recommendations">Final Recommendations</h2>

1.  **Dynamic Pricing:** **Lower the rates** or offer **discounts** for specific hotels or segments, especially during peak ADR periods, to mitigate the confirmed link between high price and cancellation.
2.  **Resort-Specific Offers:** Provide a **reasonable discount on room prices on weekends or holidays** at the Resort Hotel to address its higher cancellation ratio and higher ADR during those times.
3.  **January Campaign:** Launch targeted **campaigns or marketing** efforts in **January** to increase confirmed bookings and utilize rooms during the month with the highest cancellations.
4.  **Service Quality Focus:** **Increase quality of services** in **Portugal** to address the high cancellation volume from this country.

---

<h2 id="future-work">Future Work</h2>

1.  **Predictive Modeling:** Develop a **machine learning classification model** (e.g., using `scikit-learn`) to predict cancellation risk and enable **dynamic overbooking** or proactive retention offers for high-risk bookings.
2.  **Waitlist Optimization:** Further analyze the relationship between `days_in_waiting_list` and cancellation outcomes to create an optimal **waitlist release policy**.
3.  **Segment Deep Dive:** Conduct a granular analysis of **Online Travel Agent (OTA)** cancellations to determine if specific OTA platforms or booking characteristics contribute disproportionately to the cancellation rate, allowing for targeted contract renegotiation or incentive programs.

---

<h2 id="how-to-run-this-project">How to Run this Project?</h2>

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Shazmeengithub/hotel_booking_cancelation-data_analysis-Python
    ```
2.  **Install Dependencies:**
    ```bash
    # Install the libraries used in the code
    pip install pandas matplotlib seaborn
    ```
3.  **Execute the Analysis:**
    * Open and run the `hotel_booking_cancelation-data_analysis.ipynb` file to execute the code and reproduce the analysis, visualizations, and insights.

---

<h2 id="author-contact">Author & Contact</h2>

* **Author:** Shazmeen Shaikh
* **Contact:** https://www.linkedin.com/in/shazmeen-shaikh-30bb63237/
