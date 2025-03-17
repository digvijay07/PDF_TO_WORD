# PDF_TO_WORD
Application to convert PDF to Word

# PDF to Word Converter

A web application that allows users to upload PDF files and convert them to Word documents.

## Features

- Simple and intuitive interface
- Fast conversion of PDF to Word
- OCR (Optical Character Recognition) support for scanned documents
- Download converted Word documents directly from the browser

## Project Structure

```
PDF_TO_WORD/
├── frontend/         # React frontend
├── backend/          # Python Flask backend
```

## Prerequisites

1. Node.js and npm (for frontend)
2. Python 3.7+ (for backend)
3. Tesseract OCR (for OCR functionality)

## Installation

### Tesseract OCR Installation

For OCR functionality, you need to install Tesseract OCR:

- **Windows**: Download and install from [https://github.com/UB-Mannheim/tesseract/wiki](https://github.com/UB-Mannheim/tesseract/wiki)
- **macOS**: `brew install tesseract`
- **Linux**: `sudo apt install tesseract-ocr`

After installation, make sure the Tesseract executable is in your system PATH.

### Backend Setup

1. Navigate to the backend directory:
   ```
   cd PDF_TO_WORD/backend
   ```

2. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   ```

3. Activate the virtual environment:
   - Windows:
     ```
     venv\Scripts\activate
     ```
   - macOS/Linux:
     ```
     source venv/bin/activate
     ```

4. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

5. Run the Flask application:
   ```
   python app.py
   ```
   The backend server will start on http://localhost:5000.

### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd PDF_TO_WORD/frontend
   ```

2. Install the dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm start
   ```
   The application will open in your browser at http://localhost:3000.

## Usage

1. Open the web application in your browser (http://localhost:3000).
2. Click on the "Choose PDF file" area to select a PDF file from your computer.
3. For scanned documents or image-based PDFs, check the "Use OCR" option.
4. Click the "Convert to Word" button to begin the conversion process.
5. Once the conversion is complete, click the "Download Word Document" button to save the converted file.

## OCR Mode

The OCR mode is designed for:
- Scanned documents
- PDFs where text is embedded in images
- PDFs where text cannot be selected or copied

OCR mode uses Tesseract OCR to extract text from images in the PDF. Note that OCR conversion:
- Takes longer than regular conversion
- May be less accurate depending on image quality
- Works best with clear, high-resolution scans

## Technology Stack

- **Frontend**: React, TypeScript
- **Backend**: Flask (Python)
- **PDF Conversion**: pdf2docx Python library
- **OCR**: Tesseract OCR with pytesseract Python binding 
