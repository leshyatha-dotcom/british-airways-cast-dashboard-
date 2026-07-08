# British Airways Customer Satisfaction (CSAT) Dashboard

Tableau dashboards analyzing British Airways customer reviews to uncover satisfaction drivers, segment-level differences, and recommendations for improving customer experience.

## Business Objective

To analyze British Airways customer review data and identify the key drivers of customer satisfaction across service categories, traveller segments, and cabin classes — enabling data-driven recommendations to improve overall customer experience and recommendation rate.

## Business Problem

British Airways collects large volumes of customer reviews covering overall satisfaction and specific service categories (seat comfort, cabin staff, food & beverages, entertainment, ground service, and value for money), but this feedback is not consolidated into an actionable view. Without a clear picture of:
- which service areas underperform,
- which customer segments are least satisfied, and
- how satisfaction connects to whether customers would recommend the airline,

it is difficult for BA to prioritize where to invest in service improvements.

## Data Preparation

- **Source:** BA customer reviews dataset (`ba_reviews.csv`) joined with `Countries.csv` for geographic analysis
- **Total reviews analyzed:** 1,324
- **Data cleaning:** The 7 sub-category rating fields (Seat Comfort, Cabin Staff Service, Food & Beverages, Entertainment, Ground Service, Value For Money, and Overall Rating) contained placeholder values of **-1**, representing "not rated." These were excluded from all average calculations using calculated fields (e.g., `Rating Cleaned`, `Seat Comfort Cleaned`) to prevent them from artificially deflating KPI averages.
- **Scale note:** The overall `Rating` field uses a 1–10 scale, while the six sub-category fields use a 1–5 scale — this distinction was preserved during cleaning to avoid incorrectly truncating valid data.
- Aircraft names contained inconsistent/combined entries (e.g., multiple aircraft types merged into a single field); this is noted as a data limitation rather than corrected, to preserve the original record integrity.

## Dashboards

**Dashboard 1 — Satisfaction Overview**
KPI cards for all 7 rating categories, a world map of review density and average rating, a monthly satisfaction trend line, and average ratings by aircraft type.

**Dashboard 2 — Customer Segments**
Recommendation split (Yes/No), average rating by traveller type (Business, Solo Leisure, Couple Leisure, Family Leisure), and average rating by seat type (Economy, Premium Economy, Business, First).

## Insights

- **Overall satisfaction:** Average rating is **4.19 / 10**, indicating more customers report negative experiences than positive ones.
- **Weakest service categories:** Entertainment (2.72/5) and Food & Beverages (2.66/5) score lowest among sub-categories, while Cabin Staff Service (3.32/5) scores highest.
- **Recommendation rate:** Only **56.8%** of reviewers would recommend British Airways, while **43.2%** would not — a meaningful gap given the overall rating is below the midpoint of its scale.
- **Traveller type differences:** Business travellers report the highest average satisfaction (4.19), while Family Leisure travellers report the lowest (3.80) among segments analyzed.
- **Seat type differences:** Economy Class (4.36) and Premium Economy (4.22) passengers report comparatively higher satisfaction than other cabin classes in this dataset.
- **Trend:** Monthly average ratings fluctuate between 3.0 and 5.0 across the year, with no single sustained period of improvement or decline — suggesting satisfaction issues are systemic rather than seasonal.

## Business Recommendations

1. **Prioritize in-flight entertainment and food & beverage improvements** — these are the two lowest-rated service categories and the most direct levers for closing the gap between overall rating and recommendation rate.
2. **Investigate the Family Leisure segment specifically** — this group reports the lowest satisfaction; targeted research (e.g., family-friendly seating, entertainment content, meal options) could improve retention within this segment.
3. **Treat the 43.2% "would not recommend" group as a churn-risk segment** — follow-up surveys or service recovery outreach to this group could help identify root causes not captured in numeric ratings.
4. **Use Cabin Staff Service as a service benchmark** — since it is the highest-rated category, examine what training or process differences contribute to its performance and apply learnings to lower-scoring categories.
5. **Continue monitoring trend data monthly** — the lack of a clear seasonal pattern suggests operational or service-consistency issues rather than one-off events, warranting ongoing tracking rather than a single corrective action.

## Conclusion

This analysis shows that British Airways' overall customer satisfaction, while moderate, is held back primarily by in-flight entertainment and food & beverage service, with Family Leisure travellers representing the most at-risk segment. With just over half of customers willing to recommend the airline, targeted improvements in the identified weak areas — supported by continued monitoring — offer the clearest path to improving both satisfaction scores and word-of-mouth recommendation rates.

## Tools Used

- **Tableau Public** — dashboard design and data visualization
- **Data cleaning** — calculated fields for handling missing/placeholder values
- Dataset joined with country-level reference data for geographic analysis

## Files in This Repository
