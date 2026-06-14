# Case Study: E-Commerce Markdown Optimisation & Sentiment Analysis
Project Type: Commercial Revenue & Customer Sentiment Analytics

Tools Used: Microsoft Excel (Power Query, Advanced Formulas, Pivot Tables, Interactive Dashboard)

Dataset: 1,400+ Amazon Product Sales Records

1. Executive Summary
In competitive e-commerce environments, promotional discounting is a double-edged strategy. While aggressive markdowns can accelerate sales velocity and clear slow-moving inventory, they carry the risk of eroding profit margins and weakening brand perception.
This project serves as an optimisation diagnostic for a retail portfolio selling on Amazon. The objective was to identify the promotional sweet spot — the discount bracket that maximises gross revenue without compromising customer satisfaction or cannibalising product margins.

2. Analytical Objectives
The analysis was structured around three core business questions:

Margin Impact: Which discount brackets generate the highest absolute cash revenue relative to lost inventory value?
Customer Perception: Does deep discounting negatively affect how customers perceive product quality?
Category Dependency: Which product categories are most reliant on heavy promotional markdowns to drive sales?


3. Data Preparation & Processing
Phase A — Data Cleaning (Power Query)
The raw dataset required significant structural cleaning before analysis could begin. Using Power Query, the following transformations were applied:

Category Parsing: The raw category field contained multi-tiered, pipe-delimited strings. A delimiter split was applied to isolate the top-level parent category into a clean Main_Category column.
Data Type Correction: Currency symbols and percentage signs were stripped from financial columns, and affected fields were recast from text to numerical data types to enable accurate aggregation.

Phase B — Business Logic & Classification
To support category-level analysis, a custom discount classification column was engineered using a nested IFS formula that segmented all products into four brackets: No Discount, Low (1–20%), Medium (21–50%), and Heavy (51%+). This enabled consistent grouping across all subsequent analysis.

4. Key Findings
Finding 1: Deep Discounts Negatively Affect Customer Ratings
The data revealed an inverse relationship between discount depth and customer satisfaction. Products in the Low Discount bracket (1–20%) maintained an average rating of 4.17 out of 5.0, while products in the Heavy Discount bracket (51%+) averaged 4.06 out of 5.0.
While the difference appears marginal in absolute terms, it reflects a consistent pattern: deep discounting tends to attract more price-sensitive customers who apply greater scrutiny to product quality, resulting in lower review scores.
Finding 2: Heavy Discounting Significantly Erodes Revenue
The revenue analysis exposed a substantial gap between retail value and actual cash collected within the Heavy Discount tier. Products in this bracket carried a combined retail value of ₹2,442,594.32, yet generated only ₹827,785.19 in actual revenue — representing a loss of approximately ₹1.61 million in potential value.
By contrast, the Medium Discount tier (21–50%) proved significantly more efficient, generating a maximum of ₹3,068,171.24 while maintaining healthier margins. This positions the medium bracket as the most commercially viable promotional zone.
Finding 3: Electronics Categories Are Heavily Promotion-Dependent
Cross-referencing product categories against discount brackets revealed that Electronics (276 products) and Computers & Accessories (285 products) were disproportionately concentrated in the Heavy Discount tier, suggesting these categories rely heavily on promotional pricing to remain competitive on the platform.

5. Dashboard Design
To present findings in an accessible and actionable format, an interactive executive dashboard was developed in Excel incorporating the following design principles:

A clean, gridline-free layout to improve readability and visual clarity
A logical information flow, with the revenue margin gap chart positioned as the primary anchor, supported by customer sentiment trends and product volume distribution
An interactive slicer connected across all underlying pivot models, enabling dynamic filtering of the full dataset by product category


6. Strategic Recommendations
Based on the analysis, three actionable recommendations were identified for the business:

Introduce Markdown Caps: Implement a maximum discount ceiling of 50% on Electronics and Computers & Accessories to limit further margin erosion in these categories
Shift Focus to the Medium Discount Bracket: Redirect high-volume promotional inventory from the Heavy to the Medium tier (21–50%), where historical data indicates maximum revenue is generated at healthier margins
Monitor Quality Ratings at Discount Thresholds: Establish automated alerts for products entering the Heavy Discount bracket, tracking average customer ratings to identify quality perception risks before they compound
