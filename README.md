# **AIRBNB GLOBAL PERFORMANCE ANALYSIS**

### **Pricing, value, amenities and host behaviour across 108 countries | Power BI · DAX · Marketplace Analytics**


<img width="2400" height="1350" alt="airbnb" src="https://github.com/user-attachments/assets/3145ae6d-e5e9-4f7d-a0f7-6890d6080049" />



[**Business report (PDF)**]
· [**Power BI file (.pbix)**](Airbnb.pbix)

---

## **Project Overview**

An end-to-end marketplace analysis of **7,561 Airbnb listings** from **6,520 hosts** in **108 countries**, delivered as a 5-page interactive Power BI dashboard plus a written business report. The work answers how a travel marketplace's supply is distributed, what guests pay, where value is highest, which amenities command a premium, and how the host base is structured.

| Metric | Value |
|---|---|
| Unique listings | **7,561** |
| Unique hosts | **6,520** |
| Countries | **108** |
| Total reviews | **419,074** |
| Average price per night* | **13,868** (median **8,486**) |
| Average rating | **4.86 / 5** (median 4.89) |
| Median price per guest | **2,185** |

\*Prices are in the dataset's native currency units; the source file does not label the currency.

---

## **10 Business Questions and Reports**

### **Q1. How large and concentrated is the marketplace?**
- **Finding:** 7,561 listings across 108 countries. The top 5 countries hold **43.9%** of listings and the top 10 hold **60.0%**. India leads with 1,258 listings (**16.6%**), followed by Greece (688), Italy (652), France (385) and Thailand (333).
- **Report:** Supply is concentrated in a handful of tourism markets, so market-level shocks (regulation, demand) would hit a large share of inventory.

### **Q2. Is average price a reliable benchmark?**
- **Finding:** No. Mean price is **13,868** but the median is **8,486**; the mean sits **63% above** the median. Price skewness is **20.6**, with P90 at 28,529 and P99 at 91,341.
- **Report:** A small luxury tail inflates the average. Median price should be the reporting standard for benchmarking and pricing guidance.

### **Q3. How is supply split across price tiers?**
- **Finding:** Budget (up to 10K) is **57.9%** of listings (avg price 5,215), Mid-range (10K to 50K) is **38.4%** (19,488), and Luxury (above 50K) is **3.6%** (92,560).
- **Report:** The marketplace is a budget and mid-range business. Luxury is a niche, but its average price is **17.7x** the budget tier.

### **Q4. Does paying more buy better guest satisfaction?**
- **Finding:** Barely. Average rating is **4.84** (Budget), **4.88** (Mid-range) and **4.89** (Luxury). **71.6%** of listings are rated 4.8 or higher, and only **0.5%** are below 4.5.
- **Report:** Price is a weak signal of quality. Ratings cluster at the ceiling, so rating alone cannot separate good from excellent.

### **Q5. Which markets deliver the best value?**
- **Finding:** Using High Value Score (rating divided by average price, times 1000) for markets with 30+ listings: **Cuba 1.83**, India 0.73, Georgia 0.72, Romania 0.63, Bulgaria 0.63, Taiwan 0.59. Cuba scores **2.5x** the next market.
- **Report:** Value markets are low-price markets that still earn 4.8+ ratings. They are natural targets for value-led demand campaigns.

### **Q6. Which markets are premium, and how wide is the price gap?**
- **Finding:** Highest average prices (30+ listings): United States **30,977**, Canada 28,334, Israel 27,031, Greece 24,061, Italy 18,775. Lowest: Cuba **2,643**, India 6,605, Georgia 6,755. The top-to-bottom gap is **11.7x**. The lowest value scores are the US (0.16), Canada (0.17), Israel (0.18) and Greece (0.20).
- **Report:** Premium markets charge far more for similar ratings. Greece is the key case: large supply (688 listings) with a heavy upper tail (average 24,061 vs median 15,445).

### **Q7. How does price scale with property size?**
- **Finding:** Median price rises from **6,288** (1 bedroom) to 9,818 (2), 14,180 (3), 21,189 (4) and **33,101** (5+). Bedrooms and price correlate at Spearman rho = **0.45**. Median price per guest stays flat at about **2,000 to 2,300** up to 4 bedrooms, then reaches 2,658 for 5+.
- **Report:** Hosts price roughly in proportion to capacity. Large homes earn only a modest per-guest premium (about 19% over 1-bedroom listings).

