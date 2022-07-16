# Project Assessment

> 1.a For query classification: How many unique categories did you see in your rolled up training data when you set the minimum number of queries per category to 1000? To 10000?

For 1000 >> 376
For 10000 >> 59

> 1.b For query classification: What were the best values you achieved for R@1, R@3, and R@5? You should have tried at least a few different models, varying the minimum number of queries per category, as well as trying different fastText parameters or query normalization. Report at least 2 of your runs.

For default parameters >> R@1 0.484, R@3 0.637, R@5 0.7
For -epoch 25 -lr 0.5 -wordNgrams 2 >> R@1 0.52, R@3 0.7, R@5 0.769

> 2a. For integrating query classification with search: Give 2 or 3 examples of queries where you saw a dramatic positive change in the results because of filtering. Make sure to include the classifier output for those queries.

- `ipad`
without classifier only 4 out 10 results are iPads, the rest are accesoires
with category `pcmcat209000050007` all of the results are iPads

- `xbox`
without classifier only 1 out of 10 results is a console
with category `abcat0701001` all of the results are consoles

> 2b. For integrating query classification with search: Give 2 or 3 examples of queries where filtering hurt the results, either because the classifier was wrong or for some other reason. Again, include the classifier output for those queries.

- `nintendo`
without classifier 2 consoles and the rest are the games
with category `abcat0715016` only accesoires

- `powerbank`
without classifier 2 power supplies and one battery case
with category `abcat0811004` no results