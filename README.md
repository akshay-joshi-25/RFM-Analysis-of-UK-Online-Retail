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

<img width="1135" height="513" alt="image" src="https://github.com/user-attachments/assets/f7d48ba2-0885-4520-ab13-b74ae164da6f" />

**Overall Sales Trajectory**

Sales grow steadily from a relatively modest base in December 2010 through to a dramatic peak in November 2011, before collapsing sharply in December 2011. The November peak is visually striking — it is clearly the highest bar by a significant margin, roughly double the typical monthly volume seen in the first half of the year. The December 2011 drop is equally dramatic, falling back to levels below even the quietest months of the year.

One critical piece of context explains this entirely: December 2011 only covers 9 days of data (December 1–9), not a full month. The November peak and December collapse are therefore largely an artefact of data completeness, not a genuine business reversal. November 2011 was likely capturing full pre-Christmas trading activity, while December 2011 was cut off early. This must be front-of-mind for any interpretation.

**Domestic vs International Split**

Domestic sales (orange) dominate overwhelmingly in every single month — International (blue) is a consistently small fraction of total revenue throughout the entire period. The blue bars are visible but thin across all months, suggesting international business is a minor channel rather than a meaningful revenue driver. There is no visible trend of international share growing or shrinking — it remains a flat, small contributor.

**Unique Customers Line**

The unique customer count (red line, right axis) tells an interesting secondary story. It broadly tracks sales volume — rising from around 950 in December 2010, dipping slightly in January–April 2011, then recovering and climbing steadily from July 2011 onwards, reaching its peak of ~1,700 in November 2011.

However there are two notable divergences worth flagging. First, the customer count in early 2011 (Jan–Apr) dips more noticeably than sales revenue does — suggesting that while fewer customers were transacting, the ones who did were spending more per transaction, keeping revenue relatively stable. Second, the December 2011 unique customer count drops to around 600, which is proportionally less severe than the revenue drop — again consistent with the partial month explanation, but also suggesting average transaction value may have been lower in that short December window.

**Seasonality and Business Rhythm**

Stripping out the November/December distortion, the underlying pattern shows a mild mid-year trough in April 2011 (the quietest complete month), a steady recovery through summer, and a clear acceleration from September onwards. This is consistent with a typical retail seasonal pattern where Q4 represents peak trading. The September–November ramp is the strongest growth period in the dataset.

**Key Takeaways**

The business is heavily domestically driven with international representing a structurally minor share. Revenue and customer volume broadly move together, with the notable early-2011 divergence suggesting average spend per customer was higher in that period. The November 2011 peak and December 2011 trough should not be interpreted as a boom-bust event — they are a direct consequence of the partial December data window. The more meaningful signal is the consistent upward growth trend from July through November, which suggests genuine underlying business momentum heading into the full Christmas trading period.
