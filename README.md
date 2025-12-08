# RAG-with-LangChain

RAG is an architectural pattern that can be used to augment the performance of language models by recalling factual information from a knowledge base, and adding that information to the model query. The most common approach in RAG is to create dense vector representations of the knowledge base in order to retrieve text chunks that are semantically similar to a given user query.

RAG use cases include:
- Customer service: Answering questions about a product or service using facts from the product documentation.
- Domain knowledge: Exploring a specialized domain (e.g., finance) using facts from papers or articles in the knowledge base.
- News chat: Chatting about current events by calling up relevant recent news articles.

In its simplest form, RAG requires 3 steps:

- Initial setup:
  - Index knowledge-base passages for efficient retrieval. In this recipe, we take embeddings of the passages, and store them in a vector database.
- Upon each user query:
  - Retrieve relevant passages from the database. In this recipe, we use an embedding of the query to retrieve semantically similar passages.
  - Generate a response by feeding retrieved passage into a large language model, along with the user query.
