# MiRel: An Interactive Tool for Exploring miRNA Regulation in Disease through Automated Extraction and Conversational Interface
**Author:** Eva Gianniou  
**Institution:** Maastricht University  

## 🔍 Overview
MiRel is a tool that automates the extraction of miRNA-disease relationships from PubMed abstracts, focusing on regulation status.

## 🚀 Features
- Retrieves PubMed abstracts based on user-selected disease & publication year
- Uses deep learning for Named Entity Recognition (NER) and Relation Extraction (RE) tasks
- Provides a user friendly interface with interactive features including an **interactive table** for exploring extracted relationships
- Includes a **chatbot** for natural language queries

## 🔬 **Methodology Overview**
The methodology consisted of the following stages:

1️⃣ **Data Collection & Preprocessing**:  
- **Source**: PubMed abstracts  
- **Filtering**: Regex-based extraction of miRNA mentions  
- **Dataset Creation** for NER and RE tasks

2️⃣ **Finetuning** 

**NER (Named Entity Recognition)**:  
- Fine-tuned **BioBERT**, **PubMedBERT**, and **SciBERT** models  

**RE (Relation Extraction)**: 
- Fine-tuned **BioBERT**, **PubMedBERT**, and **SciBERT** models   
- Identifies **Upregulation, Downregulation, Dysregulation, or Else**  
- Hyperparameter Tuning, Freezing strategies, 5-fold Cross Validation

3️⃣ **Tool Implementation**:  
- **Flask backend** for data retrieval & processing  
- **HTML/JavaScript frontend**  
- **GPT-powered chatbot** for user queries  

4️⃣ 📊 **Evaluation**
**🔹 NER Results:**  
- BioBERT achieved **98% F1-score** 
- **Regex performed slightly better 99%** due to miRNA's structured naming conventions  

**🔹 RE Results:**  
- BioBERT significantly outperformed regex-based methods  
- Achieved **F1-scores between 92-95%** across folds  
- **ROC AUC:** Up to **96% accuracy** in classifying relationships  

**🔹 Tool Evaluation**: The tool was evaluated by comparing its extracted relationships to manually annotated ones from PubMed Abstracts for a specific disease and publication year
- The results with 86% Precision and 91% Recall showed strong performance of the model in identifying miRNA-disease regulatory relationships

## ❗ **Error Analysis**
- Error Analysis was conducted to identify common patterns of misclassification. 
- Preprocessing and Postprocessing steps were performed to improve tool's accuracy 


## 🛠 **Tool's Interface**
![MiRel's Interface](assets/MiRel.png.png)


## 🔮 **Future Work**
After analysing the MiRel's limitations, future enhancements were proposed to enhance and expand the tool's capabilities. 
- Implement **coreference resolution** for multi-sentence relationships  
- Improve **chatbot accuracy** using **Retrieval-Augmented Generation (RAG)**  
- Enhance **reranking functionality** to prioritize **highly relevant abstracts**  
- Extend MiRel to analyze **other biomolecules (proteins, genes)**  