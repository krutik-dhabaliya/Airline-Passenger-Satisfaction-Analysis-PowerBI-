
# Airline Passenger Satisfaction Analysis using Power BI

## Project Overview and Business Objectives
This project is based in the airline industry, where passenger satisfaction plays a crucial role in customer retention, service quality improvement, and overall business performance. Airlines collect passenger feedback across various touchpoints, but deriving clear and actionable insights from this data remains a challenge.

The analysis was conducted to address the lack of clarity around which factors most strongly influence passenger satisfaction and dissatisfaction, and how these factors vary across different passenger segments such as travel class, customer type, and purpose of travel. Without clear insights, decision-makers struggle to prioritize service improvements and allocate resources effectively.

Using Power BI dashboards, this project transforms raw survey data into meaningful visual insights that support data-driven decision-making. The analysis enables stakeholders to monitor performance across service categories, identify pain points in the passenger journey, and focus on high-impact improvement areas.

### Key Business Questions
- Which service and operational factors have the greatest impact on passenger satisfaction?
- How does satisfaction vary across different passenger segments and travel types?
- Where should airlines prioritize improvements to enhance customer experience?

### Target Audience (Stakeholders)

- Airline management and strategy teams
- Customer experience and service quality managers
- Business analysts and operational decision-makers

### Objectives of the Analysis
- Identify the key drivers of passenger satisfaction and dissatisfaction
- Compare performance across inflight, ground, and operational service categories
- Highlight improvement areas using clear, visual insights
- Enable data-driven decisions through interactive Power BI dashboards

## Data Cleaning and Transformation

### Power Query
The dataset was first imported into Power BI using Power Query, where initial data preparation and transformation steps were performed to ensure data quality and usability for analysis.

Column health indicators were reviewed to check for missing values, data type issues, and inconsistencies across all fields. This step helped identify columns requiring attention before building visualizations.

<img 
  src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Column%20Health.png?raw=true" 
  width="80%"
/>

To simplify analysis and improve readability, **conditional columns were created** to group and categorize values meaningfully, such as converting raw numerical or categorical inputs into more interpretable labels where required.

<img 
  src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Conditional.png" 
  width="50%"
/>

The Unpivot feature (Transform tab) was used to restructure multiple service-related rating columns into a standardized, long-format table. This transformation made it easier to compare satisfaction scores across different service categories within the dashboard.

Additionally, custom tables were created to organize data logically and support smoother analysis, allowing clearer segmentation and more flexible reporting within Power BI.

<img 
  src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Unpivot.png" 
  width="50%"
/>

### Data Modeling
A star schema–based data model was implemented in Power BI to support efficient analysis and flexible filtering across visuals. The DataSet table serves as the central fact table, containing passenger demographics, travel details, service ratings, and satisfaction information.

Supporting dimension tables such as Age_Bins and Satisfaction_Scale were created to simplify segmentation and enhance interpretability. An additional unpivoted service table enables easy comparison across different service categories.

<img 
  src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Star.png" 
  width="50%"
/>

Tables are connected using one-to-many relationships with bi-directional filtering, allowing interactions to flow seamlessly across visuals. This model design supports accurate insights, interactive reporting, and scalable dashboard development.

<img 
src = "https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Relationship.png" 
width="50%" 
/>

## Dashboard Design, Insights & Business Impact


The dashboard reveals that overall passenger satisfaction is **moderate**, with a large proportion of passengers falling into neutral or just-satisfied categories. This indicates a strong opportunity to improve service quality and convert neutral experiences into positive ones. 

The dashboard enables stakeholders to monitor overall performance, explore passenger segments, and identify key service improvement areas.

The layout follows a **top-down storytelling approach**, supported by a consistent color palette to improve readability and guide user attention toward key insights.

<img 
src = "https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Dashboard.png" 
width="80%" 
/>

### Key Insights and Business Impact

- The **average passenger satisfaction score is 3.0**, indicating moderate satisfaction with significant scope for improvement.
- **Neutral (63,244 passengers)** and **Satisfied (45,995 passengers)** form the largest groups, while **Very Satisfied passengers account for only 3,485**, highlighting an opportunity to elevate customer experience.
-  **Business travelers represent ~69%** of total passengers, making them the most influential segment for satisfaction improvements.
- **Inflight service and baggage handling are the strongest performers (avg. rating: 4.0)**, while the remaining service categories underperform, signaling clear opportunities for service enhancement.

