# ICD 203 for Intelligence Analysis
["ICD 203"](https://www.dni.gov/files/documents/ICD/ICD%20203%20Analytic%20Standards.pdf) degrees of likelihood for intelligence analysis, in consumable form for reference.


## Terms of Likelihood

(a) For expressions of likelihood or probability, an analytic product must use one ofthe following sets ofterms

|  almost no chance   |  very unlikely   |  unlikely   |  roughly even chance   |  likely   |  very likely   |  almost certain(ly)   |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  remote   |  highly improbable   |  improbable (improbably)   |  roughly even odds   |  probable (probably)   |  highly probable   |  nearly certain   |
|  01 - 05 %   |  05 - 20 %   |  20 - 45 %   |  45 - 55 %   |  55 - 80 %   |  80 - 95 %   |  95 - 99 %   |

Analysts are strongly encouraged not to mix terms from different rows. Products that do mix terms must include a disclaimer clearly noting the terms indicate the same assessment of probability.

(b) To avoid confusion, products that express an analyst's confidence in an assessment or judgment using a "confidence level" (e.g., "high confidence") must not combine a confidence level and a degree of likelihood, which refers to an event or development, in the same sentence.

#### Code/data reference implementation (JSONic)

```python
icd203_likelihood = {
    "almost-no-chance": [1, 5],
    "very-unlikely": [5, 20],
    "unlikely": [20, 45],
    "roughly-even-chance": [45, 55],
    "likely": [55, 80],
    "very-likely": [80, 95],
    "almost-certain": [95, 99]
}
```

##### Credits
https://fas.org/irp/dni/icd/icd-203.pdf (text version)

code implementation based on https://github.com/deadbits/mimir/blob/7883a38774e1e3ce1c0acd7287b2a7bb21c20981/mimir/lib/scoring/levels.py

inspired by [SANS CTI 2020 talk "Stop Tilting at Windmills: Three Key Lessons that CTI Teams Should Learn from the Past"](https://www.sans.org/cyber-security-summit/archives/file/summit_archive_1579635728.pdf)

markdown table generated by https://atom.io/packages/markdown-table-editor
