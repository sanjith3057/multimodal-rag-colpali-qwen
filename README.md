# Multimodal RAG with ColPali + Qwen2-VL (Colab 2026)

An end-to-end **multi-modal Retrieval-Augmented Generation** system for PDFs.  
It handles **text + visuals** (tables, charts, layouts, figures) without any OCR.

## Features
- Retrieval: Byaldi + vidore/colqwen2-v1.0 (multi-vector late-interaction, visual-aware)
- Page visualization: Shows retrieved document pages as images
- Generation: Qwen2-VL-2B-Instruct (grounded answers from images, works on free Colab T4)

## Quick Start (in Colab)
1. Open the notebook: [multimodal_rag.ipynb](https://colab.research.google.com/github/sanjith3057/multimodal-rag-colpali-qwen/blob/main/multimodal_rag.ipynb)
2. Run all cells in order
3. Upload your own PDF and ask questions!

## Example Results (on ColPali paper)
**Query:** What is the main innovation of ColPali?  
**Retrieved pages:** 3, 2  
**Answer:** The main innovation of ColPali is its novel retrieval in Vision Space concept, which could significantly alter the way document retrieval is approached in the industry moving forward.

## Tech Stack
- Retrieval: Byaldi<a href="https://github.com/AnswerDotAI/byaldi" target="_blank" rel="noopener noreferrer nofollow"></a>
- Model: vidore/colqwen2-v1.0 + Qwen/Qwen2-VL-2B-Instruct
- Dependencies: pdf2image, transformers, torch, qwen-vl-utils, bitsandbytes

## Limitations
- Free Colab T4: Generation limited to 1–2 pages (VRAM constraints)
- 2B model: Good for prototyping, but 7B+ better for complex documents


