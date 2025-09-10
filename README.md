# Medical Chatbot + Knowledge Graph (LLM × KG)

This repository contains a small **research demo** that combines a **Large Language Model (LLM)** with a **knowledge graph (KG)** for medical decision support.

## Overview
- The chatbot first generates a **patient-friendly reply** using a Hugging Face LLM pipeline.  
- Extracted symptoms are mapped into a **structured knowledge graph**, where edges encode typical symptom–specialty associations.  
- The system computes **scores for likely medical specialties**, reducing the uncertainty of purely generative LLM output.  
- The result is a hybrid approach that is more **explainable and reproducible**, suitable as a prototype for decision support under uncertainty.

## Features
- 🤖 **LLM Integration**: Hugging Face pipeline for text generation  
- 🩺 **Symptom Extraction**: Regex-based matching with synonym support  
- 📊 **Knowledge Graph**: Built with NetworkX (optional PyVis for interactive visualization)  
- 🧮 **Specialty Scoring**: Weighted mapping from symptoms → medical specialties  
- 📦 **Experiment Tracking**: MLflow integration for reproducibility  

## Example Workflow
1. User enters a message (e.g., *"I have headache and stomach pain"*).  
2. LLM generates an initial, patient-friendly response.  
3. Symptom extractor identifies `["headache", "stomach pain"]`.  
4. KG scoring suggests **Neurology** and **Gastroenterology** as most relevant specialties.  
5. Final advice is generated, incorporating both LLM output and KG recommendation.

## Disclaimer
⚠️ **For research and educational purposes only.**  
This demo is **not a medical device** and should not be used for clinical decision-making.

