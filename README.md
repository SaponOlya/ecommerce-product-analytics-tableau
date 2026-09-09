# E-commerce Product Funnel & Conversion Dashboard

## Project overview

This project analyzes user behavior in an e-commerce product using Tableau Public. The dashboard tracks the purchase funnel, overall purchase conversion, and conversion differences across devices and traffic sources.

## Business questions

- How many users progress from visit to purchase?
- At which event-level funnel stage does the largest user drop-off occur?
- Does purchase conversion differ between Mobile and Web?
- Which traffic source has the lowest observed conversion and requires further investigation?

## Dataset

The analysis uses the [Product Analytics User Event Dataset (Casual Wear)](https://www.kaggle.com/datasets/yashch05/user-event-funnel-and-retention-analytics-dataset).

The dataset contains event-level e-commerce data with fields including:

- `user_id`
- `session_id`
- `event_date`
- `event_time`
- `event_type`
- `product_id`
- `category`
- `price`
- `device`
- `traffic_source`
- `country`
- `city`

## Dashboard

[View the interactive Tableau Public dashboard](ADD_TABLEAU_PUBLIC_LINK_HERE)

![Dashboard preview](images/dashboard_preview.png)

## Key metrics

- Unique users: 12,000
- Unique purchasers: 10,566
- Overall purchase conversion: 88.1%

## Key insights

- The largest absolute event-level drop-off occurs between `checkout` and `purchase`, where unique users decline from 11,533 to 10,566.
- Visit-to-purchase conversion is nearly identical across devices: approximately 66.8% for Mobile and 66.7% for Web.
- Referral has the lowest observed visit-to-purchase conversion at approximately 47.1%, compared with 48.6% for Email.
- The difference between traffic sources is descriptive and does not establish that traffic source causes a conversion difference.
- The final dates in the daily-unique-users trend show a sharp decline and should be validated for incomplete-day or data-pipeline effects before being interpreted as a real demand decrease.

## Recommendation

Do not reduce or pause Referral traffic based only on the observed 1.5 percentage-point gap versus Email. First, investigate traffic volume, referral partners, countries, devices, product categories, revenue per visitor, repeat purchase behavior, and attribution quality. If the pattern persists after these checks, test improvements to the referral landing experience or limit only weak referral sub-sources.

## Limitations

- This is an event-level exploratory funnel: it counts distinct users for each event type separately.
- The analysis does not enforce an ordered sequence of events within the same session and time window.
- Therefore, the funnel should not be interpreted as a strict session-level conversion funnel.
- The dataset is synthetic, and its high conversion rates should not be treated as real e-commerce benchmarks.

## Tools

- Tableau Public
- Kaggle dataset
- Product analytics: funnel analysis, conversion metrics, segmentation
