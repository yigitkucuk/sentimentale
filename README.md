---
tags:
- text-classification
language:
- en
widget:
- text: "Oh, the tragedy!"
datasets:
- yigitkucuk/sentimentale-dataset
co2_eq_emissions:
  emissions: 0.7402856123778213
---

## Validation Metrics

- Loss: 0.576
- Accuracy: 0.827
- Macro F1: 0.711
- Micro F1: 0.827
- Weighted F1: 0.827
- Macro Precision: 0.708
- Micro Precision: 0.827
- Weighted Precision: 0.828
- Macro Recall: 0.716
- Micro Recall: 0.827
- Weighted Recall: 0.827
- Problem type: Multi-class Classification
- CO2 Emissions (in grams): 0.7403
- Model ID: 3099088026

## Use with Python API

```
from transformers import AutoModelForSequenceClassification, AutoTokenizer

model = AutoModelForSequenceClassification.from_pretrained("yigitkucuk/Sentimentale", use_auth_token=True)

tokenizer = AutoTokenizer.from_pretrained("yigitkucuk/Sentimentale", use_auth_token=True)

inputs = tokenizer("Oh, the tragedy!", return_tensors="pt")

outputs = model(**inputs)
```
