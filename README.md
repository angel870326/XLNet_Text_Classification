# XLNet Text Classification

## 1. Official XLNet
- Paper: https://paperswithcode.com/paper/xlnet-generalized-autoregressive-pretraining
- Code: https://github.com/zihangdai/xlnet

## 2. Hugging Face Transformers
- Source: https://github.com/huggingface/transformers
- XLNet doc: https://huggingface.co/transformers/v2.11.0/model_doc/xlnet.html
```
!pip install transformers
!pip install sentencepiece

tokenizer = XLNetTokenizer.from_pretrained('xlnet-base-cased', do_lower_case=True)
model = XLNetModel.from_pretrained('xlnet-base-cased')
```

## 3. Multi-label Text Classification
- Source: https://towardsdatascience.com/multi-label-text-classification-with-xlnet-b5f5755302df

## 4. XLNet 中文預訓練模型
- 資料來源：https://blog.csdn.net/ciacai/article/details/105008287
- 程式碼：https://github.com/ymcui/Chinese-XLNet
```
!pip install transformers
from transformers import AutoTokenizer, AutoModel

tokenizer = AutoTokenizer.from_pretrained("MODEL_NAME")
model = AutoModel.from_pretrained("MODEL_NAME")
```
|模型名|MODEL_NAME|
|---|---|
|XLNet-mid|hfl/chinese-xlnet-mid|
|XLNet-base|hfl/chinese-xlnet-base|

