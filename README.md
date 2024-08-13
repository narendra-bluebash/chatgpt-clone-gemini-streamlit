# Explore Complex PDF with chat-gemini-

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)

## 💡 What is RAGIFY-ENGINE?

RAGIFY-ENGINE is an open-source RAG (Retrieval-Augmented Generation) engine based on deep document understanding. It offers a streamlined RAG workflow for businesses of any scale, combining LLM (Large Language Models) to provide truthful question-answering capabilities, backed by well-founded citations from various complex formatted data.




## Features
- **Table Extraction**: Identify and parse tables to retrieve structured data, making it easier to answer data-specific questions.
- **Text Extraction**: Efficiently extract and process text from PDFs, enabling accurate and comprehensive information retrieval.
- **Image Analysis**: Extract and interpret images within the PDFs to provide contextually relevant information.

## Technologies Used
- **RAG (Retrieval-Augmented Generation)**: Combines retrieval and generation for more accurate answers.
- **LangChain**: Framework for building applications with language models.
- **Streamlit**: Framework for creating interactive web applications with Python.
- **Poetry**: Dependency management and packaging tool for Python.

## Setup Instructions

Follow these steps to set up the project on your local machine:

**1. Clone the Repository:**
- Begin by cloning the repository to your local machine:
```
https://github.com/langchain-tech/Ragify-engine.git
cd Ragify-engine
```

**2. Install project dependencies:**
- Use Poetry to install the dependencies defined in your pyproject.toml file. This command will also respect the versions pinned in your poetry.lock file:
```
poetry install
```
This will create a virtual environment (if one does not already exist) and install the dependencies into it.


**3. Activate the virtual environment (optional):**
- If you want to manually activate the virtual environment created by Poetry, you can do so with:
```
poetry shell
```
This step is optional because Poetry automatically manages the virtual environment for you when you run commands through it.


**4. Set Up Environment Variables:**
- Create a .env file in the root directory of your project and add the required environment variables. For example:
```
OPENAI_API_KEY = Your_OPENAI_API_KEY
POSTGRES_URL_EMBEDDINDS = YOUR_POSTGRES_URL,  like:-postgresql+psycopg://{db_user}:{db_password}@{db_host}:{db_port}/{db_name}
POSTGRES_URL = YOUR_POSTGRES_URL ,  like:- postgresql://{db_user}:{db_password}@{db_host}:{db_port}/{db_name}
COHERE_API_KEY = YOUR_COHERE_API_KEY
```

**5. Run Streamlit app**
```
python -m streamlit run web.py
```

**5. Run Data ingestion file**
- This command will insert data into your postgres database
```
python3 app.py --help
```
- usage: app.py [-h] --filename FILENAME [--parser_name PARSER_NAME]
- Process the file and extract text chunks

options:
-  -h, --help                      show this help message and exit
-  --filename FILENAME             The path to the file
-  --parser_name PARSER_NAME       The name of the parser to use like book, laws, manual, naive, one, paper, presentation, qa, resume, table


## Currently Supported Documnets are:-
- book:-   pdf, txt, htm|html, doc, (In future docx).
- laws:-   pdf, txt, htm|html, doc, docx.
- manual:- pdf, docx.
- naive:-  pdf, txt|py|js|java|c|cpp|h|php|go|ts|sh|cs|kt, htm|html, doc, docx, json, md|markdown, xlsx.
- one:-    pdf, txt, htm|html, doc, docx, xlsx.
- paper:-  pdf.
- presentation:-  pdf, pptx.
- qa:-     pdf, txt|csv, md|markdown, docx, xlsx.
- resume:- working on it.
- table:-  xlsx, txt|csv

## Result:-
![My test image](readme_img/test1.png)