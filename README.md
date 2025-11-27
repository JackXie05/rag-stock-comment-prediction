# RAG-Stock-Comment-Prediction
## Introduction
A Retrieval-Augmented Generation Pipeline for Predicting Stock Price Movements from Semantic Comment Patterns.

## Project Overview
This project builds a retrieval-augmented generation (RAG) system that uses semantic similarity of stock comments (e.g., from Guba/Reddit/X) to predict future stock price movements.
Instead of traditional sentiment → return prediction, this project focuses directly on semantic pattern matching:
	•	Given new comments for a stock
	•	Retrieve similar historical comments via vector embeddings
	•	Aggregate historical price reactions
	•	Predict near-term price movement

This project aims to explore information-rich, sentiment-free modeling for financial prediction.

## Project Structure
rag-stock-comment-prediction/
│
├── src/
│   ├── embeddings/        # Embedding models (BGE/Qwen/etc.)
│   ├── index/             # FAISS / vector search
│   ├── prediction/        # Aggregation & price prediction
│   └── utils/             # Helper functions
│
├── data/
│   ├── raw/               # Original scraped comments & prices (ignored by Git)
│   └── processed/         # Cleaned data
│
├── notebooks/             # Experiment notebooks
├── configs/               # Configuration files
├── README.md              # Project documentation

## Current Status
	•	Project structure initialized
	•	Initial embedding demo
	•	FAISS index builder
	•	Semantic retrieval baseline
	•	Time-decay weighted prediction
	•	Qwen finetuning module
	•	vLLM API for inference

## Future Work
	•	Add sentiment-free semantic aggregation
	•	Add baselines (BERT-Fin, RoBERTa, sentiment models)
	•	Deploy demo API via vLLM
	•	Visualization dashboard