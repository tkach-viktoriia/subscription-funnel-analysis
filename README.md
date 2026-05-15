# Subscription Funnel Analysis

Analysis of a subscription mobile app funnel — from ad impression to paid conversion.
Built on a simulated dataset of 10,000 users that reflects real-world subscription app metrics.

The full analysis is available in the [Jupyter notebook](subscription_funnel_analysis.ipynb).

## Main Summary & Recommendations

- **Key Finding:** Overall funnel conversion is 1.6% — only 158 out of 10,000 users who saw the ad became paying subscribers.
- **Biggest Drop-off:** Install step (70% of clicks never install) — the single highest-impact area for improvement.
- **Best Channel:** Google drives the highest overall conversion (1.91%) and the best trial-to-paid rate (40.2%).
- **Cohort Alert:** Conversion dropped 2x in March–April (from ~2% to ~1.1%) while channel mix stayed the same — suggesting a product-side issue.
- **Country Insight:** UA and DE outperform US despite significantly smaller audiences — ad spend allocation should be reconsidered.

## Dataset

Simulated dataset designed to reflect real subscription app funnel behavior:

| Parameter | Value |
|---|---|
| Total users | 10,000 |
| Acquisition channels | Google, Facebook, TikTok, Organic |
| Countries | US, UK, DE, UA, Other |
| Cohort period | January — April 2024 |
| Funnel steps | 6 (Impression → Click → Install → Onboarding → Trial → Paid) |

## Funnel Overview

| Step | Users | Conversion from Previous | Conversion from Start |
|---|:---:|:---:|:---:|
| Ad Impression | 10,000 | — | 100.0% |
| Clicked | 4,512 | 45.1% | 45.1% |
| Installed | 1,353 | 30.0% | 13.5% |
| Completed Onboarding | 877 | 64.8% | 8.8% |
| Started Trial | 453 | 51.7% | 4.5% |
| Converted to Paid | 158 | 34.9% | 1.6% |

**Install step has the highest drop-off (70%)** — 3,159 users clicked but never installed.

## Channel Performance

| Channel | Overall Conversion | Install Rate | Trial Rate | Paid Rate |
|---|:---:|:---:|:---:|:---:|
| Google | 1.91% | 32.8% | 32.6% | 40.2% |
| TikTok | 1.59% | 30.0% | 32.2% | 36.5% |
| Facebook | 1.41% | 27.3% | 36.4% | 30.7% |
| Organic | 1.10% | 28.9% | 31.7% | 27.1% |

Google leads in both overall conversion and trial-to-paid rate. Facebook has the lowest install rate despite high click volume — creatives likely attract irrelevant audience.

## Cohort Analysis

| Cohort | Users | Paid | Conversion Rate |
|---|:---:|:---:|:---:|
| 2024-01 | 2,465 | 47 | 1.91% |
| 2024-02 | 2,513 | 53 | 2.11% |
| 2024-03 | 2,575 | 30 | 1.17% |
| 2024-04 | 2,447 | 28 | 1.14% |

Conversion dropped ~2x starting March. Channel mix analysis confirmed no significant change in traffic sources — the root cause is likely a product or onboarding change in March.

## Country Performance

| Country | Overall Conversion | Install Rate | Trial Rate | Paid Rate |
|---|:---:|:---:|:---:|:---:|
| UA | 2.09% | 28.8% | 39.5% | 41.2% |
| DE | 1.96% | 30.4% | 34.2% | 42.6% |
| Other | 1.53% | 30.4% | 35.6% | 31.2% |
| UK | 1.44% | 27.6% | 35.8% | 33.3% |
| US | 1.40% | 31.2% | 30.0% | 32.4% |

US has the largest audience but the lowest conversion. UA and DE show the strongest quality despite smaller audiences.

## Best Channel by Country

| Country | Best Channel | Conversion |
|---|---|:---:|
| DE | Google | 2.81% |
| UA | Organic | 2.88% |
| UK | TikTok | 2.23% |
| US | Google | 1.90% |
| Other | Google | 1.91% |

No single universal channel — ad strategy should be localized per market.

## Key Recommendations

1. **Fix install funnel** — 70% drop-off is the single highest-impact issue
2. **Review Facebook creatives** — high clicks but lowest install rate
3. **Investigate March–April drop** — channel mix unchanged, likely a product issue
4. **Scale Google globally, TikTok for UK**
5. **Localize ad strategy per country** — best channel differs by market
6. **Reconsider US budget allocation** — largest audience but worst conversion

## Tools

- Python (pandas, numpy)
- Tableau Public

## Dashboard

[View Interactive Dashboard on Tableau Public](https://public.tableau.com/views/SubscriptionFunnelAnalysis_17787768975960/SubscriptionFunnelAnalysis)

## Repository Structure

- `README.md`
- `subscription_funnel_analysis.ipynb` — full analysis notebook
- `subscription_funnel_data.csv` — simulated dataset
- `subscription_funnel_analysis.png` — dashboard screenshot
