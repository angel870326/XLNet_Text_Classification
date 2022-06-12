# XLNet Multi-class Text Classification for Chinese and English
* Available for both multi-label and single-label classification.
* Note: Example here is using Chinese pre-trained model. English pre-trained model is commented out.
* Codes are modified from [here](#3-multi-label-text-classification-important).

## User Guide
1. To evaluate our model, we first split the training dataset into training and testing part.<br/> ```train_test_split_v2.ipynb```
2. Use the training part to train the model and the testing part to evaluate the model. (Do any modification until you get a satisfying score.)
   - For **single-label** testing, you may use **"Cross Entropy Loss Function"**: <br/> ```product/xlnet_multi_class_chinese_train_product_single_label_ce_oversample.ipynb```
   - For **multi-label** testing, you may use **"Binary Cross Entropy with Logits Loss Function"**: <br/>```product/xlnet_multi_class_chinese_train_product_single_label_bcel.ipynb```
3. Use the complete training dataset to train the model, and predict classes of a new dataset (answer unknown).<br/> ```.ipynb```


## Reference
### 1. Official XLNet
- Paper: https://paperswithcode.com/paper/xlnet-generalized-autoregressive-pretraining
- Code: https://github.com/zihangdai/xlnet

### 2. Hugging Face Transformers
- Source: https://github.com/huggingface/transformers
- XLNet doc: https://huggingface.co/transformers/v2.11.0/model_doc/xlnet.html
```
!pip install transformers
!pip install sentencepiece

tokenizer = XLNetTokenizer.from_pretrained('xlnet-base-cased', do_lower_case=True)
model = XLNetModel.from_pretrained('xlnet-base-cased')
```

### 3. Multi-label Text Classification (important)
- Source: https://towardsdatascience.com/multi-label-text-classification-with-xlnet-b5f5755302df

### 4. XLNet Chinese Pre-trained Model (中文預訓練模型)
- 資料來源：https://blog.csdn.net/ciacai/article/details/105008287
- 程式碼：https://github.com/ymcui/Chinese-XLNet

可以直接透過 transformers 使用
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


## Prevent Google Colab from Disconnecting
Right click ➡ Inspect ➡ Console
```
function ConnectButton(){
    console.log("Connect pushed");
    document.querySelector("#top-toolbar > colab-connect-button").shadowRoot.querySelector("#connect").click()
}
setInterval(ConnectButton,60000);
```
