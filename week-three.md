# Project Assessment

> 1.a For query classification: How many unique categories did you see in your rolled up training data when you set the minimum number of queries per category to 1000? To 10000?

For 1000 >> 376
For 10000 >> 59

> 1.b For query classification: What were the best values you achieved for R@1, R@3, and R@5? You should have tried at least a few different models, varying the minimum number of queries per category, as well as trying different fastText parameters or query normalization. Report at least 2 of your runs.

For default parameters >> R@1 0.484, R@3 0.637, R@5 0.7
For -epoch 25 -lr 0.5 -wordNgrams 2 >> R@1 0.52, R@3 0.7, R@5 0.769

> 2a. For integrating query classification with search: Give 2 or 3 examples of queries where you saw a dramatic positive change in the results because of filtering. Make sure to include the classifier output for those queries.


> 2b. For integrating query classification with search: Give 2 or 3 examples of queries where filtering hurt the results, either because the classifier was wrong or for some other reason. Again, include the classifier output for those queries.

