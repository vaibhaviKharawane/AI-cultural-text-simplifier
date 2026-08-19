AI-Powered Sanskrit Learning Assistant
An AI-powered educational application designed to make Sanskrit learning easier, simpler, and more interactive for students.
The system converts complex Sanskrit content into easy-to-understand Hindi explanations using OCR, translation, and Large Language Models. It also provides glossary generation, quizzes, fill-in-the-blanks, and voice-based learning features.

Project Overview
Sanskrit is a classical language with rich vocabulary and complex grammatical structures, which can make it difficult for modern students to understand.
The AI-Powered Sanskrit Learning Assistant bridges this gap by combining Artificial Intelligence, Natural Language Processing, OCR, and interactive learning techniques.

Users can either:
Enter Sanskrit text manually
Upload an image containing Sanskrit text
The system processes the input and provides:
Sanskrit text extraction
Hindi translation
Simplified Hindi explanation
Important Sanskrit terms and meanings
MCQ-based practice
Fill-in-the-blanks exercises
Text-to-Speech
Speech recognition
Instant feedback and scoring

Key Features
1. Sanskrit Text Extraction using OCR
Users can upload an image containing Sanskrit text.
The system uses Tesseract OCR to extract the Sanskrit text from the image.
2. Sanskrit → Hindi Translation
The extracted Sanskrit text is translated into Hindi using the Google Translate API.
3. AI-Based Text Simplification
The translated Hindi content is processed using the Gemini API to generate simple and student-friendly explanations.
4. Glossary Generation
The system identifies important Sanskrit terms and generates their simplified meanings in Hindi.
5. Interactive MCQs
The system automatically generates Multiple Choice Questions based on the learning content.
6. Fill-in-the-Blanks
Students can practice important words and concepts using fill-in-the-blank exercises.
7. Text-to-Speech
Simplified Hindi explanations can be converted into audio using gTTS, allowing students to listen to the content.
8. Speech Recognition
Students can provide spoken answers, which are converted into text using speech recognition.
9. Evaluation & Feedback
The system evaluates user responses and provides:

Correct/incorrect feedback
Correct answers
Hints
Explanations
Scores

System Architecture
The application follows a modular layered architecture:

                    ┌──────────────────────┐
                    │        User          │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Streamlit Frontend   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    FastAPI Backend   │
                    └──────────┬───────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       ┌──────────┐      ┌────────────┐    ┌────────────┐
       │   OCR    │      │ Translation│    │    Gemini  │
       │ Tesseract│      │    API     │    │    API     │
       └──────────┘      └────────────┘    └────────────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌──────────────────────┐
                    │ Simplified Hindi     │
                    │ + Glossary           │
                    │ + Exercises          │
                    │ + Voice Features     │
                    └──────────────────────┘
The project report describes the architecture as four major layers: **Presentation, Application, Processing/Service, and External Services**.
Workflow

User Input
    │
    ├── Sanskrit Text
    │
    └── Sanskrit Image
            │
            ▼
       OCR Processing
            │
            ▼
    Text Preprocessing
            │
            ▼
 Sanskrit → Hindi Translation
            │
            ▼
    AI Simplification
            │
            ▼
     Glossary Generation
            │
            ├── MCQs
            │
            ├── Fill in the Blanks
            │
            └── Voice Features
            │
            ▼
      Evaluation & Feedback
            │
            ▼
        Final Output

The documented workflow consists of input acquisition, OCR, preprocessing, translation, AI simplification, glossary generation, interactive learning, optional voice processing, evaluation, and output/history management.
 Technologies Used

| Technology               | Purpose                           |
| ------------------------ | --------------------------------- |
 Python               | Core programming language         |
|FastAPI              | Backend API development           |
|Streamlit            | Frontend/UI                       |
|Tesseract OCR        | Sanskrit text extraction          |
|Google Translate API | Sanskrit → Hindi translation      |
|Google Gemini API   | AI-based simplification           |
|Pytesseract        | Python OCR integration            |
|Pillow               | Image processing                  |
|gTTS                 | Text-to-Speech                    |
|SpeechRecognition    | Speech-to-Text                    |
|RapidFuzz           | Approximate answer matching       |
|Requests            | API communication                 |
|spacy              | Text processing / term extraction |

These technologies and their roles are documented in the project report.
 Project Structure

AI-Powered-Sanskrit-Learning-Assistant/
│
├── frontend/
│   ├── app.py
│   └── ...
│
├── backend/
│   ├── main.py
│   ├── services/
│   └── ...
│
├── images/
│   └── ...
│
├── requirements.txt
├── README.md
└── .gitignore
