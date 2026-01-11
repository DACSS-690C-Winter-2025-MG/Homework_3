# AHP School Selection Analysis

## Overview

This Python script performs an **Analytic Hierarchy Process (AHP)** analysis to help decide between three schools (**A, B, C**) based on multiple criteria.

HTML File Output: https://dacss-690c-winter-2025-mg.github.io/Homework_3/GoogleColabCodeHW3.html

## Criteria

The analysis evaluates schools based on six criteria:

* **Learning** – Academic quality and learning environment
* **Friends** – Social opportunities and peer relationships
* **School Life** – Overall school culture and activities
* **Vocational Training** – Career preparation and vocational programs
* **College Prep** – College readiness and preparation
* **Music Classes** – Music education opportunities

## Requirements

* Python 3.x
* pandas
* numpy
* networkx
* ahpy

Install dependencies with:

```bash
pip install pandas numpy networkx ahpy
```

## Data File Setup

Your Excel file must contain **7 sheets** (all **lowercase** names):

* `learning` – Pairwise comparisons of schools A, B, C for learning
* `friends` – Pairwise comparisons for friends criterion
* `schoollife` – Pairwise comparisons for school life
* `vocational` – Pairwise comparisons for vocational training
* `college` – Pairwise comparisons for college prep
* `music` – Pairwise comparisons for music classes
* `criteria` – Pairwise comparisons between the six criteria themselves

Each sheet should be a **square matrix** with schools (**A, B, C**) as both rows and columns, containing pairwise comparison values.

## How to Use

1. Prepare your Excel file with all required pairwise comparisons
2. Update the GitHub link in the script
3. Run the script
4. Review the output:

   * Criteria weights (which factors matter most)
   * Final school rankings with scores
   * Consistency ratios (should be **< 0.1**)

## Output

The script provides:

* **Criteria Weights** – Shows the relative importance of each criterion
* **School Rankings** – Final scores and ranking of schools A, B, C
* **Consistency Check** – Validates that your comparisons are logically consistent
* **Recommendation** – The best school choice based on your priorities

## Troubleshooting

* **Empty comparisons error**: Ensure all sheets contain valid pairwise comparison data
* **Consistency ratio > 0.1**: Review and revise comparisons for logical consistency
* **Missing sheets**: Confirm that all 7 sheets exist and use exact lowercase names

## AHP Comparison Scale

When filling in comparisons, use the following scale:

* 1 = Equal importance
* 3 = Moderate importance
* 5 = Strong importance
* 7 = Very strong importance
* 9 = Extreme importance
* 2, 4, 6, 8 = Intermediate values

## Example

If **Learning** is **5 times more important** than **Music Classes**, enter:

* `5` in the (Learning, Music) cell
* `1/5` (0.2) in the (Music, Learning) cell

