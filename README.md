# mentBERT
This fine-tuned BERT model is able to predict different mental disorders from written texts that people have written about themselves and their general experience.

# Description
https://huggingface.co/reab5555/mentBERT   
   
This model is a finetuned BERT (bert-base-uncased) model that predict different mental disorders.   
* It is trained on a costume dataset of texts or posts (from Reddit) about general experiences of users with mental health problems.   
* Dataset was cleaned and all direct mentions of the disorder names in the texts were removed.     
    
It includes the following classes:   

* Borderline
* Anxiety
* Depression
* Bipolar
* OCD
* ADHD
* Schizophrenia
* Asperger
* PTSD

# Training
Train size: 90%   
Val size: 10%   
   
Training set class counts (text samples) after balancing:   
Borderline:       10398   
Anxiety:          10393   
Depression:       10400   
Bipolar:          10359   
OCD:              10413   
ADHD:             10412   
Schizophrenia:    10447   
Asperger:         10470   
PTSD:             10489   
   
Validation set class counts after balancing:   
Borderline:       1180   
Anxiety:          1185   
Depression:       1178   
Bipolar:          1219   
OCD:              1165   
ADHD:             1166   
Schizophrenia:    1131   
Asperger:         1108   
PTSD:             1089   

   
model-finetuning: bert-base-uncased

The following hyperparameters were used during training:   
   
learning_rate: 5e-05   
train_batch_size: 32   
val_batch_size: 32   
optimizer: AdamW   
num_epochs: 2-3   

# Training results
| Epoch | Training Loss | Validation Loss |
|-------|---------------|-----------------|
| 1.0   | 0.2089        | 0.1771          |
| 2.0   | 0.1525        | 0.1716          |

F1 Score: 0.6797   
AUC Score: 0.7942   

## Classification Report
Borderline:   
 Precision: 0.6682   
 Recall: 0.5923    
 F1-score: 0.6280   
    
Anxiety:   
 Precision: 0.6620    
 Recall: 0.6497    
 F1-score: 0.6558    
    
Depression:   
 Precision: 0.7261  
 Recall: 0.5424   
 F1-score: 0.6209   
    
Bipolar:   
 Precision: 0.8055   
 Recall: 0.5233   
 F1-score: 0.6345   
    
OCD:   
 Precision: 0.8200   
 Recall: 0.6532   
 F1-score: 0.7271   
   
ADHD:   
 Precision: 0.8740   
 Recall: 0.6603   
 F1-score: 0.7523   
    
Schizophrenia:   
 Precision: 0.8017   
 Recall: 0.6472   
 F1-score: 0.7162   
    
Asperger:   
 Precision: 0.7368   
 Recall: 0.6570   
 F1-score: 0.6946   
    
PTSD:    
 Precision: 0.8612   
 Recall: 0.5812   
 F1-score: 0.6940   
