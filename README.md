# Patent Text and Patent Value Analysis

This repository is a public portfolio version of a patent analytics project that studies whether vocabulary in patent abstracts is associated with patent value.

The analysis combines patent-level value estimates from the KPSS dataset with USPTO patent grant abstracts. The notebook filters the sample to 2022 patents, merges firm identifiers, builds a document-term matrix, and measures which words and phrases are most correlated with patent value.

For a concise project overview written for portfolio review, see `PROJECT_SUMMARY.md`.

## Portfolio Version Note

This public version focuses on methodology, code structure, and selected results. Original source materials, raw datasets, and classroom-specific scaffolding are intentionally omitted.

## Highlights

- Filters KPSS patent value data to patents issued in 2022
- Merges in firm names from CRSP identifiers
- Parses USPTO XML records and extracts patent abstracts
- Builds unigram and bigram text features with `CountVectorizer`
- Examines the most common terms in patent abstracts
- Measures term-by-term correlations with `xi_real`

## Selected Findings

- Highest average patent value in the 2022 sample: **UNITEDHEALTH GROUP INC**
- Frequently used abstract terms include `first`, `second`, `device`, `data`, and `system`
- Stronger positive term correlations include `test`, `processors`, `processes`, and `chip`
- Negative term correlations are present but much weaker in magnitude

## Repository Contents

- `patent_value_text_analysis.ipynb`: cleaned notebook with methodology, code, and selected outputs
- `PROJECT_SUMMARY.md`: concise summary of the business question, analytical approach, and key results
- `requirements.txt`: Python dependencies used in the analysis

## Data Note

The raw datasets are not included in this repository. The original workflow expects access to:

- `KPSS_2023.csv`
- `crsp_names.csv`
- `ipg221213.zip`

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
