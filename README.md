# Patent Text and Patent Value Analysis

This repository is a public portfolio version of a patent analytics project that studies whether vocabulary in patent abstracts is associated with patent value.

## Public Portfolio Note

This repository is a portfolio adaptation of a larger academic analysis. It includes selected code, outputs, and summary materials for portfolio review. Raw source data, classroom-specific scaffolding, and non-essential work products are intentionally omitted, and the repository is not intended as a step-by-step instructional solution.

## Project Overview

This project analyzes whether language in patent abstracts can help explain differences in patent value by combining patent-level value estimates with USPTO abstract text.

## Business Problem

Patents are both legal assets and economic assets, so firms, investors, and innovation teams care about how to evaluate their quality at scale. If abstract language contains useful signal about novelty, technical depth, or commercial relevance, text can become a practical input in broader innovation and patent-evaluation workflows.

## Data

- Source: KPSS patent value estimates, CRSP-linked firm-name mapping data, and USPTO patent grant XML files
- Type: unstructured patent text plus structured firm and value data
- Included here: the portfolio notebook and summary materials
- Not included: the raw source files used in the original workflow

## Approach

- Filtered the patent-value sample to patents issued in 2022
- Merged in firm identifiers and names
- Parsed USPTO XML grant files and extracted abstract text
- Built a document-term matrix with unigram and bigram features
- Measured which terms were most frequent and which were most correlated with patent value

## Key Insights

- Patent abstract text contains some useful signal, but the signal is uneven
- More technical terms such as `test`, `processors`, and `chip` were more positively associated with patent value
- Many generic abstract terms contributed little explanatory value
- Text helped explain part of the variation in patent value, but it was far from a complete explanation on its own

## Recommendations

- I would use text-derived features as a supplemental input in patent screening rather than as a standalone valuation tool
- I would pay more attention to technically specific language than to broad generic wording
- I would combine abstract-text features with richer firm, market, and industry variables for a stronger decision workflow

## Start Here

- `PROJECT_SUMMARY.md`: main case-study style overview
- `patent_value_text_analysis.ipynb`: selected analysis notebook

## Repository Contents

- `patent_value_text_analysis.ipynb`: selected notebook with methodology, code, and outputs
- `PROJECT_SUMMARY.md`: detailed project narrative with business framing, approach, findings, and limitations
- `requirements.txt`: Python dependencies used in the analysis

## Data Note

The raw datasets are not included in this repository. The underlying workflow combines patent value estimates, firm-name mapping data, and USPTO patent grant XML files containing abstract text.

## Local Reproduction

Install dependencies:

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_lg
```

Then open:

- `patent_value_text_analysis.ipynb`

## Skills Demonstrated

- text preprocessing
- document-term matrix construction
- XML parsing
- data merging and wrangling
- exploratory text analytics
- feature-value correlation analysis
