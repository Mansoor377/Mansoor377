# Let's start by choosing a dataset and a theme for the infographics. 
# I will choose the theme of "Economic Development and Poverty" and use data from the World Bank.

import pandas as pd
import numpy as np
# Let's start by choosing a dataset and a theme for the infographics. 
# I will choose the theme of "Economic Development and Poverty" and use data from the World Bank.

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Loading a dataset from the World Bank related to economic development and poverty
# For demonstration, I will use a sample dataset. In a real-world scenario, you would download the actual dataset from the World Bank's website.

# Sample data structure
data = {
    "Country": ["Country A", "Country B", "Country C", "Country D"],
    "GDP (in billion USD)": [500, 800, 300, 700],
    "Population (in millions)": [50, 70, 30, 60],
    "Poverty Rate (%)": [10, 20, 30, 15],
    "Literacy Rate (%)": [98, 89, 75, 90]
}

df = pd.DataFrame(data)

# Displaying the dataframe
df


# Now, I will create 4 different plots that collectively tell a story about economic development and poverty.

# 1. GDP vs Poverty Rate
plt.figure(figsize=(10, 6))
sns.barplot(x="GDP (in billion USD)", y="Poverty Rate (%)", data=df)
plt.title("GDP vs Poverty Rate")
plt.xlabel("Gross Domestic Product (in billion USD)")
plt.ylabel("Poverty Rate (%)")
plt.grid(True)
plt.savefig("/mnt/data/gdp_vs_poverty_rate.png")
plt.show()

# 2. Population vs Literacy Rate
plt.figure(figsize=(10, 6))
sns.barplot(x="Population (in millions)", y="Literacy Rate (%)", data=df)
plt.title("Population vs Literacy Rate")
plt.xlabel("Population (in millions)")
plt.ylabel("Literacy Rate (%)")
plt.grid(True)
plt.savefig("/mnt/data/population_vs_literacy_rate.png")
plt.show()

# 3. GDP per Capita
df["GDP per Capita (USD)"] = df["GDP (in billion USD)"] * 1e9 / (df["Population (in millions)"] * 1e6)
plt.figure(figsize=(10, 6))
sns.barplot(x="Country", y="GDP per Capita (USD)", data=df)
plt.title("GDP per Capita")
plt.xlabel("Country")
plt.ylabel("GDP per Capita (USD)")
plt.grid(True)
plt.savefig("/mnt/data/gdp_per_capita.png")
plt.show()

# 4. Literacy Rate vs Poverty Rate
plt.figure(figsize=(10, 6))
sns.scatterplot(x="Literacy Rate (%)", y="Poverty Rate (%)", data=df)
plt.title("Literacy Rate vs Poverty Rate")
plt.xlabel("Literacy Rate (%)")
plt.ylabel("Poverty Rate (%)")
plt.grid(True)
plt.savefig("/mnt/data/literacy_vs_poverty_rate.png")
plt.show()

# These plots provide insights into the relationship between economic factors (GDP, GDP per capita) and social indicators (poverty rate, literacy rate).


<!---
Mansoor377/Mansoor377 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
