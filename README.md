**LLM-RAG in R
**
A hands-on exploration of Large Language Models and Retrieval-Augmented Generation (RAG) built entirely in R. This project progressively builds from basic NLP and classification to a fully functional RAG chatbot powered by OpenAI.

**What's Inside:
**
1. Neural Network Classifier (nnet)

Trains a multi-class neural network on the Iris dataset
Normalizes features, splits into train/test, and evaluates accuracy via confusion matrix
Built using R's nnet package (single hidden layer)

2. Text Processing + Naive Bayes Classifier

Preprocesses text using tm (tokenization, stopword removal, lowercasing)
Builds a Document-Term Matrix and trains a Naive Bayes classifier
Simulates a simple LLM-style text classification pipeline

3. Rule-Based Chatbot

A lightweight, pattern-matching chatbot built with base R
Responds to greetings, name queries, and exit commands
Demonstrates foundational conversational logic before introducing LLMs

4. LLM-Powered Chatbot (OpenAI API)

Connects to OpenAI's gpt-4o-mini via REST API using httr and jsonlite
Maintains a conversational loop in the R console
System prompt configurable for different assistant personas

5. RAG Pipeline (TF-IDF + Cosine Similarity)

Implements a full Retrieve-then-Generate pipeline without external LLM dependencies
Uses TF-IDF vectors and cosine similarity to retrieve the most relevant documents
Generates answers by passing retrieved context to a mock generation step

6. RAG Chatbot with Shiny + OpenAI Embeddings

Full-stack RAG app built with R Shiny
Uses OpenAI's text-embedding-3-small for semantic document embeddings
Retrieves top-k relevant documents and passes context to gpt-4o-mini for generation
Interactive UI with question input, answer display, and retrieved context view

**Tech Stack
**

Language: R
Packages: nnet, tm, text2vec, e1071, httr, jsonlite, shiny, dplyr
APIs: OpenAI Chat Completions, OpenAI Embeddings

**Setup
**

Clone the repo
Install required packages:
rinstall.packages(c("nnet", "tm", "text2vec", "e1071", "httr", "jsonlite", "shiny", "dplyr"))
Add your OpenAI API key where indicated:
rSys.setenv(OPENAI_API_KEY = "your-key-here")
Run any script independently or launch the Shiny app with shinyApp(ui, server)

**Key Concepts Covered
**

Text preprocessing and vectorization
TF-IDF and cosine similarity
Naive Bayes classification
Neural networks in R
REST API integration with OpenAI
Retrieval-Augmented Generation (RAG)
Interactive app development with Shiny
