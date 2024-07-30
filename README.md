This Repository consists of code for finetuning IndicBERT and IndicNER for Named Entity 
Recognition task in Telugu Language,over publicly available Naamapadam corpus of Telugu Language.You can directly import Naamapadam dataset using Huggingface dataset,which you can 
find in the finetuning code itself.
with train 70%, 10% validation, and 20% test set splits.You can find ChatGPT annotated data and Expert Annotated data in the data folder.

And performing a comparison of Results between IndicBERT,IndicNER and ChatGPT over
Expert annotated 25 sentences using precision,recall and f1-score for each of them 
separately with the fine-tuned models predictions and expert annotated labels,
you can see them in the Comaprison folder
The results are:
For IndicNER:
  - Macro Precision: 0.20931908834635435
  - Macro Recall: 0.19763993960247306
  - Macro F1-score: 0.20037437048556733  

For ChatGPT:
  - Macro Precision: 0.3245192307692308
  - Macro Recall: 0.19300768813691277
  - Macro F1-score: 0.20940091727858176
    
For IndicBERT:
  - Macro Precision: 0.3923867974500886
  - Macro Recall: 0.3443784924688974
  - Macro F1-Score: 0.3629307783719548

Analyzing the comparison:
- Compared with all the models above,IndicBERT seem to perform
better than IndicNER and ChatGPT.
- Possible reasons for this :
  1. Pre-training on Large Corpora: BERT-based models like IndicBERT are pre       
     trained on large corpora of text, which allows them to capture a wide range 
     of linguistic patterns and semantic relationships. This pre-training helps
     in extracting features relevant to NER tasks effectively.
  2. Fine-tuning: IndicBERT is fine-tuned specifically for NER tasks
     on Indic languages. Fine-tuning allows the model to adapt its
     parameters to the specific characteristics and nuances of the task and             language, leading to better performance.
  3. Contextual Embeddings: BERT-based models generate contextual embeddings for        each token in a sentence, taking into account the surrounding words. This     
     contextual understanding is crucial for NER tasks, as the presence of named   
     entities often depends on the context in which they appear.
- Chat GPT by default assuming most of the tags for tokens to be “O”.
- MISC labels are mostly missed by all the above model.But they
are actually present as told in expert annotated NER labels.
