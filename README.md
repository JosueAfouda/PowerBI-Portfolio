![](/images/PBI.jpg)

---
# Power BI Portfolio: Dashboards and Reports in different Business Area: Healthcare, Human Resources, Job Market, Customer Churn
---

## ABOUT ME

Hello! I'm Adegbola Aremou 🤓, a Freelance Power BI Data Analyst | Course Creator & Coach | YouTuber.

***Below, you will find some of my Power BI projects:***


## Healthcare Data Analysis in Power BI

![](/images/Analyzing_Healthcare_Data_pages/Analyzing_Healthcare_Data_page1.png)

In healthcare, improving efficiency while maintaining high-quality patient care is a top priority. In this Power BI Project, I explored a real-world dataset (The health information in this dataset is not individually identifiable. This means the dataset does not contain personal health information.) to uncover hospital efficiency insights for a consulting company called HealthStat. I analyzed attributes impacting the patient length of stay (LOS) and cost and work to identify factors contributing to hospital differences. I used my Power Query DAX and Power BI Desktop skills to clean/transform data, create measures and generate insightful visualizations. To finish off, i have compiled it all together in a sophisticated business dashboard to communicate insights for the HealthStat team.

### Actionable Insights

By interacting with this dashboard, stakeholders can:

- **Identify High-Performing Hospitals:** Quickly pinpoint which hospitals are most efficient in terms of LOS and cost, and analyze their best practices to replicate success across the network.

- **Analyze LOS by Admission Type:** Filter the data to see how length of stay varies for elective, urgent, and emergency admissions, helping to streamline patient flow for each category.

- **Investigate Cost Drivers:** Drill down into the cost components for different treatments and patient demographics to uncover opportunities for cost savings.

- **Benchmark Performance:** Compare hospitals based on a variety of metrics, such as patient age, severity of illness, and medical condition, to set realistic performance benchmarks.

- **Optimize Resource Allocation:** Use the insights to better allocate staff, beds, and other resources to meet patient demand and reduce bottlenecks.


### LOS (Length Of Stay) Comparison

![](/images/Analyzing_Healthcare_Data_pages/Analyzing_Healthcare_Data_page2.png)

This page offers a comparative view of the average Length of Stay (LOS) across different hospitals. We can see that there are significant variations in LOS, with some hospitals consistently outperforming others. By filtering by admission type (Emergency, Urgent, Elective), we can uncover further insights. For instance, we might find that a particular hospital has a longer LOS for elective surgeries, suggesting inefficiencies in their pre-operative or post-operative processes. This data allows us to identify best practices at top-performing hospitals and implement them across the board to improve patient flow and reduce costs.

* **Network-level KPIs**

  * **Average LOS = 2.65 days** (the single metric driving bed-capacity and cost discussions).

  * **Total discharges ≈ 26,000** and **151 hospitals** in the dataset — this is a scalable, multi-site problem.

  * **627 surgeons** in scope — indicates opportunity for clinician-level variation analysis.

* **Drivers of LOS (Key Influencers panel)**

  * `apr_risk_of_mortality is Minor` → *decreases* average LOS by **1.84 days**.

  * `apr_severity_of_illness is Minor` → *decreases* LOS by **1.32 days**.

  * `patient_disposition is Home w/ Home Health Services` → *decreases* LOS by **0.87 days**.

  * Interpretation: clinical severity and mortality risk strongly increase LOS; effective discharge-to-home with home health shortens stays.

* **Facility-level variation (combo chart + side bars)**

  * The blue bars (total discharges) show large differences in volume across top 15 hospitals; the line (avg LOS) reveals spikes — some hospitals with moderate/low volumes have **very high LOS**, and some high-volume hospitals have modest LOS.
  * **Top 3 highest avg LOS**: *Kings County Hospital Center* = **12.0 days**, *Interfaith medical center* = **9.3**, *Memorial Hospital for Cancer and Allied Diseases* = **9.1**.

  * **Bottom 3 lowest avg LOS**: values around **1.4–1.7 days** — these low-LOS hospitals are practical models for best practice.

---

### Cost Comparison

![](/images/Analyzing_Healthcare_Data_pages/Analyzing_Healthcare_Data_page3.png)