### Actionable Recommendations
- Prioritize improvement for dissatisfied passengers, who currently represent 12.22% (very dissatisfied) and 16.97% (dissatisfied) of the total passenger base. Targeting these groups presents the greatest opportunity to improve overall satisfaction levels.
- By addressing key service gaps for dissatisfied passengers, there is strong potential to move customers from dissatisfied to neutral, and subsequently convert neutral passengers into satisfied customers, creating a positive shift across satisfaction categories.
- Focus immediate improvement efforts on controllable service areas such as online booking, gate location, and inflight Wi-Fi, as these services consistently receive high dissatisfaction scores and can be improved more quickly compared to operational factors.
- Enhancing these high-impact services is likely to reduce dissatisfaction levels in the short term and contribute to a measurable increase in neutral and satisfied passenger ratings.
- Use the Power BI dashboard to continuously monitor changes in satisfaction distribution and assess the effectiveness of service improvements over time.

## Limitations & Assumptions
This analysis is subject to the following assumptions and limitations, which should be considered when interpreting the results:

### Assumptions
#### a.  Flight Type Classification:
Flight distance was categorized to simplify analysis and comparison:

-   **Long Flight:** Distance ≥ 3,700
    
-   **Medium Flight:** Distance ≥ 1,500 and < 3,700
    
-   **Short Flight:** Distance < 1,500  
    
This categorization is assumed to reasonably represent short-, medium-, and long-haul travel patterns.

#### b. Rounding of Average Satisfaction Scores:
Minor discrepancies were observed between the grand total average (e.g., 3.28) and KPI card average (e.g., 3.26) due to aggregation behavior in Power BI visuals. To maintain consistency across the report, average satisfaction scores were rounded to whole numbers, ensuring uniform interpretation throughout the dashboard.

#### c. Service Category Grouping:
Individual service attributes were grouped into broader categories to improve interpretability and storytelling:

- Before-Boarding Services: Ease of Online Booking, Check-in Service, Online Boarding, Gate Location

- Flight Services: On-board Service, Seat Comfort, Leg Room Service, Cleanliness, Food and Drink

- Essential Services: In-flight Service, In-flight Wi-Fi Service, In-flight Entertainment, Baggage Handling

These groupings assume that services within each category represent similar stages of the passenger journey.

### Limitation
-   **Data Scope:**   The analysis is limited to the variables available in the dataset and does not include external factors such as ticket pricing, airline brand, route characteristics, or seasonal effects.
    
-   **Sampling Bias:** The dataset is survey-based and may reflect **response bias**, as passengers with strong positive or negative experiences are more likely to provide feedback.
    
-   **Analytical Scope:**   The dashboard focuses on **descriptive and diagnostic insights** and does not establish causal relationships between service factors and satisfaction.
    

Despite these limitations, the dashboard provides meaningful insights into passenger satisfaction patterns and supports informed, data-driven decision-making.

## Future Improvements
To further enhance the value of this analysis, the following improvements can be considered:

-   **Time-Series Analysis:** Incorporate flight date or time-based data to track satisfaction trends and seasonal patterns.
    
-   **Automated Data Refresh:** Enable scheduled data refresh to ensure insights remain up to date.
    

    
-   **Enhanced Drill-Downs:** Add deeper drill-down functionality by route, airport, or service category for more granular analysis.
    
-   **External Data Integration:** Include additional data such as ticket pricing, airline brand, or route information for richer insights.

## Conclusion
This project demonstrates how Power BI can be used to transform raw passenger survey data into meaningful business insights. By combining thoughtful data modeling, intuitive dashboard design, and clear storytelling, the analysis highlights key drivers of passenger satisfaction and identifies actionable improvement areas.

The dashboard enables stakeholders to move beyond static reports, supporting informed decision-making and continuous service improvement. Overall, this project showcases a strong foundation in business intelligence, data visualization, and analytical thinking.
