🛒 DS501 - Association Rules Analysis on Grocery Transactions
Author: Mina Fahmy
📘 Overview

This project applies Association Rule Mining to a grocery store transactional dataset using the Apriori algorithm. The goal is to uncover patterns in customer purchases, identify items frequently bought together, and derive actionable insights that can inform store promotions or layout optimization.

The dataset contains 9,835 transactions across 169 items (product types). Common patterns like milk and bread or wine and cheese are explored to confirm or discover new associations.

🎯 Objective

Discover frequent itemsets in grocery transactions.

Identify strong association rules with meaningful support, confidence, and lift.

Visualize patterns to better understand relationships among products.

Demonstrate practical applications of unsupervised learning for retail analytics.

📊 Dataset Description

Source: Built-in Groceries dataset from the arules R package.

Transactions: 9,835 individual purchases

Items: 169 product types

Characteristics:

Average transaction size: 4.4 items

25% of transactions contain ≤ 2 items

Most frequent item: Whole Milk

⚙️ Methods & Implementation
1. Data Exploration

Inspect transaction density and item frequency.

Visualize transaction patterns using matrix plots and item frequency plots.

2. Apriori Algorithm

Implemented using arules::apriori() in R.

Parameters:

support threshold: 0.009 (minimum frequency of occurrence)

confidence threshold: 0.25 (minimum reliability of rule)

minlen = 2 (ignore rules with fewer than 2 items)

3. Evaluating Rules

Summary statistics for the set of rules.

Sorted by lift to identify the strongest associations.

Subsets of interest (e.g., rules containing beef or sausage).

4. Visualization

Scatter plots: support vs lift, colored by confidence.

Matrix and grouped matrix visualizations for comparing multiple rules.

Graph and parallel coordinates plots for interactive exploration.

📈 Key Insights

High-lift rules indicate strong purchasing relationships (e.g., customers buying berries often purchase whipped/sour cream).

Market basket analysis helps identify actionable, trivial, and inexplicable rules for targeted marketing.

Visualization helps filter and interpret large rule sets efficiently.

💻 Requirements

Language: R

Packages:

arules, arulesViz, colorspace, plotly


Optional installation for interactive plots:

install.packages("arules")
install.packages("arulesViz")
install.packages("colorspace")
install.packages("plotly")

▶️ How to Run

Clone the repository:

git clone https://github.com/<your-username>/DS501-Association-Rules.git
cd DS501-Association-Rules


Open the R Markdown file DS501_Association_Rules.Rmd in RStudio.

Run all code chunks sequentially to:

Explore transactions

Generate association rules

Visualize patterns

Export rules to CSV if needed

Optional: Explore interactive plots using plotly or htmlwidget outputs.

📂 Saving Rules

Association rules can be saved to a CSV file for further analysis or reporting:

write(grules, file = "grules.csv", sep = ",", quote = TRUE, row.names = FALSE)

🧠 Summary

Association rules provide an unsupervised learning approach to uncover patterns without prior knowledge.

Apriori algorithm efficiently identifies frequent itemsets and associations.

Visualization and filtering are essential for understanding large sets of rules.

The project highlights actionable insights that can drive retail decision-making.

📚 References

R Core Team (2024). R: A Language and Environment for Statistical Computing.

Hahsler, M., Chelluboina, S., & Buchta, C. (2024). arules: Mining Association Rules and Frequent Itemsets.

Groceries Dataset, arules package.
