# cmu-volleyball-ml
A linear regression project using Carnegie Mellon University women's volleyball match data from the 2025–26 season ([CMU Athletics game log](https://athletics.cmu.edu/sports/wvball/2025-26/teams/carnegiemellon?view=gamelog)).

**Question:** Do passing stats predict how efficiently CMU hits in a match?

- **Target:** team hitting percentage per match
- **Features:** reception errors, receptions, and digs, normalized per set so 3-set and 5-set matches are comparable
- **Model:** linear regression (scikit-learn), evaluated with a held-out test set and 5-fold cross-validation

## Key Findings
1. **R2 from a single split was misleading.** After removing leakage, one 80/20 split gave R² = 0.15, but 5-fold cross-validation gave an average R² of −0.04 (± 0.15).
3. **Conclusion:** With one season (36 matches), passing and defense stats alone don't reliably predict match hitting efficiency.

## Next Steps
- Combine multiple seasons for more data
- Use logistic regression to explore what separates wins from losses

## Files
- `CMU_Vball_Linear_Regression.ipynb`: analysis notebook (click "Open in Colab" to run it)
- `CMU 2025-26 Volleyball Game Log - Sheet1.csv`: match data

## Tools
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Google Colab

*Built after an introductory machine learning workshop, adapted from [Carpentries: Introduction to Machine Learning with Scikit-Learn](https://carpentries-incubator.github.io/machine-learning-novice-sklearn/index.html).*
