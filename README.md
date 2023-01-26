# Hinglish_transformer

## Requirement 
We very often get feedback on our products and on field visits in Hinglish(we work in education in Indian states). Currently we use AI4Bharats  Fairseq transformers (combining hindi <-> English translation and transliteration) to carry out Hinglish sentence conversion to English for further use for aggregation, keyword analysis and sentiment analysis. 

An example of Hinglish sentence would be - 'Aapne achha flash card ke madyam se concept ko clear kiya hai. Aapko bachho ko aur adhik involve karna chiye' 

The general structure is that the sentence is in Hindi (written in Roman script) but some nouns (like flash card) are in English. 

We don't have a transformer that is trained on Hinglish sentences but rather Hindi <-> English transformers that we leverage  to carry out the same task. It's currently not very effective and efficient and we hope to build a transformer that is trained on Hinglish sentences to improve the performance.

There is no current thinking on the design of the architecture required for the task and the aim in general is not to have a high BLEU score in our first attempt at creating this.  

We want to build a pipeline first such that it allows one to train on Hinglish data and finetune the pretrained model on new datasets. 
Once the pipeline is set up, we will continue working on modifying the architecture to improve the accuracy. 

So far, we haven't found a big enough Hinglish data set to build an effective model and the current thinking is to leverage existing Hindi<-> English transformers to generate data to carry out the same.  We do have existing Hindi/English corpus datasets to do that. 
