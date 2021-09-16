# Pandas

**Background**

Analyzing (fictional) online game purchase data.

**Project Scope**
- In a new Jupyter notebook, loading data into pandas from a .csv file.
   ```
   import pandas as pd
   file_to_load = "Resources/purchase_data.csv"
   purchase_data = pd.read_csv(file_to_load)
   ```
- Creating pandas dataframes to clean, filter and summarize the data.
- Analyzing purchase data using player metadata to identify trends.

**Analysis**
- Total player count.
   
   ![count](Images/player_count.png)
- Purchase count, average price and total sales amount. 

   ![pandas](Images/purchasing_analysis.png)
- Breakdown of purchases by gender. 
   
   ![pandas](Images/gender_analysis.png)
- Age group 20-24 has the most purchases by both purchase count and amount. 
   
   ![pandas](Images/age_analysis.png)

**Summary and Insights**
- *570 total players.*
 
- *780 total purchases, across 179 games, averaging $3.05 and $2,380 in total sales.*
 
- *Males have the most purchases and total sales amount, but the lowest average purchase at $3.02.*

- *Age group 20-24 has the most purchases by both purchase count and amount while age group 35-39 has highest average purchase of $4.76.*

- *The most purchased game is Final Critic:*

   ![Top 5 Games Purchased](Images/most_popular.png)

<!-- **Conclusion**

Futher action, data exploration and limitations. -->