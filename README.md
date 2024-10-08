# Amazon Bedrock Knowledge Bases  - Code samples for building RAG applications

## Contents
Contains following folders: 
- 01-rag-concepts
- 02-optimizing-accuracy-retrieved-results
- 03-advanced-concepts
- 04-responsible-ai

### 01-rag-concepts
- [01_create_ingest_documents_test_kb_multi_ds.ipynb](./01-rag-concepts/01_create_ingest_documents_test_kb_multi_ds.ipynb) - creates necessary role and policies required using the `utility.py` file. It uses the roles and policies to create Open Search Serverless vector index, knowledge base, data source, and then ingests the documents to the vector store. You can add multiple data sources to the knowledge base such as `Amazon S3, Confluence, Sharepoint, Salesforce, & Web crawler`. Once the documents are ingested it will then test the knowledge base using `RetrieveAndGenerate` API for question answering, and `Retrieve` API for fetching relevant documents. Finally, it deletes all the resources. If you want to continue with other notebooks, you can choose not to delete the resources and move to other notebooks. Please note, that if you do not delete the resources, you may be incurred cost of storing data in OpenSearch Serverless, even if you are not using it. Therefore, once you are done with trying out the sample code, make sure to delete all the resources. 

- [02_managed_rag_custom_prompting_and_no_of_results.ipynb](./01-rag-concepts/02_managed_rag_custom_prompting_and_no_of_results.ipynb) - Code sample for managed retrieval augmented generation (RAG) using `RetrieveAndGenerate` API from Amazon Bedrock Knowledge Bases.

- [03_customized-rag-retreive-api-hybrid-search-claude-3-sonnet-langchain.ipynb](./01-rag-concepts/03_customized-rag-retreive-api-hybrid-search-claude-3-sonnet-langchain.ipynb) - If you want to customize your RAG workflow, you can use the `retrieve` API provided by Amazon Bedrock Knowledge Bases. You can either performa `semantic` or `hybrid` search over your vector store. This notebook, provides sample code for `hybrid` search using Claude 3 models as well as demonstrates LangChain integraion with Amazon Bedrock Knowledge Bases.

- [04_customized-rag-retreive-api-langchain-claude-evaluation-ragas.ipynb](./01-rag-concepts/04_customized-rag-retreive-api-langchain-claude-evaluation-ragas.ipynb) - If you are interested in evaluating your RAG application, try this sample code for evaluating the response using RAGAS as assesment framework.


### 02-optimizing-accuracy-retrieved-results
- [advanced_chunking_options.ipynb](./02-optimizing-accuracy-retrieved-results/advanced_chunking_options.ipynb) - This notebook provides sample code for various advance chunking strategies (Fixed, Semantic, & Hierarchical) offered Amazon Bedrock Knowledge Bases for building optimum RAG applcation.
  
- [query_reformulation.ipynb](./02-optimizing-accuracy-retrieved-results/query_reformulation.ipynb) - This notebook provides sample code for query reformulation which takes a complex input query and break it into multiple sub-queries. These sub-queries will then separately go through their own retrieval steps to find relevant chunks. In this process, the subqueries having less semantic complexity might find more targeted chunks. These chunks will then be pooled and ranked together before passing them to the FM to generate a response.
  
- [csv_metadata_customization.ipynb](./02-optimizing-accuracy-retrieved-results/csv_metadata_customization.ipynb) - This notebook provides sample code walkthrough for `CSV metadata customization` feature, a newly realsed feautre for Amazon Bedrock Knowledge Bases.
  
- [metadata_filtering.ipynb](./02-optimizing-accuracy-retrieved-results/metadata_filtering.ipynb) - This notebook provides sample code walkthrough for 'metadata filtering' feature, for Amazon Bedrock Knowledge Bases.

### 03-advanced-concepts

- Provides sample code that demonstrates advanced concepts that could be applied to improve retrieval quality/results for Knowledge Base on Amazon Bedrock.
- [dynamic-metadata-filtering-KB.ipynb](./03-advanced-concepts/dynamic-metadata-filtering/dynamic-metadata-filtering-KB.ipynb) - This notebook demonstrates how to implement dynamic metadata filtering for Knowledge Bases for Amazon Bedrock using the tool use (function calling) capability and Pydantic for data validation. By leveraging this approach, you can enhance the flexibility and accuracy of retrieval-augmented generation (RAG) applications, leading to more relevant and contextually appropriate AI-generated responses.

### 04-responsible-ai
- Provides sample code for creating knowledge base and associated data sources using AWS CloudFormation templates.
- [contextual-grounding.ipynb](./04-responsible-ai/contextual-grounding.ipynb) - This notebook demonstrates how to combine Amazon Bedrock Guardrails contextual grounding filter with Amazon Bedrock Knowledge Bases. By doing so, we can ensure that the model's responses are factually grounded and aligned with the information stored in the Knowledge Base.

***

### Note
If you use the notebook - `01_create_ingest_documents_test_kb_multi_ds.ipynb` for creating the knowledge bases and do not delete the resources, you may be incurred cost of storing data in OpenSearch Serverless, even if you are not using it. Therefore, once you are done with trying out the sample code, make sure to delete all the resources. 

## Contributing

We welcome community contributions! Please ensure your sample aligns with [AWS best practices](_!https://aws.amazon.com/architecture/well-architected/_), and please update the Contents section of this README file with a link to your sample, along with a description..
