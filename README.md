# MTA Subway System Improvement Project

## Overview
This project utilizes data from the MTA subway system to address key challenges in public transportation for New Yorkers. By leveraging big data, the project identifies opportunities to enhance express service lines, prioritize ADA accessibility upgrades, and improve train line performance.

---

## Objectives
1. **Identify Stations for New Express Lines**
   - Determine high-volume stations that would benefit from express services.
2. **Prioritize ADA Accessibility Upgrades**
   - Focus on stations with high senior and disabled ridership for equitable infrastructure enhancements.
3. **Evaluate Train Line Performance**
   - Analyze delays and performance metrics to recommend improvements for underperforming lines.

---

## Data Sources
1. **Primary Data**: 
   - MTA Subway Hourly Ridership data (54M rows/month, ~3.36 GB).
2. **Supplementary Data**:
   - On-time performance metrics.
   - Incident reports for delay causes.
   - ADA compliance data.

Data was extracted programmatically using APIs via Socrata, ensuring real-time updates and integration into the ETL pipeline.

---

## Technologies
- **MongoDB**: Scalable database for large ridership datasets.
- **Neo4j**: Relationship modeling for incident and performance data.
- **Flask**: Interactive dashboard for user exploration of results.
- **Socrata**: API for data extraction and integration.

---

## Project Workflow
1. **Data Extraction**:
   - Retrieved data using Socrata API.
   - Combined ridership, incidents, and performance datasets.
2. **Data Processing**:
   - Cleaned and transformed datasets.
   - Merged data based on time, line, and station ID.
3. **Analysis**:
   - Analyzed ridership for express line opportunities.
   - Identified stations needing ADA upgrades.
   - Evaluated train line delays and performance.
4. **Visualization**:
   - Created dashboards for results using Flask.

---

## Key Findings
1. **Express Line Recommendations**:
   - High-priority stations include:
     - 1 Line (Manhattan), F Line (Brooklyn), N Line (Brooklyn).
2. **ADA Accessibility Prioritization**:
   - Key stations: 14th St/6 Av, Canal St.
   - Focus on Brooklyn and Manhattan for upgrades.
3. **Train Line Performance**:
   - A Line: Worst weekday performance.
   - F Line: Worst weekend performance.
   - Recommendations include additional security and maintenance for these lines.

---

## Scalability and Cost Considerations
1. **Data Growth**:
   - Current: 3.36 GB/month.
   - Projected growth: Linear with increasing ridership and more granular data.
2. **Performance Challenges**:
   - MongoDB utilizes 7/12 GB RAM; risk of bottlenecks as data grows.
3. **Scaling Solutions**:
   - Vertical scaling: Upgrade RAM to 24 GB ($600–$800).
   - Horizontal scaling: Add servers ($2,000–$4,000 per server).

---

## Recommendations for Future Work
1. Incorporate real-time data for dynamic insights.
2. Utilize weight-sensing data for enhanced demand predictions.
3. Expand analysis to include additional datasets for broader conclusions.

---

## License
This project is licensed under the MIT License. For more details, refer to the LICENSE file.

---

## Acknowledgments
Data provided by [data.ny.gov](https://data.ny.gov). Special thanks to the MTA for making public datasets available for research and analysis.

