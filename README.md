# Swiss {ai} Weeks

## Challenge: Swiss Financial Statement Analyst

Write an AI solution that calcualtes the following key fincancial ratios from financial statements. 

You can find an example calculation in the `./example_calc/` folder. 

You will be provided with ten example financial statements in the `./example_statements/` folder. 

Please note, that the exact wording of the required lines is not standardized. Expect to see variations in representation and granularity.

Consider the provided statements as a random sample, and try not to overfit, but build a solution that generealizes. 

## Target

Write a function that receives the path to a document (e.g., PDF file), and returns the three ratios below.

If time allows, try to include a confidence score and short comment for each calculated ratio (between 0% and 100%). 

An example response could look like the following (for inspiration only).

```json
{
    "equity_ratio": {
        "value": 0.3818,
        "confidence": 0.99,
        "comment": "All requried input values were provided unambiguously and could be used in the formula without error."
    },
    "acid_test_ratio": { [...] },
    "ebitda_margin": { [...] }
}
```

## Key Ratios:

### Equity Ratio​

Equity Ratio = (Equity / Total Assets) * 100​

of which:

- Equity: Share capital, retained earnings, reserve etc.​
- Assets: Sum of equity and liabilities (i.e. total capital)​

### Acid-Test Ratio​

Acid-Test Ratio = ( Cash and Cash Equivalents + Short-Term Receivables+ Marketable Securities) / Current
Liabilities * 100​

of which:

- Cash and Cash Equivalents: Includes physical cash, bank balances, and highly liquid investments.​
- Short-Term Receivables: Accounts receivable expected to be collected within 12 months.​
- Marketable Securities: Liquid financial instruments that can be quickly converted to cash.​
- Current Liabilities: Obligations due within one year (e.g., accounts payable, short-term loans).​

### EBITDA Margin​

EBITDA Margin = (EBITDA/Total Revenue) * 100​

of which:

- EBITDA: Earnings before interest, taxes, depreciation, and amortization

## Helpful literature

- [Schulkontenrahmen (Chart of Accounts in German)](https://www.kmu.admin.ch/dam/kmu/de/dokumente/savoir-pratique/Finances/240812%20Schulkontenrahmen%20VEB%20-%20DE.pdf.download.pdf/240812%20Schulkontenrahmen%20VEB%20-%20DE.pdf)
- [Equity Ratio](https://en.wikipedia.org/wiki/Equity_ratio)
- [Acid-Test Ratio](https://en.wikipedia.org/wiki/Quick_ratio)
- [EBITDA Margin](https://en.wikipedia.org/wiki/Earnings_before_interest,_taxes,_depreciation_and_amortization#Margin)