This page delves into the cost side of the equation, breaking down the average cost per stay by hospital. The variations in cost are even more pronounced than the variations in LOS. By cross-referencing this data with the LOS data, we can identify hospitals that are not only efficient in terms of time but also in terms of cost. We can also drill down to see which specific procedures or departments are driving up costs at underperforming hospitals. This information is critical for making targeted interventions to improve financial performance without compromising patient care.

* **Overall hospital network overview**

  * **Average LOS:** 2.65 days

  * **Average Cost per Discharge:** **$21K**

  * **151 hospitals**, representing **26K total discharges** — strong dataset coverage for benchmarking both efficiency and financial performance.

* **Variation in cost efficiency across regions**

  * Hospitals in **Capital/Adirondack** and **Southern Tier** regions show **significantly lower average costs per discharge** — reductions of **$9.3K** and **$8.6K** respectively.

  * Other cost-efficient regions include **Central NY, Finger Lakes, and Western NY**, each showing average decreases between **$7.4K–$7.8K** compared to higher-cost peers.

  * This suggests meaningful geographic cost variation likely linked to differences in patient mix, labor rates, or operational practices.

* **High-cost hospitals**

  * **Top 3 hospitals by cost per discharge:**

    * *NYU Lutheran Medical Center* — **$85K**

    * *Olean General Hospital* — **$81K**

    * *Memorial Hospital for Cancer and Allied Diseases* — **$64K**

  * These outliers represent opportunities for targeted financial performance reviews to identify inefficiencies or special case mixes driving cost inflation.

* **Cost vs. LOS relationship (Scatter Plot)**

  * The **Average LOS vs. Average Cost per Discharge** chart shows a **weak-to-moderate positive trend** — hospitals with longer LOS generally incur higher discharge costs, but there is **not a perfect linear correlation**.

  * This suggests that some hospitals manage to maintain low LOS *and* moderate costs, pointing to **operational excellence models worth replicating**.

**Example of Insight Using Dashboard Interactivity**

> By selecting **“Capital/Adiron”** in the *Health Service Area* filter, the scatter plot immediately refocuses on a cluster of hospitals with **shorter LOS (<3 days)** and **below-average costs (<$15K per discharge)**.
>
> This interactive view highlights that the **Capital/Adirondack region combines both efficiency and cost control**, serving as a **benchmark area** for performance improvement across the network. Stakeholders could then drill down to specific hospitals in that region to uncover the practices — clinical pathways, resource utilization, or discharge planning — that enable this dual optimization of LOS and cost.

---

### Hospital Profile

![](/images/Analyzing_Healthcare_Data_pages/Analyzing_Healthcare_Data_page4.png)

This page provides a comprehensive, at-a-glance view of a selected hospital's performance. It includes key metrics such as the number of patients, average LOS, average cost, and patient demographics. This allows for a deep dive into the performance of a single hospital, making it possible to identify its strengths and weaknesses. For example, we can see if a hospital is admitting a higher proportion of high-risk patients, which might explain a longer LOS or higher costs. This detailed view is essential for conducting fair and accurate performance reviews and for developing targeted improvement plans.

Key findings for the University Hospital include:

* **Performance Overview**

  * **Average Length of Stay (LOS):** **2.56 days**, slightly below the network benchmark of **2.65 days** → strong operational efficiency.

  * **Average Cost per Discharge:** **$17K**, outperforming the network average of **$21K**, indicating effective cost management and resource utilization.

* **Case Mix & Patient Severity**

  * Majority of discharges (≈ **60–65%**) come from patients with **moderate severity of illness**, followed by **minor cases**, and a small share of **major cases**.

  * This balanced mix suggests University Hospital manages both routine and moderately complex patients effectively without excessive LOS or cost inflation.

* **Mortality Risk Profile**

  * Over **75%** of patients are categorized under **minor risk of mortality**, implying that most admissions are lower-risk procedures or recoveries — consistent with a lower average LOS.

  * Moderate and major risk cases are limited, suggesting that severe, resource-intensive cases are referred elsewhere or represent a small proportion of the hospital’s portfolio.

* **Diagnostic Drivers**

  * **Osteoarthritis** dominates discharges (**≈89%**) — likely reflecting a specialization in orthopedic surgery, particularly joint replacement or related elective procedures.

  * Other diagnoses (fractures, bone disorders, rheumatoid arthritis) form a small but relevant subset — indicating orthopedic care as a strategic focus area.

