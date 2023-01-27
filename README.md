---
tags:
- autotrain
- text-classification
language:
- en
datasets:
- yigitkucuk/poem-sentimentale-dataset
---

# Model

- Problem type: Multi-class Classification
- Model ID: 3099088026

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


## Usage

You can use cURL to access this model:

```
$ curl -X POST -H "Authorization: Bearer YOUR_API_KEY" -H "Content-Type: application/json" -d '{"inputs": "I love AutoTrain"}' https://api-inference.huggingface.co/models/yigitkucuk/Poem-Sentimentale
```

Or Python API:

```
from transformers import AutoModelForSequenceClassification, AutoTokenizer

model = AutoModelForSequenceClassification.from_pretrained("yigitkucuk/Poem-Sentimentale", use_auth_token=True)

tokenizer = AutoTokenizer.from_pretrained("yigitkucuk/poem-sentimentale-dataset", use_auth_token=True)

inputs = tokenizer("I love AutoTrain", return_tensors="pt")

outputs = model(**inputs)
```