### **Q8. Which amenities are linked to price premiums?**
- **Finding:** Median price premium for listings with vs without: **hot tub +88%** (13% of listings), **pool +78%** (27%), **water view +60%** (9%), TV +40% (59%), Wifi +17% (83%), free parking +14% (75%), air conditioning +6% (36%). All differences are significant (Mann-Whitney p < 0.01).
- **Report:** Lifestyle amenities carry the biggest premiums, while basics (Wifi, parking) are near-universal and add little. Premiums are associations, not proof of cause, because pools and hot tubs also cluster in larger homes and premium markets.

### **Q9. How fragmented is the host base, and do multi-listing hosts perform differently?**
- **Finding:** **89.2%** of hosts have a single listing. Multi-listing hosts (10.8%) hold **23.1%** of listings; the largest host has 10 listings and the top 10 hosts hold only **1.0%** of listings. Multi-listing hosts price **11% lower** at the median (7,734 vs 8,671) and rate slightly lower (4.844 vs 4.861).
- **Report:** The marketplace is made of small hosts with no dominant operator. Professional hosts cluster in India, Greece, Italy and Thailand. The rating gap is statistically significant but only 0.017 points.

### **Q10. How is guest engagement (reviews) distributed?**
- **Finding:** Average **55.4** reviews per listing, median **28**. The top 20% of listings capture **62.2%** of all reviews. Reviews and rating are weakly negatively correlated (rho = **-0.19**). The United Kingdom averages about **105 reviews per listing** at a 4.94 rating, versus about 33 for India.
- **Report:** Engagement is highly unequal. Established, heavily reviewed listings rate slightly lower than lightly reviewed ones, which suggests early ratings run high.

---

## **Dashboard Preview**

> **How to add your dashboard screenshots:** in Power BI Desktop use *File > Export > Export to PDF*, or take a screenshot of each page. Save the five images into `images/dashboard/` using the exact names below. They will appear automatically once pushed to GitHub.

### **Page 1: Global Overview**

![Global Overview dashboard](images/dashboard/01_global_overview.png)

*Slot: `images/dashboard/01_global_overview.png`. Visuals: KPI cards, country map, price vs rating scatter, average price by country.*

| 7,561 listings | 6,520 hosts | 108 countries | 419,074 reviews | 13,868 avg price | 4.86 avg rating |
|---|---|---|---|---|---|

**Business insight:** Supply is concentrated. The top 5 countries (India, Greece, Italy, France, Thailand) hold **43.9%** of listings. India is the volume leader (1,258 listings, **16.6%**) at a median price of just **3,994**, while Greece has 688 listings at a median of **15,445**. Volume markets and premium markets are different places.

**Statistical insight:** Price is extremely right-skewed (skewness **20.6**): mean 13,868 vs median 8,486 (mean **+63%**), P90 28,529, P99 91,341. Report medians. Across countries with 30+ listings, price and rating correlate at Spearman rho = **0.38** (p = 0.014).

### **Page 2: Value and Pricing**

![Value and Pricing dashboard](images/dashboard/02_value_pricing.png)

*Slot: `images/dashboard/02_value_pricing.png`. Visuals: price bucket slicer, High Value Score, price per guest, price tier charts.*

| Tier | Share of listings | Avg price | Avg rating |
|---|---|---|---|
| Budget (up to 10K) | 57.9% | 5,215 | 4.84 |
| Mid-range (10K to 50K) | 38.4% | 19,488 | 4.88 |
| Luxury (above 50K) | 3.6% | 92,560 | 4.89 |

**Business insight:** The luxury tier costs **17.7x** the budget tier and earns only **+0.05** rating points. Best value: Cuba (1.83), India (0.73), Georgia (0.72), Romania (0.63). Weakest value: United States (0.16), Canada (0.17), Israel (0.18), Greece (0.20).

**Statistical insight:** Price and rating correlate at Spearman rho = **0.19** (p < 0.001); a Kruskal-Wallis test across tiers gives H = **190.4** (p < 0.001). The difference is real but small: price explains only about **3.5%** of rating variation (rho squared). **71.6%** of listings are rated 4.8+, a ceiling effect.

