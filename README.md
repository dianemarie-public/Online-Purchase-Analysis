# Pandas

**Background**

Project story.

**Project Scope**

Describe the datasets, project plan and tasks.

- Using Jupyter Notebooks, import dependencies and read data file into pandas:

   ```
   import pandas as pd
   file_to_load = "Resources/purchase_data.csv"
   purchase_data = pd.read_csv(file_to_load)
   ```
**Analysis**

<!-- Project statistics.

|Table|Col1|Col2|
|----|----|----|
|1|2|3|4|

**Findings** -->

Project insights from data and process.
- Player Count
   ```
   player_count = purchase_data["SN"].value_counts()
   player_count = player_count.count()
   ```
   ![count](Images/player_count.png)

- Purchasing Analysis
   ```
   item_count = purchase_data["Item ID"].value_counts()
   item_count = item_count.count()
   avg_price = purchase_data["Price"].mean()
   total_revenue = purchase_data["Price"].sum()
   ```
   ![pandas](Images/purchasing_analysis.png)

- Gender Analysis
   ```
   gender_group = purchase_data.groupby("Gender")
   gender_count = gender_group.nunique()["SN"]
   pct_players = gender_count/gender_count.sum()
   purchase_count = gender_group["Purchase ID"].count()
   avg_price = gender_group["Price"].mean()
   total_revenue = gender_group["Price"].sum()
   avg_player_purchase = total_revenue/gender_count
   ```
   ![pandas](Images/gender_analysis.png)

- Age Analysis
   ```
   min_age = purchase_data["Age"].min()
   max_age = purchase_data["Age"].max()
   age_bins = [min_age-1,9,14,19,24,29,34,39,max_age]
   age_bin_labels = [" 0 < 10","10 - 14", "15 - 19","20 - 24","25 - 29",
      "30 - 34","35 - 39","40 +"]
   pd.cut(purchase_data["Age"], age_bins, labels=age_bin_labels).head()
   purchase_data["Age Group"] = pd.cut(purchase_data["Age"], age_bins, labels=age_bin_labels)
   age_group = purchase_data.groupby("Age Group")
   age_count = age_group.nunique()["SN"]
   pct_players = age_count/player_count
   ```
   ![pandas](Images/age_analysis.png)

- Demographics
   ```

   ```
   ![pandas](Images/demographics.png)


- Most Popular
   ```

   ```
   ![pandas](Images/most_popular.png)

- Most Profitable
   ```
   items_df = items_df.sort_values("Purchase (total)", ascending=False)
   top_5 = items_df.head(5)
   ```
   ![pandas](Images/most_profitable.png)

**Conclusion**

Futher action, data exploration and limitations.