* **Patient Disposition Patterns**

  * Most patients (**≈77%**) are discharged **home or to self-care**, with another **10%** discharged **home with home health services**.

  * Only a small proportion go to **skilled nursing** or **inpatient rehab** facilities — showing effective discharge planning and relatively quick post-acute transitions.

**Example of Insight Using Dashboard Interactivity**

> By selecting **different hospitals** in the drop-down filter, stakeholders can **benchmark LOS and cost performance** relative to the network average gauges (2.65 days / $21K).
>
> For instance, selecting *University Hospital* instantly reveals that it performs **better than average in both LOS and cost**, and that its **case mix is dominated by moderate orthopedic cases with low mortality risk**.
>
> This interactive comparison allows decision-makers to **identify top-performing hospitals like University Hospital as operational benchmarks**, guiding best-practice sharing — such as efficient orthopedic workflows, early discharge protocols, or optimized resource allocation.

---

## Customer Churn Analysis in Power BI

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page1.png)

For subscription-based businesses, reducing customer churn is a top priority. In this Power BI Project, i investigated a dataset from an example telecom company called Databel and analyzed their churn rates. Analyzing churn doesn’t just mean knowing what the churn rate is: it’s also about figuring out why customers are churning at the rate they are, and how to reduce churn. I answered these questions by creating measures and calculated columns, while simultaneously creating eye-catching report pages.

### Actionable Insights

By interacting with this dashboard, stakeholders can:

- **Identify At-Risk Customer Segments:** Analyze churn by demographic data such as age, gender, and location to tailor marketing and retention efforts.

- **Understand the Impact of Contract Type:** See how churn rates differ between month-to-month, one-year, and two-year contracts to encourage longer-term commitments.

- **Evaluate the Role of Payment Methods:** Determine if there is a correlation between payment methods (e.g., credit card, bank transfer, electronic check) and customer churn.

- **Analyze the Effect of Additional Services:** Investigate how services like online security, tech support, and streaming TV influence customer loyalty.

- **Pinpoint Service Issues:** Drill down into customer complaints and technical support inquiries to identify and address operational issues that lead to churn.


### Overview

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page1.png)

This overview page provides a high-level summary of customer churn at Databel. It highlights the overall churn rate, the total number of churned customers, and the financial impact of this churn. The page is designed to give executives a quick snapshot of the health of the customer base and to alert them to any significant changes in churn trends. The key metrics are presented in a clear and concise way, allowing for immediate understanding and action.

### Age Groups

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page2.png)

This page segments customer churn by age group, revealing which demographics are most likely to churn. For example, we might discover that younger customers are more likely to churn than older customers. This insight would allow us to create targeted marketing campaigns and retention offers for different age brackets. Understanding the generational differences in customer loyalty is key to developing a successful, multi-faceted retention strategy.

### Contrat Type

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page3.png)

This page analyzes the impact of contract type on customer churn. It's no surprise that customers on month-to-month contracts are more likely to churn than those on longer-term contracts. This visualization quantifies that difference, showing exactly how much of a loyalty boost a one-year or two-year contract provides. This data can be used to inform pricing strategy and to design incentives that encourage customers to sign up for longer-term commitments.

### Payments and Contracts

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page4.png)

This page provides a deeper dive into the interplay between payment methods, contract types, and churn. For example, we might find that customers who pay by electronic check and are on a month-to-month contract have the highest churn rate. This kind of granular insight is invaluable for identifying high-risk customer segments and for developing targeted interventions. For instance, we could offer a discount to these customers if they switch to a more secure payment method and a longer-term contract.

### Extra Charges

![](/images/customer_churn_analysis_pages/customer_churn_analysis_page5.png)

This page examines the role of extra charges, such as for premium channels or extra data, in driving customer churn. It might reveal that customers who have a high number of extra charges are more likely to churn, perhaps because they feel they are not getting good value for their money. This insight could lead to a simplification of the pricing structure or to the creation of bundled packages that offer better value.

## Human Resources (HR) Analytics with PostgreSQL and Power BI

![](/images/hr_analytics_reporting_pages/hr_analytics_reporting_page1.png)

In this Power BI project, I explored a Human Resources (HR) dataset for a fictitious software company, Atlas Labs, to showcase my skills in Power BI. I focused on importing, cleaning, analyzing, and visualizing HR data to uncover meaningful insights.

