# Document Classification using LLM

We are performing text classification using BERT.
BERT is a bidirectional transformer pretrained using a combination of masked language modeling objective and next sentence prediction on a large corpus comprising the Toronto Book Corpus and Wikipedia.

The dataset we used here is the 20 newsgroups text dataset. The 20 newsgroups dataset comprises around 18000 newsgroups posts on 20 topics split in two subsets: one for training (or development) and the other one for testing (or for performance evaluation). The split between the train and test set is based upon a messages posted before and after a specific date.
The twenty newsgroups can be seen as -
![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/85654e34-d3c2-4491-8a8c-84bee88a2de9)

An example of the text data seen in the dataset can be - 
![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/d11a9072-3397-4738-83e0-97be5eceb65e)

To run this code on Colab change the runtime to GPU and start execution.

1. Initially, we install all the required libraries
2. Then, we initialize the BERT Model and import all the required libraries related to BERT.
3. Next, we create all the training and testing datasets by splitting thr original dataset.
4. Next, we create the BERT embeddings for both the training and testing dataset from the text available and create datasets suitable for training. ![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/63c9fb64-aa92-492c-9e53-7b20903c2a55)
5. Next, we select accuracy and f1 score as the evaluation metric for both training process and testing process. ![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/a404913b-75dc-41e1-acef-cfde39b1b1a2)
6. We then select the BertForSequenceClassification model which is a Bert Model transformer with a sequence classification/regression head on top (a linear layer on top of the pooled output) e.g. for GLUE tasks and initilizae it with training arguments. ![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/604e6082-7b03-4479-830b-ce4e983dff9a)
7. Then, we use the metrics and arguments initialized in steps 5 and 6 and start training. We train for only 5 epochs. We can also train further to improve the accuracy and F1 score. The losses during training can be seen as - ![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/219d89f8-8895-40f0-88f9-6843c8790e6d)
8. After the completion of the text classification training, we then evaluate it on the test dataset. The accuracy and F1 score seen after training for five epochs is ~73.3%.![image](https://github.com/Ani1211999/DocumentClassificationusingLLM/assets/42744730/3cda0406-b6c5-4c70-afea-e28651a8f593)

