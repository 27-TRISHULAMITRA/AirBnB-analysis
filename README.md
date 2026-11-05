🎯 About Me

I am a Data Analyst specializing in E-commerce and marketplace analytics.

🔍 Decision first. Every analysis starts with a business question.
🧹 Clean data, trusted insights. I validate before I visualize.
📈 One dashboard, one story. Each page answers one decision.
🤝 Data to action. I turn metrics into clear recommendations.
🧰 Technical Toolbox
💻 Languages & Data Wrangling
Python (Pandas, NumPy)
Data cleaning: duplicates, nulls, whitespace, type fixes, outliers
Feature engineering: price buckets, value scores, per-guest metrics
📊 Data Visualization & BI
Power BI (DAX, data modeling, interactive dashboards)
Excel (Pivot Tables, formulas, charts)
🛒 Domain Expertise
E-commerce analytics: pricing, ratings, reviews, segmentation
Marketplace analysis: supply, seller performance, product mix
📌 GitHub Stats
<p align="center"> <img height="170" src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=default&hide_border=true" /> <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=default&hide_border=true" /> </p>
🏠 Featured Project: Airbnb Listings — Cleaning & Visual Analysis

Business Problem: Raw listing data was inconsistent. Pricing, quality, host and amenity drivers were unclear. Tech Stack: Python · Power BI · DAX · Excel Output: 5-page interactive Power BI report.

🧹 Data Preparation Impact
Metric	Before	After
Rows (amenity-exploded)	71,281	7,559 unique listings
Country labels	131 (whitespace duplicates)	106 valid markets
Corrupted records	2 shifted rows	Removed
Missing prices	2 listings	Flagged

Engineered fields:

Price Bucket: Budget (≤ 10,000) · Mid-range (≤ 50,000) · Luxury (> 50,000)
Price per Guest = Average price ÷ Average guests
High Value Score = (Average rating ÷ Average price) × 1000
Host Type: Single-listing vs Multi-listing (2+)
📌 Headline KPIs
🏘️ Listings	👤 Hosts	🌍 Markets	💰 Avg Price	💵 Median Price	⭐ Avg Rating	💬 Reviews
7,559	6,518	106	13,868	8,486	4.86	419,074

💡 Prices are in the source dataset's currency units.

🌍 Dashboard 1 — Global Overview
<table> <tr><td align="center">


<img width="1344" height="740" alt="Screenshot 2026-11-05 154530" src="https://github.com/user-attachments/assets/4cb3e7a3-cc31-47ed-bbeb-1026097462d1" />


</td></tr> </table>
💼 Business Insight
Concentrated supply. The top 10 markets hold 60.0% of listings.
India leads with 1,258 listings (16.6% share).
Next in line: Greece 688, Italy 652, France 385, Thailand 333.
Premium vs value markets:
United States is the priciest (≥ 30 listings) at 30,977.
Greece averages 24,061, 3.6x India's 6,605.
Cuba is the lowest at 2,643.
Action: Position India, Georgia and Cuba as value markets. Target US, Canada and Israel for premium pricing.
📐 Statistical Insight
Median price (8,486) sits 39% below the mean (13,868).
Skewness = 20.6. A few luxury listings pull the average up.
P90 = 28,529 and P99 = 91,341. Use the median for typical price.
Rating is saturated: average 4.86, median 4.89, and 71.6% of listings score ≥ 4.8.
💰 Dashboard 2 — Value & Pricing
<table> <tr><td align="center">

<img width="1764" height="820" alt="Screenshot 2026-11-05 154748" src="https://github.com/user-attachments/assets/e0aef902-9883-4dd7-a9de-52fbac3a5df1" />


</td></tr> </table>
💼 Business Insight
Budget dominates supply: 57.9% of listings (4,381).
Mid-range holds 38.4% (2,906). Luxury is only 3.6% (274).
Budget wins on value: High Value Score 0.93 vs 0.05 for Luxury (17.6x).
Price per guest climbs fast:
Bucket	Avg Price	Price / Guest	Avg Rating
Budget	5,215	1,345	4.85
Mid-range	19,488	3,311	4.88
Luxury	92,560	8,706	4.89
Action: Luxury charges 17.7x Budget's price for only +0.04 rating. Promote Budget and Mid-range as the best value tiers.
📐 Statistical Insight
Price vs rating: Pearson r = 0.075 (very weak). Paying more does not buy better quality.
Price vs guests: r = 0.36 (0.45 on log price).
Price vs bedrooms: r = 0.40. Capacity drives price more than quality.


🛏️ Dashboard 3 — Amenities & Property Mix
<table> <tr><td align="center">

