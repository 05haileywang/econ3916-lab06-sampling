# econ3916-lab06-sampling

Sampling for Machine Learning: Train-Test Splits
Objective

I studied how the way a sample is drawn affects model evaluation and estimate accuracy, using the Titanic dataset and a simulation of the 1936 Literary Digest polling failure.

Methodology
Explored the Titanic dataset (891 passengers) with survival as the target.
Compared a naive train-test split with a stratified one, and checked that stratifying keeps the survival rate the same in both halves.
Found and fixed data leakage in a StandardScaler step and a SimpleImputer step.
Wrote a function, split_by_share(), that splits a table given a test share and a seed, and checked it against the lab's own split.
Simulated the 1936 Literary Digest polling failure on 10 million voters.
Computed Meng's data defect correlation for a biased sample.
Compared the biased sample of 4,382,503 responses with a random sample of 50,000.
Ran 100 replications to compare the biased and random samples.
Key Findings
Stratifying the split kept the survival rate the same in the training and test sets.
Fitting the scaler and imputer before splitting leaked information from the test set. I fixed both.
Sample design beats sample size. The biased sample of 4,382,503 responses was less accurate than the random sample of 50,000.
A data defect correlation of 0.1475 produced an error of 8.3 percentage points.
