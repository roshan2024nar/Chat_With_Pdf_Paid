Chat with PDF - Paid Version
Overview
The Chat with PDF - Paid Version is an advanced AI-powered application that allows users to interact with the contents of PDF documents in a conversational manner. This premium version utilizes OpenAI's advanced language models to deliver faster and more accurate responses compared to the free version. With its intuitive interface, users can efficiently ask questions and retrieve relevant information from uploaded PDFs.

Features
Upload PDFs: Users can upload multiple PDF documents for processing.
Process PDFs: Extract text from the PDFs and build a searchable index.
Conversational Interface: Ask questions about PDF content and receive accurate AI-generated responses in real-time.
Chat Layout: Displays chat history with user messages on the right and bot responses on the left for clear visualization.
High Accuracy & Speed: Enhanced precision and response speed with the help of OpenAI's language models.
Requirements
Python 3.7 or higher
Streamlit
dotenv
PyPDF2
langchain (including langchain, faiss, huggingface_hub)
OpenAI API Key
Installation
1. Clone the Repository:
bash
Copy code
git clone https://github.com/your-repo/chat-with-pdf.git
cd chat-with-pdf
2. Create and Activate a Virtual Environment:
bash
Copy code
python -m venv .venv
# On Windows
.venv\Scripts\activate
# On macOS/Linux
source .venv/bin/activate
3. Install the Required Dependencies:
bash
Copy code
pip install -r requirements.txt
4. Set Up Environment Variables:
Create a .env file in the root directory and add your OpenAI API key:

makefile
Copy code
OPENAI_API_KEY=your_openai_api_key_here
Usage
1. Run the Streamlit App:
bash
Copy code
streamlit run app.py
2. Open the App:
In your web browser, navigate to http://localhost:8501.

3. Upload PDFs:
Use the file uploader on the sidebar to upload one or more PDF documents.

4. Process PDFs:
Click on the "Process" button to extract text from the PDFs and build the searchable index.

5. Ask Questions:
Enter your questions in the input box at the top of the page. The AI will respond based on the content of the uploaded PDFs, providing detailed and accurate answers.

Code Explanation
get_pdf_text(pdf_docs): Extracts text from the uploaded PDF documents.
get_text_chunks(text): Splits the extracted text into smaller chunks for easier processing.
get_vectorstore(text_chunks): Builds a FAISS vector store using embeddings generated from OpenAI.
get_conversation_chain(vectorstore): Initializes the conversational chain that integrates the LLM with the vector store.
handle_userinput(user_question): Processes the user’s question and displays the conversation history.
main(): Sets up the layout for the Streamlit app and handles user input and PDF processing.
Notes
Performance: The paid version significantly enhances the performance and accuracy of the responses compared to the free version.
API Usage: Ensure you have a valid OpenAI API key and monitor your API usage according to OpenAI's pricing and rate limits.