I performed exploratory data analysis and leveraged DAX to create dynamic, interactive visualizations. My analysis included a deep dive into employee attrition, identifying key factors that influence turnover and providing actionable insights for improving retention.

The final deliverable was a professionally designed Power BI report with a clean, branded layout, highlighting critical HR metrics and insights for business decision-making.

### Actionable Insights

By interacting with this dashboard, stakeholders can:

- **Identify Attrition Hotspots:** Pinpoint the departments, job roles, and locations with the highest employee turnover.

- **Analyze the Impact of Compensation:** Explore the relationship between salary, pay raises, and attrition to ensure competitive compensation packages.

- **Assess Employee Satisfaction:** Correlate job satisfaction scores with attrition rates to identify areas for improvement in the work environment.

- **Understand Demographic Trends:** Analyze attrition by age, gender, and tenure to develop targeted retention initiatives for different employee groups.

- **Evaluate Performance and Attrition:** Investigate the connection between performance ratings and employee turnover to retain top talent.


Skills demonstrated: Power BI, Data Modeling, DAX, Data Visualization, Exploratory Data Analysis, HR Analytics, Report Design.

### Overview

![](/images/hr_analytics_reporting_pages/hr_analytics_reporting_page1.png)



### Demographics

![](/images/hr_analytics_reporting_pages/hr_analytics_reporting_page2.png)



### Performance Tracker

![](/images/hr_analytics_reporting_pages/hr_analytics_reporting_page3.png)



### Attrition

![](/images/hr_analytics_reporting_pages/hr_analytics_reporting_page4.png)



## Analyzing Job Market Data in Power BI

![](/images/Analyzing_Job_Market_pages/Analyzing_Job_Market_page1.png)

In this project, I explored a real-world job posting dataset for a fictional recruitment company, DataSearch, to analyze trends in the data science and analytics job market. I used Power Query to investigate, clean, and transform the data, uncovering which skills are most in-demand for data scientists, data analysts, and data engineers.

I applied DAX to create dynamic visualizations that highlighted key trends and insights. Finally, I combined all findings into an interactive, business-ready Power BI dashboard, enabling the DataSearch team to make informed decisions and answer critical questions about talent demand.

### Actionable Insights

By interacting with this dashboard, stakeholders can:

- **Identify In-Demand Skills:** Analyze which technical skills (e.g., Python, R, SQL, Tableau) are most frequently requested by employers for different job roles.

- **Track Job Title Trends:** See the rise and fall in demand for specific job titles like Data Scientist, Data Analyst, and Data Engineer.

- **Analyze Company Hiring Behavior:** Identify which companies are hiring the most and what their typical job requirements are.

- **Explore Geographic Trends:** Filter job postings by location to understand regional differences in demand and salary.

- **Advise on Skill Development:** Use the data to advise job seekers and corporate clients on the most valuable skills to develop for a career in data.


Skills demonstrated: Power BI, Power Query, DAX, Data Cleaning, Data Visualization, Dashboard Design, Job Market Analytics.

### Jobs

![](/images/Analyzing_Job_Market_pages/Analyzing_Job_Market_page2.png)



### Skills

![](/images/Analyzing_Job_Market_pages/Analyzing_Job_Market_page3.png)



### Company

![](/images/Analyzing_Job_Market_pages/Analyzing_Job_Market_page4.png)



## CONTACT DETAILS

*Let’s connect and see how we can build something useful together!*
<table>
  <tbody>
    <tr>
      <td>📧</td>
      <td><a href="mailto:josh.aremou229@gmail.com">josh.aremou229@gmail.com</a></td>
    </tr>
    <tr>
      <td>📍</td>
      <td>FR, FRANCE</td>
    </tr>
    <tr>
      <td>⬇️</td>
      <td><a href="https://drive.google.com/file/d/1Tt1t8BoWD-d6SeLtp9Bxwsvmt19PmTJG/view?usp=sharing">Download my CV</a></td>
    </tr>
    <tr>
      <td>🌐</td>
      <td><a href="https://www.linkedin.com/in/adegbola-aremou-0aa190390">The things I do daily on LinkedIn</a></td>
    </tr>
    <tr>
      <td>📺</td>
      <td><a href="https://www.youtube.com/c/JADATATECHCONSULTING">Watch my tutorials on YouTube</a></td>
    </tr>
  </tbody>
</table>
