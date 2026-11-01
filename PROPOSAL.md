# Proposal

At most one page. Replace the prompts under each heading. Leave the headings.

## Hypothesis

State the claim in one sentence. Then name the single quantity you will forecast or estimate, with its units and the time window.

A logistic regression model using features of websites will identify phishing websites more effectively than a simple majority-class baseline on held-out data. The quantity I will estimate is the number of phishing websites incorrectly classified as legitimate per 1,000 websites evaluated. I will measure this on a held-out test set from the historical dataset, not on a live stream of websites.

## Data

Name the source, the unit of observation, the sample size, the time span, and how the data were collected. Say how what you measure differs from the quantity the decision needs. Say whether the terms let you republish the files. A release asset is a republished copy. If the terms do not allow that, the files stay off GitHub and `data/README.md` gives the command that downloads them from the source.

I will use the UCI Phishing Websites dataset, which contains 11,055 website observations and 30 integer-valued features associated with phishing detection. Each observation represents a website described by features such as URL characteristics and other indicators of suspicious behavior. The dataset was assembled from historical website sources, including phishing archives and legitimate website directories. I will document the collection period as reported by the dataset metadata and inspect the data for missing values, class imbalance, and potential leakage before modeling. The dataset is available under the Creative Commons Attribution 4.0 license, which permits redistribution with attribution. I will cite the original dataset authors and follow the course repository's instructions for publishing data in a GitHub release tagged data.

## Decision affected by the model

Name who acts, and what they will do differently because of the prediction. Say which mistake costs more.

A cybersecurity analyst or security team could use the model's predictions to prioritize websites for human review. The goal would be to reduce the number of phishing websites that go undetected while limiting unnecessary warnings about legitimate websites. Missing a phishing website may expose users to credential theft or financial loss, so I expect false negatives to be more costly than false positives. I will compare a majority-class baseline with logistic regression and a decision tree, evaluate their performance on the same held-out test set, and use the estimated error rate and its uncertainty to assess whether the model is useful for this decision. The model will be treated as a screening aid rather than proof that a website is safe or malicious.
