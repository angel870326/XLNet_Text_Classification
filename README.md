# XLNet Multi-class Text Classification for Chinese and English
* Available for both multi-label and single-label classification.
* Note: Example here is using Chinese pre-trained model, English pre-trained model is commented out.
* Codes are modified from [here](#3-multi-label-text-classification).

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

## 3. Multi-label Text Classification (important)
- Source: https://towardsdatascience.com/multi-label-text-classification-with-xlnet-b5f5755302df

## 4. XLNet Chinese Pre-trained Model (中文預訓練模型)
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