### **Page 3: Amenities and Property Mix**

![Amenities and Property Mix dashboard](images/dashboard/03_amenities_property_mix.png)

*Slot: `images/dashboard/03_amenities_property_mix.png`. Visuals: amenity and country slicers, bedroom donut, guests vs price scatter, amenity bars.*

| Amenity | Prevalence | Median price with | Median price without | Premium |
|---|---|---|---|---|
| Hot tub | 13.1% | 14,603 | 7,757 | **+88%** |
| Pool | 27.0% | 13,174 | 7,418 | **+78%** |
| Water view | 9.0% | 13,052 | 8,154 | **+60%** |
| TV | 59.1% | 9,710 | 6,959 | +40% |
| Wifi | 82.7% | 8,766 | 7,467 | +17% |

**Business insight:** One-bedroom listings are **50.1%** of supply (3,789). Median price climbs from 6,288 (1 bedroom) to 33,101 (5+). Pools, hot tubs and water views are the strongest price-linked amenities.

**Statistical insight:** Bedrooms vs price: Spearman rho = **0.45**. Premium differences are significant (Mann-Whitney p < 0.001 for hot tub, pool, water view, TV, Wifi). Listings with each premium amenity still average **4.85 to 4.87** in rating, in line with the 4.86 overall, so amenities lift price, not rating. Median price per guest is flat (about 2,000 to 2,300) up to 4 bedrooms.

### **Page 4: Host Analysis**

![Host Analysis dashboard](images/dashboard/04_host_analysis.png)

*Slot: `images/dashboard/04_host_analysis.png`. Visuals: host and listing KPIs, top hosts, host rating and listing combo, country bars.*

| Single-listing hosts | Multi-listing hosts | Listings held by multi-listing hosts | Largest host | Top 10 hosts' share |
|---|---|---|---|---|
| 89.2% | 10.8% | 23.1% | 10 listings | 1.0% |

**Business insight:** Supply is fragmented across small hosts with no dominant operator. Multi-listing hosts concentrate in India, Greece, Italy and Thailand and price **11% lower** at the median (7,734 vs 8,671 for single-listing hosts).

**Statistical insight:** Ratings differ between host types (Mann-Whitney p < 0.001) but by only **0.017 points** (4.844 vs 4.861), a negligible effect. Reviews per listing: 51.7 for multi-listing hosts vs 56.6 for single-listing hosts.

### **Page 5: Country Deep-Dive**

![Country Deep-Dive dashboard](images/dashboard/05_country_deep_dive.png)

*Slot: `images/dashboard/05_country_deep_dive.png`. Visuals: price by bedrooms and country matrix, country slicer, ranking table.*

| Priciest (30+ listings) | Avg price | Cheapest (30+ listings) | Avg price |
|---|---|---|---|
| United States | 30,977 | Cuba | 2,643 |
| Canada | 28,334 | India | 6,605 |
| Israel | 27,031 | Georgia | 6,755 |
| Greece | 24,061 | Bulgaria | 7,703 |

**Business insight:** The price gap between the top and bottom market is **11.7x**. Cuba's value score (1.83) is **2.5x** the next market. Engagement varies sharply: the United Kingdom averages about **105 reviews per listing** (rating 4.94) vs about **33** in India.

**Statistical insight:** Reviews are heavily skewed: the top 20% of listings hold **62.2%** of all reviews (mean 55.4, median 28). Reviews and rating correlate at rho = **-0.19** (p < 0.001), which suggests early ratings run high and settle as reviews accumulate (a hypothesis, not proven here).

---

## **Key Takeaways**

1. **Supply is concentrated.** Five countries hold 43.9% of listings, so regional shocks have an outsized effect.
2. **Average price misleads.** Mean is 63% above the median because of a small luxury tail; use medians.
3. **Price does not buy quality.** A 17.7x price jump from Budget to Luxury adds only 0.05 rating points.
4. **Value sits in low-price markets.** Cuba, India, Georgia and Romania earn 4.8+ ratings at a fraction of premium-market prices.
5. **Lifestyle amenities carry the premium.** Hot tubs, pools and water views are linked to +60% to +88% higher median prices; basics like Wifi add little.
6. **Hosts are small and fragmented.** 89.2% have one listing and the top 10 hosts hold 1.0% of supply.
7. **Ratings are saturated.** 71.6% of listings score 4.8 or higher, so ratings alone cannot rank quality.

