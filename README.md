# Customer Satisfaction Analysis | Power BI Capstone Project

An end-to-end Power BI analysis of 10,999 e-commerce electronics orders, built for the **OdumareTech Data Analytics Bootcamp**. The project turns raw order data into an interactive dashboard and a stakeholder presentation, focused on customer satisfaction and delivery performance.

<img width="1800" height="1032" alt="dashboard_page1" src="https://github.com/user-attachments/assets/99c115cd-d784-4472-945c-55846b93afd5" />

<img width="1800" height="1032" alt="dashboard_page2" src="https://github.com/user-attachments/assets/fd6b67f7-9e31-43a2-852d-7af7ca09ba43" />

---

## Project Goals

An e-commerce company selling electronic products wants actionable insights from its customer database. The goals were to analyse:

1. **Customer demography**
2. **Customer satisfaction**
3. **Importance of products**
4. **Preferred mode of shipment**
5. **Promptness of shipment completion**
6. **Warehouse block usage** (5 blocks, A to E)

The company also asked for **additional KPIs** discovered during analysis, beyond the six above.

## Dataset

- **Source:** [Customer Analytics dataset by Prachi Gopalani on Kaggle](https://www.kaggle.com/datasets/prachi13/customer-analytics?resource=download)
- **Size:** 10,999 orders, 12 columns, no missing values or duplicate IDs
- **Key fields:** Warehouse block, Mode of shipment, Customer care calls, Customer rating (1 to 5), Cost of the product (USD), Prior purchases, Product importance, Gender, Discount offered (%), Weight (grams), Shipment completion promptness (1 = not on time, 0 = on time)

## Tools

- **Power BI Desktop:** data modelling, DAX measures, dashboard
- **Power Query:** data cleaning and calculated columns
- **PowerPoint / PDF:** stakeholder presentation
- **GitHub:** version control and documentation

### Dashboard
- **Page 1, Overview:** KPI cards (orders, revenue, rating, late %, discounts, delivery fees), orders and revenue by warehouse block, orders by shipment mode, late % by product importance and discount band, orders by rating
- **Page 2, Deep Dive:** orders by gender and product importance, late % by weight band, customer care calls and shipment mode, average rating by prior purchases
- Slicers for Mode of Shipment, Product importance, Gender and Warehouse block

## Key Findings

| Area | Finding |
|---|---|
| Overall | 10,999 orders, $2.25M revenue, average rating 2.99 / 5 |
| Demography | Even split: 5,545 female, 5,454 male. Same late rate and rating for both |
| Satisfaction | Ratings spread evenly across 1 to 5 (about 2,200 each). Late and on-time orders rate the same (about 3.0) |
| Product importance | Low 5,297, Medium 4,754, High 948 orders. High-importance products are late most often (65% vs about 59%) |
| Shipment mode | Ship 68%, Flight 16%, Road 16%. Late rates about 59 to 60% for every mode |
| Promptness | **59.7% of orders (6,563) were not delivered on time** |
| Warehouse blocks | Block E handles 3,666 orders (about 33%), double any other block, and earns about $0.75M vs $0.38M per other block |
| Extra: discounts | Orders with discounts over 10% (2,196 orders) were almost always late, vs 49.6% for 10% or less |
| Extra: weight | Parcels up to 3 kg are 74.8% late vs 50.5% for 3 to 6 kg (only 8 orders above 6 kg) |
| Extra: care calls | Late % falls from 65% at 2 calls to about 52% at 6 to 7 calls |

## Recommendations

1. **Review the discount process.** If discounted orders were late as often as the rest, overall lateness could fall from about 60% to about 50%.
2. **Prioritise high-importance products,** which are late 65% of the time.
3. **Rebalance warehouse work,** since Block E carries double the orders.
4. **Investigate why light parcels (0 to 3 kg) are late 75% of the time.**
5. **Use repeat care calls as an early warning,** and record delivery dates and delay reasons.

## Limitations

- The 100% late rate for discounts over 10% is unusually clean and should be verified against how the data was recorded.
- Ratings do not change with lateness, so the data does not explain what drives satisfaction.
- There are no dates, delay reasons, locations or customer IDs, so trends and repeat customers cannot be analysed.
- Some groups are small (only 8 orders above 6 kg).
- "Late" is yes or no, with no measure of how late.
- The dataset is a public sample and should be validated against full operational data.

