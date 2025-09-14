# LangChain-powered-MCQ-Generator
Project Description
This project provides two Python applications that leverage LangChain and the Groq API to automatically generate multiple-choice questions (MCQs) from text documents. The applications can process .pdf, .docx, and .txt files. They extract text from the uploaded documents, use a large language model (LLM) to create a specified number of MCQs, and then save the generated questions as .txt and .pdf files.

Features
Text Extraction: Extracts content from common document types (.pdf, .docx, .txt).
LLM Integration: Uses the llama-3.3-70b-versatile model via the LangChain framework and Groq API for high-speed question generation.
Customizable Output: Allows the user to specify the number of MCQs to generate.
Multiple Formats: Saves the generated questions in both a plain text file (.txt) and a portable document format (.pdf).

Two Application Types:
app.py: A web-based application built with Flask that provides a user-friendly interface for uploading files and downloading the generated MCQs.
main.py: A command-line script for local, non-interactive use, ideal for batch processing or automation.


Setup and Installation
Prerequisites
Python 3.8 or higher
pip install Flask pdfplumber python-docx fpdf langchain-groq

Set up your API Key:

Obtain a Groq API key.
In both app.py and main.py, replace " " with your actual API key.



File Structure
app.py: The Flask web application.
main.py: The command-line script.
index.html: The HTML template for the file upload page.
results.html: The HTML template for the results page.
uploads/: Directory for uploaded files (used by app.py).
results/: Directory for generated .txt and .pdf files.
The Wonders of Science.docx: Example document to be used with main.py.



Web Application (app.py)
To start the Flask server, run:

Bash

python app.py
Open your web browser and navigate to http://127.0.0.1:5000.
Use the interface to upload a document and specify the desired number of questions.
After generation, you can download the MCQs in both .txt and .pdf formats.

2. Command-Line Script (main.py)
Before running, ensure you have a document you want to process.
Modify the UPLOAD_FILE variable in main.py to point to your desired file (e.g., "path/to/your/document.pdf").
Adjust the NUM_QUESTIONS variable if you need a different number of MCQs.

Run the script from your terminal:

Bash
python main.py
The generated files will be saved in the results/ folder
