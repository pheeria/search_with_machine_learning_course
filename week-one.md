# First week's project

## Project Assessment
> Do you understand the steps involved in creating and deploying an LTR model?  Name them and describe what each step does in your own words.

1. Decide whether you need ML at all. Probably not for non-ecommerce businesses or similar, where search doesn't drive the income.
2. Set up good tracking on queries, clicks, dwells, orders, filters and sorting.
3. Set up ratings and reviews.
4. Iteratively decide which features to rely on.
5. 


> What is a feature and featureset?

Feature is a field of document, seen as a dimension in the vector space.
Featureset is a set of features, an LTR model we train.

> What is the difference between precision and recall?

Precision and recall are conflicting forces, one usually coming at the cost of the other. Let me try to explain based on the food delivery industry.
Generally, ecommerce wants to improve the recall. If somebody searches for `McDonald's` and we don't have them nearby, it is probably ok to suggest them `Burger King` (using query expansion and/or synonyms). However, if somebody wants `halal meat`, we better serve them `halal` results (using query classification). This increases precision, however narrows the search scope, impacting the recall negatively.

> What are some of the traps associated with using click data in your model?

If we don't have the data about the results that *were not* clicked, the models we train will become biased. We can/should also collect and include the data when the customer decides to apply filters/sorting, being not satisfied with the results. 

> What are some of the ways we are faking our data and how would you prevent that in your application?

> What is target leakage and why is it a bad thing?

> When can using prior history cause problems in search and LTR?

> Submit your project along with your best MRR scores

My scores can be found in `week-one.md` in the repository: https://github.com/pheeria/search_with_machine_learning_course/blob/main/week-one.md 

## Initial approach

```
Simple MRR is 0.269
LTR Simple MRR is 0.269
Hand tuned MRR is 0.367
LTR Hand Tuned MRR is 0.372

Simple p@10 is 0.090
LTR simple p@10 is 0.088
Hand tuned p@10 is 0.162
LTR hand tuned p@10 is 0.158
Simple better: 61   LTR_Simple Better: 13   Equal: 956
HT better: 352      LTR_HT Better: 215      Equal: 570
```

## Set main score weight to zero

```
Simple MRR is 0.319
LTR Simple MRR is 0.136
Hand tuned MRR is 0.383
LTR Hand Tuned MRR is 0.145

Simple p@10 is 0.109
LTR simple p@10 is 0.055
Hand tuned p@10 is 0.180
LTR hand tuned p@10 is 0.061
Simple better: 763  LTR_Simple Better: 688  Equal: 11
HT better: 854      LTR_HT Better: 683      Equal: 14
```

## Add phrase match with slop

```
Simple MRR is 0.398
LTR Simple MRR is 0.226
Hand tuned MRR is 0.453
LTR Hand Tuned MRR is 0.230

Simple p@10 is 0.143
LTR simple p@10 is 0.100
Hand tuned p@10 is 0.200
LTR hand tuned p@10 is 0.103
Simple better: 847  LTR_Simple Better: 721  Equal: 16
HT better: 953      LTR_HT Better: 743      Equal: 17
```

## Add customer rating average and count
```
Simple MRR is 0.299
LTR Simple MRR is 0.375
Hand tuned MRR is 0.436
LTR Hand Tuned MRR is 0.387

Simple p@10 is 0.114
LTR simple p@10 is 0.169
Hand tuned p@10 is 0.202
LTR hand tuned p@10 is 0.182
Simple better: 480  LTR_Simple Better: 697  Equal: 10
HT better: 676      LTR_HT Better: 640      Equal: 19
```

## Add artist name, short and log descriptions

```
Simple MRR is 0.271
LTR Simple MRR is 0.450
Hand tuned MRR is 0.419
LTR Hand Tuned MRR is 0.467

Simple p@10 is 0.094
LTR simple p@10 is 0.165
Hand tuned p@10 is 0.203
LTR hand tuned p@10 is 0.180
Simple better: 348  LTR_Simple Better: 565  Equal: 10
HT better: 537      LTR_HT Better: 570      Equal: 18
```

## Add sales rank

```
Simple MRR is 0.303
LTR Simple MRR is 0.460
Hand tuned MRR is 0.391
LTR Hand Tuned MRR is 0.458

Simple p@10 is 0.102
LTR simple p@10 is 0.170
Hand tuned p@10 is 0.157
LTR hand tuned p@10 is 0.177
Simple better: 511  LTR_Simple Better: 663  Equal: 11
HT better: 621      LTR_HT Better: 672      Equal: 18
```