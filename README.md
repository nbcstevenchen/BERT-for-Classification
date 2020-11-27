# BERT-for-Classification

Some background knowledge:  
BERT can generate 2 kind of output: 1. two dimensional sequence_output(word embeddings) .  2. one dimensional pooled output(cls or sentence embedding) 
I recommend to use sequence_output of BERT(Many paper show that this is better than cls embedding).  
  
Python 3.6  
Required Library:  
PyTorch
transformers: pip install transformers
tensorflow2.0

I recommend to use Bert_classification_tf2.py or ipynb  
  
For tensorflow 2.0: Bert_classification_tf2.py or ipynb  
I implemented 3 models for fine-tuning BERT:  
1. create_model_sequence_output(trainable=True): create a fine-tune model that uses two dimensional sequence_output of BERT(word embeddings)  
2. create_model_cls_output(trainable=True): create a fine-tune model that uses one dimensional pooled output(cls or sentence embedding)  
3. create_model_2(trainable=True): as same as create_model_cls_output(trainable=True)  
if trainable=True: --> the weights of pre-trained BERT will also be adjusted during fine-tuning.  
if trainable=False: --> the weights of pre-trained BERT will not be adjusted during fine-tuning.  



For pytorch: Bert_classification_pytorch.py or ipynb  
I only implemented 1 model for fine-tuning BERT: create a fine-tune model that uses one dimensional pooled output(cls or sentence embedding)  
  
I put the example codes inside each python file. I used part of data in IMDB datatset as an example.
