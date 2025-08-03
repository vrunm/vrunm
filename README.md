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

**Performance Evaluation of Rankers and RRF Techniques for Retrieval Pipelines**

[Code](https://github.com/avnlp/rrf)
[Report](https://github.com/avnlp/rrf/blob/main/paper/rankers_rrf.pdf)

A RAG pipeline can be tuned in many ways to give more relevant answers. One important way is to improve the retrieved context which is input to the LLM. This ensures that the generated answers are coherent and consistent with the content in the original documents.

In the intricate world of LFQA and RAG, making the most of the LLM’s context window is paramount. Any wasted space or repetitive content limits the depth and breadth of the answers we can extract and generate. It’s a delicate balancing act to lay out the content of the context window appropriately. 

We have done a comparative study of adding different combinations of rankers in a Retrieval pipeline along with the use of Reciprocal Rank Fusion (RRF) techniques. The results were evaluated on four metrics, viz., Normalized Discounted Cumulative Gain (NDCG), Mean Average Precision (MAP), Recall and Precision. We aim to analyze the effectiveness of adding different rankers to pipelines to improve the quality of retrieved documents.

 - **[Financial Dashboard :](https://github.com/vrunm/Financial_Dashboard)**
Built an end-to-end Financial Dashboard that collects and consolidates all of a business's critical observations in one place using the information obtained from the annual 10-K SEC Filings.
The financial dashboard contains:

    - Insights and summaries for different sections from annual corporate filings.
   
    - Sentiment-based score that measures the company's performance over a certain time period.
   
    - Identification of Important topics and Frequently occuring words mentioned in the report.

**Open Source Contributions**:
  - **[Haystack](https://github.com/deepset-ai/haystack)**: [deepset-ai/haystack](https://github.com/deepset-ai/haystack/pulls?q=is%3Apr+author%3Avrunm+is%3Aclosed+sort%3Aupdated-desc), [deepset-ai/haystack-core-integrations](https://github.com/deepset-ai/haystack-core-integrations/pulls?q=is%3Apr+author%3Avrunm+is%3Aclosed+sort%3Aupdated-desc)
  






<!--

**vrunm/vrunm** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

-->

