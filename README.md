# 📊 **RFM Analysis of a U.K. based Online Retail Firm**

The objective of this project is to perform RFM (Recency, Frequency, Monetary) analysis on a U.K. based and registered online retail company’s transactional data to segment customers based on their purchasing behavior, identify high-value and at-risk customers, and generate actionable insights to support targeted marketing strategies and improve customer retention.

# 📌 **Overview**

This project will cover the following:
- Conduct an exploratory data analysis of the retail firm's monthly sales performance.
- Perform RFM analysis of the firm's transactional data to segment customers and uncover valuable insights.

# 📂 **Datasets**
The dataset used for this project was publicly made available by the University of California's Machine Learning Repositry. Due to confidentiality reasons, the name of the retail firm was not disclosed.
- It contained a total of 541,909 transactions (rows) made between December 1, 2010 and December 9, 2011.
- Each transaction contained an Invoice Number, Product Name, Quantity, Transaction Date, Unit Price, Customer ID, and the Country from where the order was placed.

You can access this dataset by clicking [here](https://archive.ics.uci.edu/dataset/352/online+retail)

# 🔧 **Tools Used**

- **Python** was used for data wrangling.
- **Excel** was used for data visualization, exploratory data analysis, and RFM analysis.

# 📈 **Exploratory Data Analysis**

<img width="1135" height="513" alt="image" src="https://github.com/user-attachments/assets/26556742-00b0-48b2-93fe-b3509a411610" />

**Sales trend**
Revenue remains stagnant from December 2010 to August 2011, but accelerates meaningfully from September, culminating in a November 2011 peak of ~£1.45M — roughly double the quietest months (January–April 2011) and the strongest month in the entire dataset.

**Domestic dominance**
Domestic sales (orange) overwhelmingly drive revenue in every single month, consistently accounting for 78–90% of monthly revenue throughout the entire period — never dropping below three quarters of total sales. December 2010 and April 2011 share the highest domestic share at 90%, while January 2011 sees it dip to its lowest at 78%. The variation is relatively narrow, confirming domestic is not just dominant but structurally entrenched as the primary revenue engine.

**Unique customers**
The customer count line closely mirrors the sales trend but with two notable nuances. It dips more sharply in January–April than revenue does, implying fewer customers were transacting but spending more per visit — average transaction value was holding up the revenue floor during the slow months. From September onwards, both revenue and unique customers accelerate together, suggesting the Q4 growth is driven by both more customers and higher spend simultaneously.

# 🧠 **RFM Analysis**

## RFM Segmentation Map — 4,339 Customers

<img width="610" height="356" alt="image" src="https://github.com/user-attachments/assets/36d37271-c911-4a93-ae40-5a4a081c77e8" />

**How to read the grid**

Each cell represents a combination of Recency Score (x-axis, 1–5) and Frequency + Monetary Score (y-axis, 1–5). Higher scores are better on both axes — so the top-right corner (R=5, FM=5) is where your best customers live, and the bottom-left (R=1, FM=1) is where your most disengaged customers sit. Cell size is uniform but the percentage and count inside each cell tell you how concentrated your customer base is in that zone.

## Segment-by-Segment Interpretation

**Champions — 924 customers (21%)**
Your best customers across all three dimensions. They bought very recently, buy most frequently, and spend the most. They occupy the top-right cluster of the grid (R=4–5, FM=4–5), which is exactly where you want concentration. At 21% of your base this is a healthy proportion. These customers are already fully engaged — the priority is retention and reward rather than aggressive marketing. They are also your most likely brand advocates and referrers.

**Loyal Customers — 811 customers (19%)**
The second largest segment and the backbone of the business. They buy regularly with good frequency and spend, sitting in the middle-right zone (R=3–5, FM=3). They haven't quite reached Champion status but are on the path. Combined with Champions, these two segments represent 40% of your entire base — a strong signal of a relatively healthy customer base. The goal here is deepening the relationship to push them toward Champion status.

**Hibernating — 797 customers (18%)**
The third largest segment and a significant concern. These customers score low on all three dimensions — they sit in the bottom-left zone (R=1–2, FM=1–2), with the largest single cell being R=1, FM=2 at 9.9% (430 customers). They have not purchased in a long time, do not buy frequently, and spend little. At 18% of the base, this is a large pool of effectively lost customers. Mass re-engagement campaigns here typically yield poor ROI — a single low-cost reactivation attempt is worthwhile, but resources are better spent on segments closer to active.

**About to Sleep — 435 customers (10%)**
Sitting in the R=2, FM=1–2 zone, these customers are on the verge of becoming fully inactive. Their recency is fading and engagement is low. This is an urgent intervention segment — they have not gone fully dormant yet, so the cost of re-engagement is still lower than it will be if they slide into Hibernating. Time-limited offers and "we miss you" messaging are the standard playbook here.

**Promising — 372 customers (9%)**
Recent customers with moderate frequency but spend that hasn't fully developed yet. They appear in the R=3, FM=2 cell (6.2%, 270 customers) primarily. They show interest and have returned, but haven't committed to a regular purchasing habit. Second-purchase incentives, personalised product recommendations, and onboarding sequences are most effective here — the conversion window to Loyal Customer is still open.

**New Customers — 351 customers (8%)**
Very recent purchasers with low frequency, sitting along the bottom of the right side of the grid (R=4–5, FM=1–2). They have just discovered the business but have no purchase history to evaluate. The priority is triggering a second purchase quickly — the probability of a customer returning drops sharply after the first purchase if no second purchase follows within a reasonable window. Welcome flows and first-time buyer offers are the primary lever.

**At Risk — 305 customers (7%)**
These customers once had decent frequency and monetary scores but their recency has slipped badly — they sit in the R=1–2, FM=3 zone. They were reasonable customers who have gone quiet. Something changed — a bad experience, a competitor, or simply disengagement. Re-engagement campaigns acknowledging the gap work better here than generic discounts. Surveying this segment for feedback can also reveal systemic product or service issues.

**Can't Lose Them — 190 customers (4%)**
A small but disproportionately important segment. These customers sit in the R=1–2, FM=4–5 zone — they were once high-frequency, high-spending customers but haven't been seen in a long time. Losing them permanently would represent a significant revenue impact. At only 190 customers, this segment is small enough to warrant highly personalised, high-effort outreach — potentially direct personal contact rather than automated email sequences, depending on the business context.

**Potential Loyalist — 66 customers (2%)**
Recent customers with improving but not yet strong frequency and monetary scores. They are on a positive trajectory but the segment is small. The opportunity is real but limited in scale — nurturing campaigns and loyalty incentives can accelerate their development.

**Need Attention — 88 customers (2%)**
Sitting at R=3, FM=1, these customers have mid-range recency but very low frequency and spend. They engaged with the business not too long ago but have not developed a meaningful purchasing pattern. Re-engagement is still viable given the reasonable recency score, but the low FM profile means they need to be convinced of value rather than simply reminded to return.

## Overall Assessment

The distribution tells a broadly positive but cautionary story. The top-right concentration is encouraging — Champions and Loyal Customers together at 40% means the business has a strong core. However the bottom-left mass of Hibernating (18%) and About to Sleep (10%) customers means 28% of the base is disengaged or nearly lost. The strategic priority is clear: protect and reward the top-right, urgently intervene with About to Sleep before they slide further, and accept that Hibernating largely represents sunk cost requiring only minimal reactivation effort.

The Can't Lose Them segment, though small at 4%, deserves attention disproportionate to its size given the historical value those customers represent.

You can access the Python code used to perform the RFM Analysis by clicking [here.](https://github.com/akshay-joshi-25/RFM-Analysis-of-UK-Online-Retail/blob/main/RFM%20Analysis.ipynb)
