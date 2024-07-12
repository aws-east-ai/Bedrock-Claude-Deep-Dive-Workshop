# Lab 3 Multimodal

## Overview

The multi-modal capability of Claude 3 allows for the input of not only text but also an image that you can ask questions about.

An example of the new mulimodal capability of the Claude 3 model is shown below with the new Messages API structure. The lab has tips on getting started with images and seeing how you can effectively prompt Claude with images to carry out tasks such as interpreting and analyzing charts or extracting content from forms or mind maps. We also have a best practices guide for improving performance with Claude 3 Vision.

With the Amazon Titan Multimodal Embeddings G1 model, you can create embeddings for multimodal data, specifically text and image data. These embeddings can then be used for multimodal search and Retrieval Augmented Generation (RAG) use-cases, for example searching images by text only, images only or a combination of text and images. In addition, an example of using Claude 3's vision capabilities and Titan Multomodal Embeddings model in a RAG workflow is shown using Langchain.

## Workshop labs

1. **Image understanding and visual QA**: In this module, you will learn how to read and understand images using Claude 3 and some best practices. This module uses 3 files: `01_how_to_transcribe_text.ipynb`, `02_reading_charts_graphs_powerpoints.ipynb` and `03_best_practices_for_claude3_bedrock.ipynb`.
2. **Multimodal embedding and searching**: In this module, you will learn how to embed and search images with multimodality. This module uses `04_bedrock-titan-multimodal-embeddings.ipynb` file.
3. **Multimodal RAG**: In this module, you will learn how to write RAG pipeline using multimodal. This module uses `05_multimodal_rag.ipynb` file.
