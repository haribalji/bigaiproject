
# DEMO VIDEO :https://drive.google.com/file/d/1ymU8jb_H42CObcRXegFxJ7gOdkfDAmYK/view?usp=sharing


RAG-Based Q&A:
flow-control

1.User uploads a PDF → saved as uploaded.pdf.

2.Text extracted → split into chunks.

3.Each chunk → converted to embeddings (SentenceTransformer).

4.Embeddings + text → stored in ChromaDB.

5.User asks a question → question embedded → top relevant chunks retrieved.

6.Retrieved context + question → sent to Llama-3.1 model (via HuggingFace).

7.Model generates and returns clear, formatted answer.


<img width="1134" height="716" alt="Screenshot 2025-11-08 142943" src="https://github.com/user-attachments/assets/68e435c7-b2e4-403f-9631-8c30f079519e" />



OCR model
The system integrates OCR technology to convert handwritten or printed notes into editable, dyslexia-friendly digital text. Students can upload or capture images of their notes, which are processed using two deep learning models:

CRAFT (Character Region Awareness for Text Detection): Detects text areas and links characters into words using region and affinity scores.

CRNN (Convolutional Recurrent Neural Network): Reads and converts detected text into clean, readable digital form using CNN, RNN, and CTC layers.

Then, the extracted text is sent to Gemini, which generates detailed explanations of the content in both Tamil and English.



<img width="1409" height="667" alt="image" src="https://github.com/user-attachments/assets/14ca34bc-111a-424f-aebd-00195c09d104" />


<img width="1330" height="613" alt="image" src="https://github.com/user-attachments/assets/5c0c3b9c-e585-4640-8ab0-22ff009bbe9d" />






AI Summarization & TTS:
We used gemini-2.0-flash to generate simplified and concise summaries. By carefully crafting prompts, the model rephrases complex text into easier, dyslexia-friendly. This summarized content is then converted into speech using a TTS engine, available in both Tamil and English Text to Speech, helping users comprehend and retain information more effectively.


<img width="1411" height="625" alt="image" src="https://github.com/user-attachments/assets/39d2f3d9-15e7-476f-b29d-32bae19b9135" />

<img width="1451" height="687" alt="image" src="https://github.com/user-attachments/assets/5d7da10a-1c63-4197-83f2-7672397cb0fc" />









# **AI Models-Requriment:**

1.Embedding Model:arvindcreatrix/bge-baes-my-qna-model (SentenceTransformer)

2. LLM:meta-llama/Llama-3.1-8B-Instruct:novita via HuggingFace router

3. Generator:Gemini 2.0 Flash

4. Vector DB:ChromaDB



# Tech Stack

React.js

Node.js

Express.js

FastAPI

Uvicorn

Python

ChromaDB

Sentence Transformers

Gemini 2.0 Flash / Llama 3.1

PyPDF

JWT (JSON Web Token)

dotenv

CSS

ESLint

Babel

npm

#  Hosting Platforms

Frontend: Vercel

Backend (Node.js): Render







# ⚙️ Local Setup

Follow the steps below to run the project locally:

# 1. Clone the repository
 git init
  git clone https://github.com/haribalji/bigaiproject.git
  
# 2. Navigate to the frontend folder
cd frontend

# 3. Install all necessary frontend packages
npm install

# 4. Run the frontend
npm start

# 5. Open another terminal and navigate to the backend folder
cd backend

# 6. Install all necessary backend packages
npm install

# 7. Start the backend server
node index.js
# (or use nodemon for auto-reload)
nodemon index.js

# 8.install dependencies using:
pip install -r requirements.txt

# 9. Open another terminal and start the RAG (AI) FastAPI server
uvicorn rag_api:app --reload

# 10. Open another terminal, navigate to backend again
cd backend

# 11. Run the Python application
python app.py

After Setup

Frontend: http://localhost:3000

Node.js Backend: http://localhost:5000

FastAPI (AI Backend): http://127.0.0.1:8000




