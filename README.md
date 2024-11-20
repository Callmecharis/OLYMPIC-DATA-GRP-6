## OLYMPIC-DATA-GRP-6
## INTRODUCTION/OVERVIEW
Introduction/Overview:

For this project, we are doing exploratory data analysis on Olympics  Games data. Our objective was to develop a comprehensive and interactive Power BI report that showcases insights into key aspects of the Olympics. This project serves as a demonstration of our data analysis skills, from data import and transformation to data modeling and visualization.

 *Key insights include:* 
 
We analyze the performance of men versus women in the Olympic Games. By categorizing medal count and gender, we can discern how some countries may have higher performing athletes from men or women.

Count of Medal By Gender 

Total number of medals won by countries.

Distribution of athletes by gender and sports.

Country-wise Medal Count

Top 10 Countries by Medals

2. *Data Import* 

Title: Data Import Process

To begin the analysis, we imported two(2) CSV files format that captured different aspects of the Olympics. Each dataset provided a unique view of the event, such as athlete names, countries, gender, disciplines, sports, events and the number of medals won. The primary datasets we used included:

Summer & Winter csv: Contains information about athletes, including their country and discipline, the total count of gold, silver, and bronze medals won by countries. And also, shows the gender distribution of participants in each discipline.

Power BI’s 'Get Data' feature made the import process seamless, supporting various file formats. We used CSV files, which were easily integrated into Power BI. During this step, we ensured that all datasets were formatted consistently, and we took note of any potential issues like missing values or incorrect data types.

 *Challenges faced:* 

One of the datasets had inconsistent data formats, such as commas in the name field or text fields where numeric values were expected. These issues were resolved during the data transformation phase and ......(Mazi Ben to supply how he was able to clean the data)

3. Data Transformations (Power Query)

Title: Data Transformations in Power Query

Data cleaning and transformation are critical steps in preparing raw data for analysis. In Power BI, we used Power Query to apply various transformations, ensuring that the data was consistent, accurate, and ready for analysis.
Key transformations we applied included:

Replacing Values:  we replaced missing or inconsistent values using Power Query’s Replace Values feature, especially in cases where country names or abbreviations were inconsistent across datasets.

Data Type Corrections: Ensured that numeric fields (e.g., number of medals or athletes) were set to the correct data types, avoiding text or mixed data formats.

Calculated Columns: We added calculated columns for total medal to ensure these values could be easily referenced during the data modeling phase.

This transformation phase ensured that the data was clean and cohesive, making the modeling and visualization processes more efficient.

4. Data Modeling

Title: Data Modeling Approach

With the data imported and transformed, we proceeded to build a star schema data model, a highly efficient structure for analytics. The star schema allowed for quick and easy filtering of large datasets, ensuring fast performance during visualization.
The star schema involved:

Fact Tables: These tables contained the core data of interest, such as the Medals, Athletes, and Countries tables, which included transactional data (e.g., medal counts and athlete details).

This model provided the foundation for interactive and high-performance visualizations.

￼

Data Modeling

5. Creating Measures

Title: Crafting DAX Measures for Deeper Insights

Once the model was established, we used DAX (Data Analysis Expressions) to create dynamic measures for key insights. These measures allowed us to perform complex calculations on the fly, enabling the dashboard to display dynamic and context-sensitive metrics based on the user’s interactions.
Key measures created:

i. Total Sports:

Total Sports = SUM(Sports[Total])

--This measure calculated the total number of medals won by each 
country across all disciplines.

ii. Total Athletes:
Total Athletes = COUNTROWS(Athletes)

--This measure counted the total number of athletes across all countries 
and disciplines.

iii. Rank by Medals:

Rank by Medals = RANKX(ALL(Medals[Country]), [Total Medals], ,DESC )

--This measure ranked countries by the total number of medals won, 
enabling users to see how countries compared in terms of Olympic performance.

6. *Data Visualization* 

Title: Creating Interactive Dashboards with Power BI

We focused on creating highly interactive and visually engaging dashboards using a variety of Power BI features, including buttons, slicers, and custom visuals. The goal was to provide users with an intuitive experience where they could explore the data and uncover insights on their own.
Visuals used:

Card Visuals: Displayed key metrics such as Total Medals, Total Athletes, and Total Countries.

Bar and Column Charts: Used to show the distribution of medals by country, athlete participation by sports, and the number of countries participating in each event.

Slicers: Added for filtering by Country, Events, and Gender to allow users to focus on specific aspects of the data.

Buttons for Page Navigation: We created custom buttons for smooth navigation between different report pages, including Summary, Medals Overview, Athletes Performance, and Countries.

Pie Charts and Maps: Used to display the Medal Distribution across countries and global participation in the Olympics.

Example screenshot:

￼

￼

7. Conclusion

This project showcases the end-to-end process of working with Power BI, from data import and transformation to building advanced data models and creating interactive dashboards. The result is a comprehensive report that provides valuable insights into the Olympics, making it easy to explore medal distributions, athlete participation, and country rankings.
Working on this project allowed us to deepen our expertise in Power BI, particularly in crafting efficient data models, writing dynamic DAX measures, and creating user-friendly visualizations. We look forward to applying these skills in real-world business environments to deliver actionable insights.
“Explore the full interactive report here: Power BI Olympic Report”.
