# 📊 AI and ML Job Market Trends

## 📌 Overview
This project explores **trends in the Artificial Intelligence (AI) and Machine Learning (ML) job market for 2023** using real-world datasets from Kaggle.  
The focus is on analyzing **salaries, job postings, skills, demand by state, and work settings** to provide insights into the current AI/ML industry landscape.

I applied **data cleaning, merging, statistical testing, and visualization** techniques to answer key research questions about the job market.


**Course:** IST 652 — Final Project  

## 📂 Datasets (Kaggle Sources)
1. [AI/ML Salaries Dataset](https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2023)  
   - Includes job title, experience level, company size, location, and compensation (USD).  

2. [AI/ML Job Postings Dataset](https://www.kaggle.com/datasets/ruchi798/data-science-job-postings-from-glassdoor)  
   - Job postings with columns such as `job_title`, `company_name`, `city`, `job_type`, `job_level`, and `job_link`.  

3. [AI/ML Job Skills Dataset](https://www.kaggle.com/datasets/PromptCloudHQ/data-scientist-job-descriptions)  
   - Lists job-related skills linked to each job (via `job_link`).  

4. [AI/ML Job Summary Dataset](https://www.kaggle.com/datasets/PromptCloudHQ/data-scientist-job-descriptions)  
   - Contains textual job summaries/descriptions for each posting.  

## 🛠️ Preprocessing
1. **Fuzzy Matching for Job Titles**  
   - Used `thefuzz` to align inconsistent job titles (e.g., *"Sr. ML Engineer"* vs *"Senior Machine Learning Engineer"*).  

2. **Merging Datasets**  
   - `job_postings + job_skills` (via `job_link`).  
   - Added `job_summary`.  
   - Merged with `salaries` using fuzzy-matched job titles.  

3. **Data Cleaning**  
   - Handled missing values.  
   - Standardized columns (e.g., job type labels: Remote, Onsite).  


## 🔍 Research Questions & Methods
We explored the following:

1. **Which AI/ML job roles are most in demand in the U.S., and how do their salaries compare?**  
   - Aggregated postings by role, calculated average salaries.  

2. **How do salaries differ between Associate vs Senior roles?**  
   - Two-sample T-test.  

3. **How does demand vary across U.S. states?**  
   - Extracted state from location, visualized heatmap.  

4. **Do remote jobs pay differently than onsite jobs?**  
   - Bootstrapping salaries (remote vs onsite).  

5. **Which companies are top recruiters, and how do their salaries compare?**  
   - Company-wise aggregation vs industry average.  

6. **What are the top 10 most in-demand technical skills?**  
   - Exploded `job_skills` column, frequency counts.  

7. **Is there a relationship between skill count and salary?**  
   - Pearson correlation + scatter plot with regression line.  


## 📊 Tools & Libraries
- **Python**: pandas, numpy, seaborn, matplotlib, thefuzz  
- **Statistics**: T-test, Bootstrapping, Pearson correlation  
- **Visualization**: Bar plots, heatmaps, scatter plots  


## 📈 Outputs
- Horizontal bar plots (job roles vs salary).  
- Heatmap of job demand across states.  
- Bootstrap salary distribution plots (remote vs onsite).  
- Company salary comparison chart.  
- Top skills bar plot.  
- Scatter plot of skills vs salary.  


## ✅ Key Insights
- **Experience matters** → Senior roles earn significantly more.  
- **Remote jobs pay better** than onsite roles.  
- **Top-paying skills**: Python, SQL, AWS, TensorFlow, PyTorch.  
- **Top recruiters**: Certain companies hire at scale but may pay below/above average.  
- **Skills vs Salary** → weak correlation, but specialized skills boost pay.  

