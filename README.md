# PDF-to-Answer with AI

This project extracts and summarizes content from PDFs, leveraging the power of OpenAI's GPT-3.5 and GPT-4 models. The system handles text, tables, and images within PDFs, providing detailed answers to user queries based on the extracted content.

## Features

- **PDF Parsing**: Extracts text, tables, and images from PDF files using the `unstructured` library.
- **Text Summarization**: Summarizes extracted text and tables using OpenAI's GPT-3.5.
- **Image Description**: Encodes and describes images using OpenAI's GPT-4 with vision capabilities.
- **Vector Store Creation**: Stores document summaries in a FAISS vector store for efficient similarity search.
- **Question Answering**: Uses a custom GPT-4 based chain to answer user queries based on the context from the vector store.

## Installation

1. **Install dependencies**:
    ```sh
    sudo apt install tesseract-ocr -y
    sudo apt install libtesseract-dev -y
    sudo apt-get install poppler-utils -y
    pip install langchain_community
    pip install langchain unstructured[all-docs] pydantic lxml openai chromadb tiktoken opencv-python faiss-cpu
    ```

2. **Set up OpenAI API Key**:
    ```python
    from google.colab import userdata
    openai_api_key = userdata.get('OPENAI_API_KEY')
    ```
