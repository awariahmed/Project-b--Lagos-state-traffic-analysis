# project-b--Lagos-state-traffic-analysis
LAGOS STATE TRAFFIC ANALYSIS & MOBILITY INTELLIGENCE
Capstone Project Report 
1. Executive Summary
Lagos State, the commercial nerve center of Nigeria, faces immense urban mobility challenges characterized by high population growth density, motorization rates, and infrastructure constraints. This capstone project establishes an exhaustive data-driven traffic analysis framework and executive dashboard model to evaluate arterial corridor performance, quantify commuter delay minutes, and isolate environmental and incident-based congestion drivers. By analyzing 1,500 telemetry and observational records spanning major Lagos transit arteries (such as the Lekki-Epe Expressway, Third Mainland Bridge, Ikorodu Road, and Apapa-Oshodi Expressway), this project delivers actionable intelligence for urban planners, transportation agencies, and supervisory stakeholders.

2. Dataset Architecture & Variable Specifications
The underlying project dataset (Lagos_Traffic_Executive_Dashboard.xlsx) is structured across three core sheets (Executive Dashboard, Traffic Data, and Lookup & Calculations) containing 1,500 granular records across thirteen operational attributes:

Transactional Identifiers: Record ID (unique keys e.g., TRF-1000), Date, Time, and operating Hour (0–23).

Temporal & Spatial Categorization: Day Type classification (Weekday vs. Weekend), major Lagos Corridor, and specific bottleneck Junction / Area (e.g., Ojota Interchange, Ajah Junction, CMS, Mile 2).

Environmental & Incident Parameters: Categorical tracking of Weather conditions (Clear, Light Rain, Heavy Rain, Overcast, Flooded) and roadway Incident Reported (None, Accident, Vehicle Breakdown, Fallen Truck, Road Maintenance).

Quantitative Performance Metrics: Avg Speed (km/h), Speed Limit (km/h), computed Delay (mins), estimated Vehicle Count, and automated Congestion Level (Free Flow, Moderate, Heavy, Severe).

3. Key Analytical Findings & Operational Insights
Multi-dimensional aggregation of the dataset reveals critical behavioral patterns across Lagos transport corridors:

Corridor Speed Bottlenecks: High-density commercial corridors like Agege Motor Road, Funsho Williams Avenue, and Ikorodu Road record the lowest average speeds (21–25 km/h) due to mixed commercial land use and roadside friction. In contrast, multi-lane expressways maintain higher free-flow averages (37–38 km/h) during off-peak windows.

Congestion Severity Distribution: Heavy and Severe congestion account for over 50% of all observed intervals across Lagos State, while free-flow conditions are strictly confined to late-night hours and early weekend mornings.

Weather & Incident Impact Multipliers: Heavy rainfall and urban flooding double average travel delays compared to clear weather. Sudden roadway obstructions (such as fallen trucks on critical bridge links) trigger cascading gridlock across connecting mainland-island arteries.

Rush-Hour Dynamics: Weekdays display sharp bimodal peaks during morning commuter rushes (7:00 AM – 9:00 AM) and evening departures (5:00 PM – 8:00 PM), where delays exceed 30 minutes, whereas weekend traffic shows a flatter afternoon-skewed distribution.

4. Dashboard Implementation Blueprint (Excel & Power BI)
To facilitate seamless supervisory review, the dashboard has been built in Excel with live formulas and structured for Power BI Desktop (.pbix) export:

Core Excel Formulas & KPIs (Executive Dashboard)
Total Records Monitored: =COUNTA('Traffic Data'!A2:A1501)

Average Speed (km/h): =AVERAGE('Traffic Data'!J2:J1501)

Average Delay (Mins): =AVERAGE('Traffic Data'!L2:L1501)

Total Traffic Volume: =SUM('Traffic Data'!M2:M1501)

Power BI DAX Measures (Optional Supervisor Submission)
Code snippet
Total Volume = SUM('Traffic Data'[Vehicle Count])
Code snippet
Avg Speed = AVERAGE('Traffic Data'[Avg Speed (km/h)])
Code snippet
Avg Delay = AVERAGE('Traffic Data'[Delay (mins)])
Code snippet
Severe Congestion % = DIVIDE(CALCULATE(COUNTROWS('Traffic Data'), 'Traffic Data'[Congestion Level] = "Severe"), COUNTROWS('Traffic Data'), 0)
Visual Layout Architecture
Header Banner: Deep Navy (#1F4E78) background with prominent title and executive subtitle blocks.

KPI Card Row: Four summary cards highlighting Total Records, Average Speed, Average Delay, and Total Volume.

Corridor Bar Chart: Clustered horizontal bar chart ranking corridors from slowest to fastest to isolate key bottleneck arteries.

Congestion Donut/Pie Chart: Percentage breakdown illustrating the ratio of Free Flow versus Moderate, Heavy, and Severe gridlock states.

5. Strategic Policy Recommendations
Based on the empirical findings from the Lagos traffic dataset, the following recommendations are submitted for supervisory endorsement:

Rapid Incident Clearance Protocol: Deploy dedicated emergency towing units and rapid response squads along critical bottlenecks (such as the Third Mainland Bridge and Apapa Expressway) to mitigate incident-induced delay multipliers.

Weather-Responsive Traffic Advisories: Implement automated variable messaging systems and flood-warning rerouting protocols along vulnerable low-lying corridors during heavy downpours.

Commercial Transport Rationalization: Enforce strict loading bay regulations and terminal management along high-friction corridors like Agege Motor Road and Ikorodu Road to preserve lane capacity.
