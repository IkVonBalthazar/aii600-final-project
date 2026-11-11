# Decisions

This file is the history of the project. Append an entry when a choice changes the work: the quantity, the data, the split, the model, the loss, or the action. Leave old entries in place. A later entry can reverse an earlier one. If a result depends on a random draw, record the seed under Why. The split entry records the cutoff date, or the seed and the fraction. The pull request that merges the code names this entry.

## 2026-11-03: Proposal

- Decision. What you chose
-   I chose to use the UCI Phishing Websites dataset to develop a machine learning model that identifies phishing websites. I will compare a majority-class baseline, logistic regression, and a decision tree to determine which approach best helps cybersecurity analysts prioritize suspicious websites for human review.
- Why. The evidence.
-   The UCI dataset contains 11,055 website observations and 30 integer-valued features associated with phishing detection. It provides a suitable foundation for comparing machine learning models using historical website data. I chose this topic because phishing is a significant cybersecurity threat, and incorrectly classifying a phishing website as legitimate can expose users to credential theft and financial loss. I will primarily evaluate models using the number of false negatives per 1,000 websites tested.
- Alternative. What you rejected.
-   I considered using a live phishing website dataset or collecting website information independently. However, I rejected this approach because collecting and verifying live website data would introduce additional complexity and make the project more difficult to complete within the available time. The UCI dataset provides an established source of data with enough observations and features for this analysis.
- Revisit. What would change the choice.
-   I would reconsider my choice if the dataset contains significant data leakage, missing or unreliable information, or does not provide enough predictive value. I would also reconsider the approach if logistic regression and the decision tree perform no better than the majority-class baseline, or if their false-negative rates are too high for practical cybersecurity screening. Evidence from held-out test results, uncertainty estimates, and model comparisons will guide any changes.
