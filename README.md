# Seeing and Understanding: A Novel LLM based VQA System

This repository contains the implementation of a modular Visual Question Answering (VQA) system that enhances visual reasoning by integrating image captioning and external knowledge retrieval using a Large Language Model (LLM). The system is designed to handle questions that require both image understanding and commonsense/world knowledge.

## Project Overview

Our VQA pipeline consists of three main components:

1. **Visual Feature Extraction**: Uses a pre-trained InceptionV3 model to generate structured visual embeddings.
2. **Caption Generation**: Applies a Transformer-based decoder with visual attention to generate context-aware captions for input images.
3. **Knowledge-Augmented Answering**: Utilizes a pre-trained LLM (Flan-T5) to retrieve or generate external knowledge and produce final answers based on the question and image caption.

## Motivation

Traditional VQA models are limited to information directly present in the image. This project extends their capabilities by incorporating contextual and external knowledge, enabling the system to answer complex questions requiring reasoning beyond the image.

## Requirements

Python 3.8+
TensorFlow
Transformers (transformers by HuggingFace)
Pillow
numpy
All dependencies are listed in requirements.txt.

## Dataset

We evaluate our system using the COCO-VQA 2.0 dataset, focusing on the Balanced Real Images subset for knowledge-intensive questions.

Download it here: https://visualqa.org/download.html

## Example Output 

![Alt text](/surfer.jpg)

Caption (Generated): A man in a red wetsuit is riding a wave.
Input Question: How does the wetsuit help the man while riding the wave?
Answer (Model): The wetsuit protects the man from the cold water.
Ground Truth: It keeps him warm and protects him from the cold water.

