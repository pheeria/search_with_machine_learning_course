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

```
iphone: 4s 0.869681, 3gs 0.806757, 3g 0.791568, apple 0.780217, ifrogz 0.775029, silicone 0.708414, belkin 0.696796, hardshell 0.678458, incase 0.67294, luxe 0.663057
headphones: earbud 0.862296, ear 0.842161, noise 0.774051, bud 0.773696, akg 0.718969, kicker 0.667051, sennheiser 0.664069,  skullcandy 0.662942, 2xl 0.660852, stereo 0.624376
laptop: laptops 0.663422, notebook 0.64583, netbook 0.532348, briefcase 0.525498, espresso 0.521515, processor 0.495462, 98 0.492725, sleeve 0.49085, macbook 0.484611, tucano 0.484576
```

> b. What fastText parameters did you use?

Epoch of 25 and minimum count of 20

> c. How did you transform the product names?

I re-used the dataset generated for classification. So, lowercased, removed non-alphanumeric characters and excessive whitespaces.

3. For integrating synonyms with search:

> a. How did you transform the product names (if different than previously)?

> b. What threshold score did you use?

> c. Were you able to find the additional results by matching synonyms?

4. For classifying reviews:

> a. What precision (P@1) were you able to achieve?

> b. What fastText parameters did you use?

> c. How did you transform the review content?

> d. What else did you try and learn?