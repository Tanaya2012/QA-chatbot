# QA-chatbot
This GitHub repository focuses on developing a QA chatbot through the use of open-source models, specifically utilizing either Retrieval Augmented Generation or fine-tuning techniques. The repository includes code and a provided dataset for implementing this project. It can automatically find answers to matching questions directly from documents. The dataset is retrieved from the following link:
https://www.cdc.gov/vaccines/hcp/acip-recs/vacc-specific/hpv.html

## Approches
* Question Answering System Using Simple Split and Cosine Similarity
* Question Answering System Using Word2Vec Embedding Technique
* Question Answering System with Fine-Tuned BERT Technique
* Question Answering System Using Retrieval Augmented Generation 

## Challenges
* Text extracted from pdf documents. I extracted the text from a PDF document that contained data organized in two columns. To ensure relevance and accuracy, I implemented a filtering process to remove any unnecessary information or extraneous content. This resulted in a refined and streamlined dataset suitable for further analysis or processing tasks.
* Bert is a really powerful model for tackling a question-answering problem. However, it comes up with the limitation of 512 tokens and the documents were really longer than 512 tokens. In order to handle this limitation the whole text was divided into tokens of size 512 and the best answer was taken as the final answer
* For training BERT, I created a question-answer dataset by extracting text from the PDF documents and using it to fine tune BERT. This dataset can be used for various natural language processing tasks, including question answering and text comprehension.

## Pretrained Model and Dataset Used
* word2vec
* bert-large-uncased-whole-word-masking-finetuned-squad
* distilbert-base-uncased-distilled-squad
* ms-marco-MiniLM-L-12-v2
* LaMini-Flan-T5-783M

## Results
The best generated answers for the given questions were using Retrieval Augmented Generation which were as follows:
* Question:  When did the GARDASIL 9 recommendations change?
  Answer:  The GARDASIL 9 recommendations changed in February 2015.
* Question:  What were the past 3 recommendation changes for GARDASIL 9?
  Answer:  The Acip advisory committee on immunization practices recommended GARDASIL 9 as one of three HPV vaccines that can be used for routine vaccination.
* Question:  Is GARDASIL 9 recommended for Adults?
  Answer:  The context does not provide information on whether GARDASIL 9 is recommended for adults.
* Question:  Does the ACIP recommend one dose GARDASIL 9?
  Answer:  The ACIP recommends one dose of GARDASIL 9 as one of three HPV vaccines that can be used for routine vaccination.
