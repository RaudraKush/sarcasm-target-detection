# Sarcasm-Target-Detection

The repository contains the implementation of EMNLP-2019 submission : 'A deep-learning framework to detect sarcasm targets'.

**Data Set**:

Original Dataset : https://github.com/Pranav-Goel/Sarcasm-Target-Detection

The **dataset.csv** file contains snippets(book_text) and probable targets.
It is then preprocessed and whose output is present in **pre_processed_dataset.csv** file which contains 4 columns:
1. left_context - set of words to the left of the probable sarcasm target
2. right_context - set of words to the right of the probable sarcasm target
3. candidate_words - probable sarcasm target 
4. target_status - 1(sarcasm target), 0(not a sarcasm target)  

The **Data_preparation.ipynb** file does the embedding of the left_context, right_context and candidate_words based on preloaded embeddings contained in file **crawl-300d-2M.vec**.
The **crawl-300d-2M.vec** file can be downloaded from https://fasttext.cc/docs/en/english-vectors.html
These features are dumped in a pickle file.

The **Socio_Linguistic_Feature_Extraction.ipynb** file  extracts the POS, NER, Empath features using the Standford NER API and Standford POS API. 

The empath is a python module. So please install the module.

These two files can be downloaded from below links:

1.Standford NER API: https://nlp.stanford.edu/software/CRF-NER.html#Download (3.9.2 version is used in this code)

2.Standford POS API: https://nlp.stanford.edu/software/tagger.shtml (3.9.2 version is used in this code)

These output features are dumped in a pickle file.

The **Model.ipynb** file does the training and k-cross validation of the features extracted from the previous file.

***References***:

Original Code: https://github.com/Srijanb97/Sarcasm_Target_Detection-EMNLP-

Original Dataset: https://github.com/Pranav-Goel/Sarcasm-Target-Detection

This repository contains the implementation of EMNLP-2019 submission : '**A deep-learning framework to detect sarcasm targets**'.
