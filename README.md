# Patent Text and Patent Value Analysis

This repository is a public portfolio version of a patent analytics project that studies whether vocabulary in patent abstracts is associated with patent value.

The analysis combines patent-level value estimates with USPTO patent grant abstracts and asks whether text features from abstracts can help explain patent value.

## Public Portfolio Note

This repository is a portfolio adaptation of a larger academic analysis. It includes selected code, outputs, and summary materials for portfolio review. Raw source data, classroom-specific scaffolding, and non-essential work products are intentionally omitted, and the repository is not intended as a step-by-step instructional solution.

## Start Here

- `PROJECT_SUMMARY.md`: main case-study style overview
- `patent_value_text_analysis.ipynb`: selected analysis notebook

## At a Glance

- Business question: can patent abstract language help explain patent value?
- Methods: XML parsing, text preprocessing, document-term matrix construction, and term-level correlation analysis
- Headline takeaway: a small set of more technical terms appears more informative than generic abstract language, but text alone does not fully explain patent value

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
