This Repository consists of code for finetuning IndicBERT and IndicNER for Named Entity 
Recognition task in Telugu Language,over publicly available Naamapadam corpus of Telugu Language
with train 70%, 10% validation, and 20% test set splits.

And performing a comparison of Results between IndicBERT,IndicNER and ChatGPT over
Expert annotated 25 sentences using precision,recall and f1-score for each of them 
separately with the fine-tuned models predictions and expert annotated labels,
you can see them in the Comaprison folder

You can directly import Naamapadam dataset using Huggingface dataset,which you can 
find in the finetuning code itself.

You can find ChatGPT annotated data and Expert Annotated data in the data folder.

