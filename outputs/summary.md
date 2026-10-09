# Titanic: introductory descriptive analysis

The analysis uses 891 training passengers with observed survival outcomes.
Overall, 342 survived (38.4%).
The 418 test passengers have no observed survival outcomes; the sample submission
is an example output, not ground truth. Neither supplies outcomes for this analysis.

## Missing values

- train.csv, Age: 177 missing (19.9%).
- train.csv, Cabin: 687 missing (77.1%).
- train.csv, Embarked: 2 missing (0.2%).
- test.csv, Age: 86 missing (20.6%).
- test.csv, Fare: 1 missing (0.2%).
- test.csv, Cabin: 327 missing (78.2%).

All other columns have zero missing values. Survived, Pclass, and Sex are complete
in the training data, so all training passengers contribute to these survival rates.
No missing values were filled, and no rows were dropped.

## Survival rates

Each rate is survivors divided by passengers in that group, multiplied by 100.
For a binary 0/1 outcome this is also the group's mean of Survived, multiplied by 100.

| Pclass | Passengers | Survivors | Survival rate |
| --- | --- | --- | --- |
| 1 | 216 | 136 | 63.0% |
| 2 | 184 | 87 | 47.3% |
| 3 | 491 | 119 | 24.2% |

| Sex | Passengers | Survivors | Survival rate |
| --- | --- | --- | --- |
| female | 314 | 233 | 74.2% |
| male | 577 | 109 | 18.9% |

The joint groups help inspect how the two recorded characteristics overlap:

| Pclass | Sex | Passengers | Survivors | Survival rate |
| --- | --- | --- | --- | --- |
| 1 | female | 94 | 91 | 96.8% |
| 1 | male | 122 | 45 | 36.9% |
| 2 | female | 76 | 70 | 92.1% |
| 2 | male | 108 | 17 | 15.7% |
| 3 | female | 144 | 72 | 50.0% |
| 3 | male | 347 | 47 | 13.5% |

## Observed associations and limitations

In this sample, survival was higher in first class (63.0%) than second
(47.3%) or third (24.2%). Passengers recorded as female had a
higher survival rate (74.2%) than those recorded as male (18.9%).
These are descriptive associations, not evidence that class or sex caused survival.
The separate group rates do not adjust for age, family circumstances, or other factors;
the joint table is still descriptive. Group sizes differ, and this workshop training
sample may not represent all Titanic passengers or other populations. Missing age
and cabin data limit broader comparisons. No uncertainty intervals or significance
tests were calculated, and the dataset's binary Sex labels limit the categories described.
No predictive model was trained by this analysis.

The two charts label axes, percentages, and group passenger counts; they show observed
proportions rather than predictions.
