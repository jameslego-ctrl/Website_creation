# **PDF Summarizer App**
==========================

### **Brief Description**
-------------------------

A Streamlit-based application for uploading PDF files, extracting their content, and generating AI-powered summaries using Hugging Face's pre-trained LaMini-Flan-T5-248M language model and LangChain.

### **Project Goal**
--------------------

* Gain hands-on experience with:
	+ Streamlit
	+ LangChain
	+ Transformer-based models
* **Note:** This project is for educational purposes and not intended for deployment or production use at this stage.

### **Features**
------------

* **Upload PDF Files**: Upload PDFs for summarization
* **In-App PDF Viewer**: View uploaded PDFs directly within the app
* **Automatic Summarization**: Automatically generate summaries of uploaded PDF content

### **Requirements**
-----------------

* **Programming Language:** Python
* **Front-end:** Streamlit
* **LLM Framework:** LangChain
* **Pre-trained Models Library:** Hugging Face Transformers
* **Computation Framework:** PyTorch
* **Encoding Method:** Base64

### **How it Works**
--------------------

#### **Model**
* **LaMini-Flan-T5-248M**: A fine-tuned version of `google/flan-t5-base` on the LaMini-instruction dataset (2.58M samples).
* **Localization**: The model is installed within the project directory for seamless integration.

#### **Tokenizer & Summarization**
* **Tokenizer**: Utilizes LangChain's T5 Tokenizer for converting text into tokenized inputs.
* **Model for Summarization**: Employs `T5ForConditionalGeneration` for fetching the pre-trained model dedicated to text summarization.

#### **PDF Processing & Summarization Pipeline**
1. **Upload**: Upload a PDF file to the application.
2. **Processing**: PyPDFLoader processes the file, splitting it into manageable text chunks.
3. **Summarization**: The text is then summarized using the LaMini-Flan-T5-248M model, leveraging the Hugging Face pipeline for summarization and LangChain for integrating PDF loading and model processing.
4. **Output**: A concise summary of the PDF's content is generated and presented within the app.

### **License**
-------

*This project uses third-party libraries. Please refer to the licenses of:*
* [Hugging Face Transformers](https://github.com/huggingface/transformers/blob/main/LICENSE)
* [LangChain](https://github.com/hwchase17/langchain/blob/master/LICENSE)
* [Streamlit](https://github.com/streamlit/streamlit/blob/develop/LICENSE)
*For the project's specific license (if applying), please see below (or add your license here):*
* **[Your License Name]** (Optional)
[![License: YourLicenseName](https://img.shields.io/badge/License-YourLicenseName-yellow.svg)](YourLicenseURL)

### **Contributing**
------------

*Contributions are welcome. Please:*
1. **Fork** this repository.
2. Create your **feature branch** (`git checkout -b feature/yourFeature`).
3. **Commit** your changes (`git commit -m 'Add some feature'`).
4. **Push** to the branch (`git push origin feature/yourFeature`).
5. Submit a **pull request**.

### **Acknowledgments**
-----------------------

*Special thanks to:*
* Hugging Face for their pre-trained models and Transformers library
* The developers of LangChain for their innovative framework
* Streamlit for their intuitive front-end solution