## **Business Recommendations**

| Insight | Recommended action |
|---|---|
| Mean price is distorted by a luxury tail | Report median price and median price per guest as the standard benchmarks |
| Cuba, India, Georgia, Romania, Taiwan lead on value | Run value-led demand campaigns and recruit supply in small value markets (Romania, Bulgaria, Serbia) |
| Pool, hot tub and water view carry +60% to +88% price links | Coach hosts to highlight or add these features; test the premium with controlled pricing experiments |
| Price per guest is flat up to 4 bedrooms | Give hosts capacity-based price guidance (about 2,000 to 2,300 per guest) |
| 71.6% of listings are rated 4.8+ | Add finer quality signals (sub-ratings, review text) so ranking does not rely on stars alone |
| US, Canada, Israel and Greece have the lowest value scores | Position as premium markets and test value messaging or bundles |
| 89.2% single-listing hosts, 10.8% of hosts hold 23.1% of listings | Build onboarding for small hosts; monitor quality on multi-listing hosts |
| Reviews concentrated in top 20% of listings | Create review-nudge flows to lift newer listings |
| Row duplication in the data model (see below) | Split into Listings and Amenities tables and fix the DAX measures before wider sharing |

## **Data Quality and Limitations**

- **The source table has one row per amenity.** The 71,281 rows represent only **7,561 unique listings** (about 9.4 rows each). All figures in this report use distinct listing IDs.
- **Known dashboard issue (current .pbix):** `Total_Reviews = SUM(airbnb[reviews])` adds the review count once per amenity row, giving **3,924,642** instead of the true **419,074**. As a result `Reviews per Listing` shows **519** instead of **55.4**. `Average_Price` and `Average_rating` are also weighted by amenity rows (price 14,108 vs 13,868 per listing). Suggested fix:
  ```DAX
  Total_Reviews = SUMX ( VALUES ( airbnb[id] ), CALCULATE ( MAX ( airbnb[reviews] ) ) )
  Average_Price = AVERAGEX ( VALUES ( airbnb[id] ), CALCULATE ( MAX ( airbnb[price] ) ) )
  Average_rating = AVERAGEX ( VALUES ( airbnb[id] ), CALCULATE ( MAX ( airbnb[rating] ) ) )
  ```
  The cleaner long-term fix is a Listings table plus a separate Amenities table linked on `id`.
- **No dates.** The dataset is a snapshot, so seasonality, occupancy and revenue cannot be analysed.
- **Price currency is not labelled.** Values are in native units.
- **Data cleaning applied:** country names were trimmed of stray spaces; 1 rating above 5 (value 40) was excluded from rating statistics; 2 listings with no price were excluded from price statistics.
- **Association, not causation.** Amenity premiums and country comparisons are descriptive; larger homes and premium markets also differ in other ways.
- **Small markets excluded from rankings.** Country rankings require 30+ listings.

## **Tools Used**

- **Power BI Desktop:** data modelling, DAX measures (High Value Score, price per guest, host listing counts, price tiers), report design
- **Power Query:** cleaning and transformation
- **Python (pandas, SciPy):** listing-level validation, Spearman, Kruskal-Wallis and Mann-Whitney tests
- **Statistics:** correlation, non-parametric hypothesis tests, skewness

## **Repository Structure**

```
AirBnB-analysis/
├── README.md
├── Airbnb.pbix
├── reports/
│   └── Airbnb_Business_Report.pdf
└── images/
    ├── airbnb.png
    └── dashboard/
        ├── 01_global_overview.png
        ├── 02_value_pricing.png
        ├── 03_amenities_property_mix.png
        ├── 04_host_analysis.png
        └── 05_country_deep_dive.png
```

---

**Author:** Trishula Mitra · Data Analyst · Kolkata, India





















- 💬 **Ask me about:** Power BI dashboards, data cleaning, pricing analysis

---

<p align="center"><i>Data tells the story. I make it actionable.</i></p>
