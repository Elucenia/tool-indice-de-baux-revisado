<!-- ELUCENIA technical documentation · indice-de-baux-revisado · en · no clinical/professional/rights approval -->

# Revised Baux score

[conditions, sources and permissions](https://elucenia.org/en/tools/indice-de-baux-revisado)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Age

`idade`

years · range: 0–110

### Burned body surface area

`scq`

% · range: 0–100

### Inhalation injury?

`inalacao`

- `0` — No
- `1` — Yes

## Method edition

Revised Baux/Osler 2010: age+TBSA+17 inhalation injury; original logistic model

## Documented formula

Revised Baux = age (years) + TBSA burned (%) + 17 × inhalation injury (1=yes, 0=no).

In Osler’s model (39888 burn patients in the US registry), age and TBSA had almost equal weights; inhalation injury equalled 17 years or 17% TBSA. Death probability comes from logistic transformation of the score.

## Limits and population

The revised Baux sums age, percentage of burned area and 17 for inhalation injury. The raw total is not a mortality percentage: probability requires the version’s logistic transformation. The simplified model performed worse than the more complex model in the article and requires interpretation in the appropriate clinical population.

## References

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

The higher the score, the higher the predicted mortality; inhalation injury is equivalent to 17 years (or 17% of TBSA)

| Result details | |
| --- | --- |
| Classic Baux (age + TBSA) | 70 |
| Inhalation injury | +17 |

The classic Baux score was created as an estimate of mortality in %; with current treatment, this reading overestimates the risk.


### 2

The higher the score, the higher the predicted mortality; inhalation injury is equivalent to 17 years (or 17% of TBSA)

| Result details | |
| --- | --- |
| Classic Baux (age + TBSA) | 110 |
| Inhalation injury | no |

The classic Baux score was created as an estimate of mortality in %; with current treatment, this reading overestimates the risk.


### 3

The higher the score, the higher the predicted mortality; inhalation injury is equivalent to 17 years (or 17% of TBSA)

| Result details | |
| --- | --- |
| Classic Baux (age + TBSA) | 38 |
| Inhalation injury | no |

The classic Baux score was created as an estimate of mortality in %; with current treatment, this reading overestimates the risk.