<img width="1766" height="810" alt="Screenshot 2026-11-05 154807" src="https://github.com/user-attachments/assets/0eb9781c-3f26-44f0-8707-f912ee70a93f" />



</td></tr> </table>
💼 Business Insight
Core amenities are standard: Kitchen 78.7%, Wifi 77.8%, Free parking 74.6%.
Premium amenities command a premium (median price):
Amenity	Listing Share	Median With	Median Without	Uplift
Hot tub	13.1%	14,603	7,757	+88%
Pool	27.0%	13,174	7,418	+78%
Wifi	82.7%	8,766	7,467	+17%
Free parking	75.2%	8,722	7,634	+14%
Property size scales price: 1-bedroom avg 8,389 → 4-bedroom avg 28,448 (3.4x).
Action: Add pool or hot tub to lift price. Basic amenities only meet expectations.
📐 Statistical Insight
Amenity count vs price: r = 0.064. Amenity type matters, not volume.
Average listing has 9.4 amenities.
Rating stays flat at 4.85–4.92 across bedroom counts.
Pool listings: rating 4.85 vs 4.87 without. Pools raise price, not satisfaction.

👤 Dashboard 4 — Host Analysis
<table> <tr><td align="center">


<img width="1735" height="806" alt="Screenshot 2026-11-05 154723" src="https://github.com/user-attachments/assets/d6e82cfa-17b5-4307-973b-0a1efdb08fb3" />


</td></tr> </table>
💼 Business Insight
Fragmented supply: 6,518 hosts manage 7,559 listings (1.16 per host).
Multi-listing hosts are only 10.8% of hosts but own 23.1% of listings.
Largest portfolio: 10 listings per host.
Professional hosts price lower:
Host Type	Listings	Avg Price	Avg Rating	Reviews / Listing
Single-listing	5,818	14,337	4.87	56.6
Multi-listing (2+)	1,743	12,302	4.84	51.7
Action: Multi-listing hosts compete on volume. Single-listing hosts earn a 14% price premium.
📐 Statistical Insight
Price gap: multi-listing hosts are 14.2% cheaper on average.
Rating gap: only 0.02 points. Not practically significant.
Rating vs reviews: r = −0.017. Review volume does not predict rating.
Data note: host_name is not unique (e.g., "Maria" spans 29 listings). Analysis uses host_id.
🔎 Dashboard 5 — Country Deep Dive
<table> <tr><td align="center">

<img width="1750" height="804" alt="Screenshot 2026-11-05 154615" src="https://github.com/user-attachments/assets/6c85c30d-468e-4473-bca9-d93a78ba1dc2" />


</td></tr> </table>
💼 Business Insight
Best value markets (≥ 30 listings, High Value Score):
Market	Listings	Avg Price	Value Score
Cuba	115	2,643	1.83
India	1,258	6,605	0.73
Georgia	233	6,755	0.72
Highest-demand markets (reviews per listing): Iceland 264, United States 137, Switzerland 115, United Kingdom 105.
India has the most total reviews (41,102) but only 32.7 per listing.
Premium markets (US, Greece) score 0.16–0.20.
Action: Scale supply in India and Georgia. Defend premium pricing in the US and UK.
📐 Statistical Insight
Top-rated: UK 4.94, Canada 4.93, US 4.92.
Lowest-rated: Portugal 4.81, India 4.82, Belgium 4.82.
Rating spread across markets is only 0.12 points.
Price spread is 11.7x (2,643 to 30,977). Price, not rating, separates markets.
Sample caution: markets under 30 listings are excluded from rankings.
✅ Key Takeaways
🌍 Supply is concentrated: 60% of listings sit in 10 markets.
💰 Price is driven by capacity: bedrooms (r = 0.40) and guests (r = 0.36), not rating (r = 0.075).
🏊 Amenities that pay: hot tub +88% and pool +78% median price.
👤 Hosts are small-scale: 1.16 listings per host.
⭐ Quality is uniform: 4.86 average rating, so price becomes the main decision lever.
🤝 Let's Connect
<p align="left"> <a href="https://www.linkedin.com/in/YOUR_HANDLE"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a> <a href="mailto:trishulamitra@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a> <a href="https://YOUR_PORTFOLIO_URL"><img src="https://img.shields.io/badge/Portfolio-Visit-2E7D32?style=for-the-badge&logo=googlechrome&logoColor=white" /></a> </p>
📫 Email: trishulamitra@gmail.com
💼 Open to: Data Analyst roles in E-commerce
💬 Ask me about: Power BI dashboards, data cleaning, pricing analysis
<p align="center"><i>Data tells the story. I make it action
