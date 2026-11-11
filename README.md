# Duka Bora sales dashboard (Power BI)

![Dashboard](DUKA%20MOJA.png)

My first Power BI dashboard, analysing 22 months of sales (Jan 2025 – Oct 2026) for **Duka Bora Supermarkets**, a chain of 6 stores across Kenya: Nairobi CBD, Westlands, Mombasa Nyali, Kisumu Milimani, Nakuru Town and Eldoret Central.

> Note: Duka Bora is a fictional company. The dataset is simulated for learning, but it is modelled on real Kenyan retail patterns: M-Pesa as the main payment method, month-end payday spikes, the December peak, back-to-school demand and school-fees months.

## Business questions
1. How are sales and profit trending over time?
2. Which stores sell the most, and which earn the least per sale?
3. Which stores are giving away margin through discounts?
4. How are customers ordering: in-store, WhatsApp or online?

## Headline numbers
| Metric | Value |
|---|---|
| Revenue | KES 31.0M |
| Profit | KES 4.59M |
| Margin | 14.8% |
| Orders | 28,009 |

## Key finding
**Mombasa Nyali is losing margin to discounts.** Its margin fell from about 15.5% in 2025 to about 10% in 2026. Since March 2026 its average discount has been 6.2%, against under 1% in every other store. Sales did not grow enough to make up for it.
**Recommendation:** review the Mombasa promotion. Is it bringing in new customers, or discounting sales that would have happened anyway?

## Data model
A star schema with one fact table and three lookup tables:
- **Sales** (fact): one row per item sold
- **Products**: 25 products in 7 categories
- **Stores**: 6 stores with county and region
- **Targets**: monthly revenue target for each store

## DAX measures
