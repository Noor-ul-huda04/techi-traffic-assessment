# TECHi traffic: is it really up?

Reported sessions are up 79% since September. However, most of the increase appears to come from a tracking change on 1 February. After adjusting for that change, I estimate that the underlying growth is around 24%. The details and calculations are included in the memo and supporting files.

## Files

- memo.md: Main memo with the analysis, findings, and recommendation.
- method.txt: Explains how the 120 articles were collected and coded.
- techi_articles.csv: The 120 article records collected from the public TECHi pages.
- data_invented/traffic_table.csv: Traffic data provided in the brief. This is kept separate because it is not real scraped data.
- analysis.xlsx: Excel calculations using live formulas, including a Checks sheet.
- analysis.ipynb and analysis.py: Python versions of the analysis. Both produce the two charts.
- charts: The two charts, designed to work in black and white using different line styles, markers, and hatching.

## Setup

The analysis uses Python 3 with pandas, matplotlib, and openpyxl.

To run the Python version:

python analysis.py

The Excel version can also be opened directly in analysis.xlsx.

No account or paid software is required.

## Decisions

- I used the overall site total instead of section totals. The section pages overlap, with three articles appearing in two sections. The AI section also contains a large number of stock pieces.
- To estimate the February tracking effect, I calculated an expected value for each section using January traffic and its average monthly increase. I then compared the actual February value with that estimate. The six section factors were between 1.425 and 1.450, so I used 1.443 as the main adjustment factor and also calculated low and high cases.
- The traffic table does not contain the same month from the previous year, so I did not describe the comparison as year-over-year. The comparison is August 2026 against September 2025, which is an 11-month difference.
- I treated newsletter signups as a separate measure that is not affected by the analytics tracking change. This is an assumption because I do not have access to the underlying tracking setup.
- For Guides, I kept the articles and merged the section rather than removing them. This can easily be changed later.

## Tradeoffs and limitations

- The tracking factor is estimated rather than directly observed. It assumes the change affected the sections at roughly the same rate.
- The expected February traffic is based on a straight-line trend from five previous points.
- The 20 newest articles from each section are not enough to reach November 2025 or February 2026.
- The format and names_a_company fields were coded using my own judgement.

## Tests

The Checks sheet in analysis.xlsx contains the basic validation results:

- 120 rows
- No blank values in the required fields
- No word-count mismatches
- No digit mismatches
- 117 unique URLs
- Excel results match the Python results

## What I would improve

If I had more time or access to additional data, I would:

- Store the exact scrape date and time in the CSV.
- Open each article page and record its actual publication date instead of relying only on the section pages.
- Have a second person review the article-format coding.
- Get January and February 2026 pageview data directly from the ad/analytics network to test the estimated tracking factor.