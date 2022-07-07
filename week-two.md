# Project Assessment

1. For classifying product names to categories:

> a. What precision (P@1) were you able to achieve?

```
N       10000
P@1     0.968
R@1     0.968
```

> b. What fastText parameters did you use?

Learning Rate of 1.0, epoch of 25 and word n-grams of 2

> c. How did you transform the product names?

Lowercase, remove non-alphanumeric characters and remove excessive whitespaces

> d. How did you prune infrequent category labels, and how did that affect your precision?

Grouped and only trained categories having more than 500 products

> e. How did you prune the category tree, and how did that affect your precision?

I didn't do that part.

2. For deriving synonyms from content:

> a. What were the results for your best model in the tokens used for evaluation?

> b. What fastText parameters did you use?

> c. How did you transform the product names?

3. For integrating synonyms with search:

> a. How did you transform the product names (if different than previously)?

> b. What threshold score did you use?

> c. Were you able to find the additional results by matching synonyms?

4. For classifying reviews:

> a. What precision (P@1) were you able to achieve?

> b. What fastText parameters did you use?

> c. How did you transform the review content?

> d. What else did you try and learn?