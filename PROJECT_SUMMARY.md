# Project Summary

This summary presents the business question, analytical approach, and selected findings from the public portfolio version of the project. Supporting source materials and classroom-specific scaffolding are intentionally omitted.

## Executive Summary

This project analyzes whether patent abstract language contains useful signal about patent value. Using patent-level value estimates from the KPSS dataset and abstract text from USPTO patent grant records, the analysis builds text features and measures how specific words and phrases relate to patent value.

The results show that abstract language does contain some signal, but the strength of that signal is uneven. A small number of more technical terms, such as `test`, `processors`, and `chip`, are more positively associated with patent value, while many common terms have weak or near-zero relationships.

From a business analytics perspective, the project is useful because it shows how unstructured text can be converted into measurable features and linked to economically meaningful outcomes.

## Business Question

Can language in patent abstracts help explain differences in patent value?

This question matters because patents are both legal and economic assets. If abstract text captures meaningful signals about novelty, technical content, or commercial relevance, it may help support downstream research on innovation quality and firm value.

## Analytical Approach

- Loaded patent value data and filtered the sample to patents issued in 2022
- Merged in firm names using CRSP identifiers
- Parsed USPTO XML patent grant records and extracted abstract text
- Built a document-term matrix using unigram and bigram features
- Applied text preprocessing to keep lowercase alphabetic terms, remove stop words, and cap the vocabulary at 1,000 features
- Measured which terms were most common and which were most correlated with patent value (`xi_real`)

## Data Scope

The workflow combines three main inputs:

- KPSS patent value data
- CRSP-linked firm name data
- USPTO patent grant abstract text

The raw source files are not included in this public repository.

## Key Findings

### Firm-Level Result

The company with the highest average patent value in the 2022 sample is:

- **UNITEDHEALTH GROUP INC** with an average `xi_real` of **616.07**

### Frequently Used Terms

Common abstract terms include:

- `first`
- `second`
- `device`
- `data`
- `system`

### Terms More Positively Associated with Patent Value

Examples of stronger positive correlations include:

- `test`
- `processors`
- `provides`
- `processes`
- `chip`

### Terms More Negatively Associated with Patent Value

Negative correlations are weaker overall, with examples such as:

- `includes first`
- `unit`
- `first`
- `direction`

## Interpretation

The results suggest that text features extracted from patent abstracts contain some economically relevant signal, but they are far from a complete explanation of value. The most informative positive terms tend to be more technical, while many generic terms contribute little insight.

This pattern is consistent with a common analytics outcome: unstructured text can be informative, but signal quality depends heavily on feature specificity and the broader business context.

## Why This Matters

This project demonstrates how to connect text analytics with economic outcomes. That analytical pattern can transfer to many business settings, such as:

- product description analysis
- customer review analysis
- legal or compliance document screening
- innovation and R&D intelligence

The core value is not just text processing itself, but the ability to turn language into structured features and relate those features to a measurable target.

## Limitations

- The analysis uses one slice of time rather than a full longitudinal design
- Correlation does not imply causation
- Patent value likely depends on many firm, market, and industry factors not captured in the abstract alone
- Vocabulary-based methods can miss deeper semantic meaning

## Files

- `patent_value_text_analysis.ipynb`: notebook with the analysis workflow and outputs
- `requirements.txt`: Python dependencies
