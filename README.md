# 📊 Skill Demand Analysis in Indian Job Postings

This project analyzes job listings from India to identify the most in-demand technical skills across various job roles. Using Python-based data processing and visualization tools, it presents both raw skill frequencies and normalized percentages to reveal deeper insights into industry expectations.

---

## 📁 Dataset

The dataset used is `data_jobs.csv`, which contains job postings scraped from multiple online sources. Each record includes:

- 🧠 `job_title_short` – Simplified job title (e.g., Data Scientist, Data Analyst)
- 🛠 `job_skills` – A list of skills required for the job
- 🌍 `job_country` – Country of the job listing
- 💰 `salary_in_usd` – (Optional) salary details
- 📅 `job_posted_date` – Date when the job was posted

---

## 🛠️ Tools & Libraries

- **Pandas** – For data wrangling and transformation
- **Matplotlib** – For basic visualizations
- **Seaborn** – For enhanced, styled visualizations
- **AST** – To safely convert stringified lists into actual Python lists

---

## 🔍 What This Project Does

### 1. 🇮🇳 Focus on Indian Job Listings
Filters data to only include jobs from **India** for focused analysis.

### 2. 💥 Skill Frequency Analysis
- Explodes the `job_skills` list so each skill becomes a row.
- Groups by both `job_skills` and `job_title_short` to count how many times each skill appears per role.

### 3. 📊 Visualization 1: **Top 5 Most Common Skills per Job Title**
- Picks the top 3 job titles with the most listings.
- For each, plots the **top 5 most frequently mentioned skills**.
- Uses horizontal bar charts for better readability.

📌 Example:  
A job title like “Data Analyst” might show:
- SQL (40,000 mentions)
- Excel (35,000 mentions)
- Python (30,000 mentions)  
…and so on.

### 4. 📈 Visualization 2: **Skill Percentage Likelihood**
- Normalizes skill mentions by dividing `skill_count` by total jobs for that title.
- Plots **likelihood (%)** that a job of a certain title will request a given skill.
- Adds percentage labels next to each bar.

📌 Example:  
If 80% of “ML Engineer” postings ask for “TensorFlow,” this gets reflected visually.

---

## 📷 Visual Previews

### 🔹 Skill Count Plot:
![Skill Count](3.project/images/top_3_jobs_skills.png)

### 🔸 Skill Percentage Plot:
![Skill Percent](3.project/images/skill_demand.png)

---

### Insights

📊 Plot 1: Counts of Skills Requested in Indian Job Postings
This chart shows raw frequency of skill mentions in the top 3 most common job titles.

✅ Data Analyst:
SQL dominates with the highest mentions.

Python and Excel are closely tied in demand.

Tableau and Power BI appear as popular BI tools but with fewer mentions.

✅ Data Engineer:
SQL and Python remain dominant, with SQL slightly ahead.

Spark, AWS, and Azure indicate strong demand for big data and cloud skills.

✅ Data Scientist:
Python is the most requested skill, reaffirming its central role.

SQL and R are still relevant.

Cloud and visualization tools like AWS and Tableau show modest demand.

📈 Plot 2: Likelihood of Skills Requested (%-based Normalized View)
This plot normalizes skill counts by the total number of job postings for each role, giving a true sense of how likely a skill is to appear in a posting for that role.

✅ Data Analyst:
Over 51% of job listings require SQL.

Python and Excel are nearly equally important (~35%).

Tableau and Power BI show moderate demand (~21–27%).

✅ Data Engineer:
SQL is required in 68% of job posts — the highest among all titles.

Python follows closely at 60%.

Spark, AWS, and Azure all hover between 35–37%, showing demand for distributed computing and cloud platforms.

✅ Data Scientist:
Python dominates with a 69.6% requirement rate.

SQL is also important (47.9%), followed by R at 32.6%.

Cloud & BI tools like AWS (19.4%) and Tableau (18.3%) trail behind, indicating they're desirable but not mandatory.


Data Engineers need to be particularly strong in cloud and big data platforms.

Data Scientists benefit from statistical programming (R) in addition to Python and SQL.

Visualization skills (e.g., Tableau, Power BI) are more emphasized in Data Analyst roles.
