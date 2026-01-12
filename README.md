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

<p align="center">
  <img src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Star.png" width="45%" />
  <img src="https://github.com/krutik-dhabaliya/Airline-Passenger-Satisfaction-Analysis-using-Power-BI/blob/main/Images/Relationship.png" width="45%" />
</p>
