Chat with PDF - Paid Version
Overview
The "Chat with PDF - Paid Version" application allows users to interact with PDF documents by asking questions about their contents. This enhanced version leverages OpenAI's powerful language models to provide faster and more accurate responses compared to the free version. The app offers a conversational AI interface to help users retrieve and understand information from their uploaded PDFs efficiently.

Features
Upload PDFs: Users can upload multiple PDF documents for processing.
Process PDFs: Extract text from the PDFs and create a searchable index.
Conversational Interface: Ask questions about the PDF content and receive accurate AI-generated responses.
Chat Interface: View conversation history with messages from the bot aligned to the left and user messages aligned to the right.
High Accuracy: Enhanced response accuracy and speed using OpenAI's language models.
Requirements
Python 3.7 or higher
Streamlit
dotenv
PyPDF2
langchain (includes langchain, faiss, huggingface_hub, etc.)
OpenAI API Key
Installation
Clone the Repository:

bash

git clone https://github.com/your-repo/chat-with-pdf.git
cd chat-with-pdf
Create and Activate a Virtual Environment:

bash

python -m venv .venv
.venv\Scripts\activate  # On Windows
# or
source .venv/bin/activate  # On macOS/Linux
Install the Required Dependencies:

bash

pip install -r requirements.txt
Set Up Environment Variables:

Create a .env file in the root directory and set your OpenAI API key:

makefile

OPENAI_API_KEY=your_openai_api_key_here
Usage
Run the Streamlit App:

bash

streamlit run app.py
Open Your Web Browser and navigate to http://localhost:8501.

Upload PDFs: Use the file uploader in the sidebar to upload your PDF documents.

Process PDFs: Click on the "Process" button to extract text from the uploaded PDFs and build the searchable index.

Ask Questions: Enter your questions in the input box at the top of the page to interact with the uploaded PDFs. The AI will provide accurate responses based on the content of the documents.

Code Explanation
get_pdf_text(pdf_docs): Extracts text from the uploaded PDF documents.
get_text_chunks(text): Splits the extracted text into chunks for processing.
get_vectorstore(text_chunks): Creates a FAISS vector store using embeddings from OpenAI.
get_conversation_chain(vectorstore): Initializes the conversational retrieval chain with the LLM and vector store.
handle_userinput(user_question): Processes user questions and displays the conversation history.
main(): Sets up the Streamlit app layout and handles user input and PDF processing.
Notes
Performance: The paid version offers significantly improved performance and accuracy compared to the free version.
API Usage: Ensure you have a valid OpenAI API key and manage your usage according to OpenAI's pricing and usage policies.