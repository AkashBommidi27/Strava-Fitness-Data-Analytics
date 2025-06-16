Strava Fitness Data Analytics
Overview
This project analyzes fitness tracker data from Strava to uncover user behavior patterns in activity, sleep, and heart rate, serving as a proxy for Bellabeat's wellness devices. The goal is to provide actionable insights to enhance Bellabeat's marketing strategy, improve user engagement, and support data-driven product decisions. The analysis leverages SQL for data merging, Python for data processing and clustering, and Tableau for visualization.
Project Structure

Data Source: Strava fitness tracker datasets (daily, hourly, minute-level activity, sleep, and heart rate data)
Tools Used:
SQL: For merging datasets (daily, hourly, and minute-level data)
Python: For data cleaning, clustering (PCA and K-Means), and analysis (using pandas, seaborn, matplotlib, and scikit-learn)
Tableau: For creating interactive dashboards to visualize trends and insights


Notebook: Strava_Project_submission.ipynb contains the full analysis workflow
Visualizations: Tableau dashboards are included as images in the repository
Datasets: Stored in ./datasets/Data Files (downloaded from Google Drive)

Key Insights
1. Activity Trends

Daily Activity Patterns (Tableau Dashboard: Daily Insights)

Average distance traveled per day: 5.49 miles
Total steps over the period: 7,179,636 steps
Average calories burned: 2,304 calories per day
Activity peaks around mid-April, with a noticeable decline by early May (seen in the "Distribution of Total Steps" and "Distribution of Calories" charts).
Users spend the majority of their time in a sedentary state (931,738 minutes), with limited very active (19,885 minutes) and fairly active (12,751 minutes) time, indicating potential for increasing engagement in higher-intensity activities.


Hourly Activity Patterns (Tableau Dashboard: Hourly Data Dashboard)

Average steps per hour: 320.2 steps
Average calories burned per hour: 97.39 calories
Average intensity per hour: 12.04
Steps and calorie burn peak between 10 AM and 2 PM, suggesting users are most active during late morning to early afternoon.
Intensity levels are generally low, with most hours showing minimal activity (seen in the "Avg Intensity per Hour" histogram), indicating opportunities for encouraging more consistent activity throughout the day.



2. Sleep Patterns

Sleep Efficiency (Tableau Dashboard: Sleep Data Dashboard)
Users spend more time in bed than asleep, with an average difference of 40-60 minutes (seen in the "Time in Bed vs Time Asleep" scatter plot).
Average sleep per weekday is highest on Sunday (450 minutes) and lowest on Wednesday (400 minutes), suggesting potential sleep disruptions midweek.
The number of sleep records per night averages around 1, with slight increases on weekends (seen in the "Avg Sleep Records per Weekday" chart), indicating more fragmented sleep during the week.



3. Heart Rate Analysis

Heart Rate Variability (Tableau Dashboard: Heartbeat of User)
Heart rate (BPM) varies widely across users, ranging from 50 to 90 BPM on average.
Some users (e.g., Id: 2026352035) show consistently higher heart rates (90 BPM), potentially indicating higher stress or fitness levels, while others (e.g., Id: 8792009665) stay lower (70 BPM).
This variability suggests opportunities for personalized health insights, such as stress management or fitness tracking features.



4. User Segmentation

Clustering Results (Python Analysis)
Using PCA and K-Means clustering, users were segmented into two groups:
Segment 0 (Active Users): High total steps, calories burned, and very/fairly active minutes. These users are engaged in regular, intense physical activity.
Segment 1 (Less Active/Sedentary Users): Lower steps and calories burned, with more lightly active and sedentary minutes. These users may benefit from motivational features to increase activity.


This segmentation allows Bellabeat to tailor marketing strategies, such as targeting active users with performance tracking features and sedentary users with activity prompts.



5. Calorie Burn vs. Intensity

Correlation Analysis (Tableau Dashboard: Hourly Data Dashboard)
A strong positive correlation exists between total steps and calories burned (seen in the "Calories vs Total Steps" scatter plot), with higher step counts linked to greater calorie expenditure.
Very active minutes contribute significantly to calorie burn (seen in the "Very Active Minutes vs Calories Burnt" scatter plot), suggesting that encouraging high-intensity activity can boost overall energy expenditure.
Average intensity and calorie burn also show a positive relationship (seen in the "Calories vs Avg Intensity" scatter plot), reinforcing the importance of intensity in fitness goals.



Methodology

Data Loading:

Datasets were downloaded from Google Drive and extracted into ./datasets.
Five core datasets were created: daily_df, hourly_df, minute_df, heartbeat_df, and sleepday_df.


SQL:

Merged daily datasets (dailyActivity, dailyCalories, dailyIntensities, dailySteps) into daily_df.
Merged hourly datasets (hourlyCalories, hourlyIntensities, hourlySteps) into hourly_df.
Merged minute-level datasets (minuteCalories, minuteIntensities, minuteSteps, minuteMETs) into minute_df.


Python:

Performed data cleaning and preprocessing (e.g., handling timestamps, removing duplicates).
Conducted PCA and K-Means clustering to segment users into active and sedentary groups.
Generated summary statistics and correlations (e.g., steps vs. calories, intensity vs. calorie burn).


Tableau:

Created three dashboards:
Daily Insights: Visualizes total steps, distance, and calorie burn trends over time.
Hourly Data Dashboard: Displays hourly steps, intensity, and calorie burn patterns.
Sleep Data Dashboard: Shows sleep duration, time in bed, and sleep records by weekday.
Heartbeat of User: Highlights heart rate variability across users.





Recommendations for Bellabeat

Increase Activity Engagement:

Target sedentary users (Segment 1) with reminders to increase very active minutes, especially during low-activity periods (e.g., early morning or evening).
Promote high-intensity activities to boost calorie burn, as seen in the correlation between intensity and calories.


Improve Sleep Quality:

Offer features to help users reduce the gap between time in bed and time asleep (e.g., bedtime routines, relaxation prompts).
Address midweek sleep disruptions by suggesting consistent sleep schedules.


Personalized Health Insights:

Use heart rate variability to provide tailored recommendations, such as stress management for users with higher BPM or fitness challenges for those with lower BPM.
Leverage user segmentation to customize features (e.g., performance tracking for active users, step goals for sedentary users).


Marketing Strategy:

Highlight the benefits of high-intensity activity in campaigns, as it significantly impacts calorie burn.
Focus on weekend sleep improvements to appeal to users struggling with weekday sleep consistency.



How to Run

Clone the repository:git clone https://github.com/AkashBommidi27/Strava-Fitness-Data-Analytics.git


Install dependencies:pip install pandas seaborn matplotlib scikit-learn gdown


Open the Jupyter Notebook (Strava_Project_submission.ipynb) and run the cells to reproduce the analysis.
View the Tableau dashboards (images) in the repository for visualizations.

Dependencies

Python 3.x
Libraries: pandas, seaborn, matplotlib, scikit-learn, gdown, sqlite3
Tableau (for visualizations)

Data Source

Datasets are downloaded from a Google Drive link provided in the notebook: Google Drive Link

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or collaborations, reach out via GitHub: AkashBommidi27.
