# TECHi traffic: is it up?

[R] = real scraped rows (120, opened 3 Oct 2026).  
[I] = invented traffic table.  
Figures are in `analysis.ipynb`.

**Bottom line:** Traffic is up, but not 30% YoY. Reported sessions are up 79%; about 70% of that increase appears to come from a tracking change. Underlying growth is about +24%.

## a) Is "up 30% YoY" true?

Not as stated, and it cannot be checked from the table. The table [I] starts in September 2025, so there is no month with a year-ago comparison.

The nearest pair is August 2026 vs September 2025:

102,805 / 57,500 - 1 = **+78.8%**

That is an 11-month comparison, not YoY. Neither figure is 30%.

## b) Underlying change

The 1 February step looks like a measurement change based on the table:

1. **January to February total:** 64,000 to 94,685 = **+47.9%**, compared with about **+1.7%** in a normal month.

2. **All six sections stepped together.** I let each section continue its own trend, using:

   Expected February = January + (January - September) / 4

   The resulting step factors range from **1.425 to 1.450**. Section trends range from about **+3% to -2.6% per month**. Guides also stepped up: expected 3,600 vs reported 5,220.

3. **Signups did not show the same step.** They continued their usual increase of about +30 per month. Sessions per signup went from 69.6 to 99.7 in one month.

The main calculation is:

**k = 94,685 / 65,625 = 1.443**

Adjusted August:

**102,805 / 1.443 = 71,253**

Compared with September 2025:

**71,253 / 57,500 - 1 = +23.9%**

So the estimated underlying increase is about **24% over 11 months**, or about **26% annualised**.

Using a k range of 1.425 to 1.480 gives an estimated increase of **20.8% to 25.4%**.

This assumes the tracking change affected the sections equally and that signups were unaffected. Neither assumption is verified.

### November

November looks like a one-off.

Crypto had 24,800 sessions compared with 10,550, the mean of October and December. That is about **14,250 extra sessions**, or 19% of that month's site total.

December returned to 11,000.

Signups were 860 compared with an expected 865, so there was effectively no conversion response.

### Signups

Signups increased from 820 to 1,140, or **+39.0%**. The increase was roughly +30 per month, with:

- no step in February
- no bump in November
- no visible dent when Guides declined

## c) Retire Guides?

**Merge it and keep the articles.**

Guides fell from 7.1% of sessions to 0.7%. It had 725 reported sessions, or about 500 after adjustment, which is an estimated **85% decline since March**.

Ads appear to contribute very little there.

In April, Guides sessions fell by 2,755 while signups still increased by about 30.

## Notes against rows [R]

"Guides has published almost nothing since March" is true for April to June, when there were five pieces, but it is contradicted by July, when there were 11.

"Second AI writer, September 2025" cannot be tested from these rows. The AI rows show eight bylines in the last 12 days, while the table's AI trend of about +700 sessions per month does not show a clear change.

The aggregator and snippet notes are also limited by the rows starting on 11 March. For those points, the table is the stronger source, and it supports both observations.

## Two findings from my rows [R]

**1. Publishing does not explain the Guides decline.**

Pieces per month from April to August:

**0, 3, 2, 11, 1**

Sessions over the same period:

**2,175; 1,595; 1,160; 870; 725**

July had the most pieces, but sessions still fell by 25%.

**2. Sections are loose labels.**

AI has 10 of 20 stock-ticker headlines, the same number as Markets.

Three articles appear in two sections, giving **117 unique URLs out of 120 rows**.

Five of the 17 bylines account for 74 of the 120 rows, across multiple sections.

## Where the rows meet the table

The loose section labels are one reason I use the **site total** rather than the section totals for the main traffic estimate.

## Recommendation and cost if wrong

Use **"about +24% since September (21% to 25%), signups +39%"** rather than 30% or 79%.

For Guides, merge the section but keep the articles.

If some of the February step is real traffic, this approach under-credits the team's growth. If the step is entirely measurement, using the reported sessions for ad forecasts would overstate traffic by up to about **1.44 times**.

Removing Guides risks about **500 adjusted sessions per month (0.7%)**, plus any signups that cannot be identified from the available data. The change is reversible.

I would change this conclusion if the ad network or server logs showed February 2026 pageviews more than 15% above January, compared with a normal trend of about 3%. I would also revisit the Guides decision if the email platform showed that Guides pages generated 30 or more of roughly 1,100 monthly signups.

The next useful number is the ad network's January and February 2026 pageviews because they should bypass the swapped analytics snippet. A ratio near **1.03** would be consistent with the measurement-change explanation; a ratio near **1.45** would indicate that the traffic increase was also present in the independent pageview data.

## Limits

- There is no year-ago month in the table.
- Relative dates in the scraped rows may be off by one day.
- The 20 newest rows cover different time periods, from 12 days for AI to 206 days for Guides.
- The tracking factor, k, is inferred rather than directly observed.