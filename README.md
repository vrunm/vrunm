### Hi, I am **Varun**!
NLP developer working in the enhancement and development of applications based on Large Language Models (LLMs).

Some of the projects I have worked on:

**Retrieval Augmented Generation (RAG) using LLMs for Earnings Call Transcripts**
 - Built a pipeline to perform open-ended question-answering on earnings call transcripts using Generative Large Language Models (LLMs). The pipeline can answer questions on information present
 directly in a transcript, as well as combine information from multiple transcripts to answer indirect questions.
 - Earnings calls are a critical source of information for institutional investors, helping them make better investment decisions. The transcripts of these calls are voluminous, generated every quarter, and difficult to parse and correlate. Hence, extracting actionable information from multiple transcripts is extremely crucial.
 - The pipeline uses Retrieval Augmented Generation (RAG) to incorporate new information, and does not require retraining the Generative LLMs. The pipeline consists of an Embedding LLM, Context
 Retriever, Prompt Generator and a Generative LLM. RAG retrieves data from outside the model, and augments the prompts by adding the retrieved data in-context. This allows for easy attribution and minimal hallucination.
 - The pipeline first pre-processes the transcripts, and text snippets are extracted from each section of the earnings call. The text snippets are chunked dynamically based on text similarity. This is done so that each chunked snippet is less than 512 tokens, and accurate embeddings can be created from the text snippets.
 - The pipeline next creates an embedding for each chunk, and stores these embeddings in a Pinecone vector database. We experimented with the following SOTA embedding models: SBERT, MPNET, SGPT and INSTRUCTOR. The INSTRUCTOR model generated embeddings which resulted in the best context retrieval.
 - The embeddings are retrieved from the Vector Database, and used as context to the open-ended questions. The context is passed along with the question to the generative LLM for generating an accurate and concise answer to the question.
 - Compared different strategies for context retrieval, including dense embedding retrieval and hybrid retrieval. A combination of both strategies gave the best results.
 - Created different prompt templates for entity extraction and question-answering. We used ideas from the templates used in LLM frameworks like Langchain, Llama Index, OpenPrompt, and Promptify.
 - Weak supervision techniques based on the AMA paper by the Hazy Research Lab at Stanford were used to improve the prompts for extracting the entities and dynamically generating few-shot examples.
 - Carried out extensive prompt tuning by iteratively refining prompt formatting, instructions and incorporating few-shot examples. Semantic Search was used to dynamically retrieve similar few-shot examples for better text generation performance. Detailed instructions were added to ensure the LLM uses the context effectively and generates coherent text.
 - Experimented with the following instruction-tuned generative LLMs for generating answers: Llama-2, Vicuna, Alpaca, Dolly, FLAN-T5 and GPT-3. The Llama-2 and GPT-3 LLMs generated the most
 accurate and concise answers.
 - Tuned the text generation hyperparameters: Temperature, Top-p, Top-k, and Max-Length to improve generation performance and evaluated the generated answers on Coverage, Redundancy, and
 Hallucination. This helped quantitatively compare text generation performance while making sure the generation was accurate.


**A comparison of Hyperparameter Tuning and Optimizer Selection on Training Efficiency and LLM Performance:**

- **[Question Answering on the Squad Dataset:](https://github.com/vrunm/Question-Answering-Squad)**
Built a Question Answering system for News Articles.
For the SQuAD dataset, a baseline was set using the BERT model. The BERT model was fine-tuned using an AdamW optimizer with learning rate of 5e-5, and a batch-size of 32. The DistilBERT and RoBERTa models were also fine-tuned using an AdamW optimizer with learning rate of 5e-5 and a batch-size of 32. The models were trained for 6 epochs each. The performance of the model was evaluated on the basis of F1-Score(Weighted) on the test set. The RoBERTa model achieved the best performance on the SQuAD dataset.
A comparative study of different optimizers used for training was done. The optimizers were tuned for different parameters by a specific way of search spaces. Each parameter was first tuned on a large search space, and then a smaller and more refined search space was used to find the optimal value for training the model.


- **[Text Summarization News Articles:](https://github.com/vrunm/Text-Summarization-News-Articles)**
Built a summarization model that gives short and concise summaries for News Articles.
For the Multi-News dataset, a baseline was set using the BART model. The BART model was fine-tuned using an AdamW optimizer with learning rate of 2e-5, and a batch-size of 32. The
DistilBART model was also fine-tuned using an AdamW optimizer with learning rate of 2e-5 and a batch-size of 32. The model were trained for 6 epochs each. The performance of the model was evaluated on the basis of the ROUGE-1, ROUGE-2 and ROUGE-L scores on the test set. The DistilBART model achieved the best performance on the Multi-News dataset.
A comparative study of different optimizers used for training was done. The optimizers were tuned for different parameters by a specific way of search spaces. Each parameter was first tuned on a large search space, and then a smaller and more refined search space was used to find the optimal value for training the model.

- **[Sentiment Analysis For Financial News Articles:](https://github.com/vrunm/Text-Classification-Financial-Phrase-Bank)**
Built a sentiment analysis model to predict the sentiment of a Financial News article.
For the Financial PhraseBank dataset, a baseline was set using the BERT model. The BERT model was fine-tuned using an AdamW optimizer with learning rate of 5e-5, and a batch-size of 32. The FinBERT and DistilBERT models were also fine-tuned using an AdamW optimizer with learning rate of 5e-5 and a batch-size of 32. The models were trained for 6 epochs each. The performance of the model was evaluated on the basis of the Accuracy and F1-Score (Weighted) on the test set. The FinBERT model achieved the best performance on the Finanacial PhraseBank dataset.
A comparative study of different optimizers used for training was done. The optimizers were tuned for different parameters by a specific way of search spaces. Each parameter was first tuned on a large search space, and then a smaller and more refined search space was used to find the optimal value for training the model.

 - **[Financial Dashboard :](https://github.com/vrunm/Financial_Dashboard)**
Built an end-to-end Financial Dashboard that collects and consolidates all of a business's critical observations in one place using the information obtained from the annual 10-K SEC Filings.












<!--

**vrunm/vrunm** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

-->

