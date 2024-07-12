# Lab 2 Amazon Bedrock Knowledge Base - Samples for building RAG workflows

## Contents
- [01_create_ingest_documents_test_kb.ipynb](./01\_create_ingest_documents_test_kb.ipynb) - creates necessary role and policies required using the `utility.py` file. It uses the roles and policies to create Open Search Serverless vector index, knowledge base, data source, and then ingests the documents to the vector store. Once the documents are ingested it will then test the knowledge base using `RetrieveAndGenerate` API for question answering, and `Retrieve` API for fetching relevant documents. Finally, it deletes all the resources. If you want to continue with other notebooks, you can choose not to delete the resources and move to other notebooks. Please note, that if you do not delete the resources, you may be incurred cost of storing data in OpenSearch Serverless, even if you are not using it. Therefore, once you are done with trying out the sample code, make sure to delete all the resources. 

- [02_managed-rag-kb-retrieve-generate-api.ipynb](./02\_managed-rag-kb-retrieve-generate-api.ipynb) - Code sample for managed retrieval augmented generation (RAG) using `RetrieveAndGenerate` API from Knowledge Bases for Amazon Bedrock.

- [03_customized-rag-retrieve-api-langchain-claude-v2.ipynb](./03\_customized-rag-retrieve-api-langchain-claude-v2.ipynb) - Code sample for using the `RetrieveQA` chain from LangChain and Amazon Knowledge Base as the retriever.


Remember to use the [99_CLEAN_UP.ipynb](./99\_CLEAN_UP.ipynb)

***

### Note
If you use the notebook - [01_create_ingest_documents_test_kb.ipynb](./01\_create_ingest_documents_test_kb.ipynb) for creating the knowledge bases and do not delete the resources, you may be incurred cost of storing data in OpenSearch Serverless, even if you are not using it. Therefore, once you are done with trying out the sample code, make sure to delete all the resources. 

## Contributing

We welcome community contributions! Please ensure your sample aligns with  [AWS best practices](https://aws.amazon.com/architecture/well-architected/), and please update the **Contents** section of this README file with a link to your sample, along with a description.