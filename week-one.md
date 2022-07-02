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