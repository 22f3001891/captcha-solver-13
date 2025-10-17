# Image OCR Demo (Not for CAPTCHA/Verification)

MIT Licensed, single-file web app for performing Optical Character Recognition (OCR) on general images directly in the browser using Tesseract.js. It supports loading an image via a query parameter (?url=...) or local upload/drag-and-drop. The app explicitly refuses to process CAPTCHA or verification-related images and is not intended to bypass any security mechanisms.

## Overview

- Client-side OCR in the browser (no server).
- Load images via:
  - URL input
  - Drag & drop or file upload
  - Query parameter: ?url=https://example.com/image.png
- Progress and status indicators while recognizing text.
- Copy recognized text with one click.
- Built-in sample image used by default if no URL is provided.

Important:
- This tool is for general OCR tasks only. It is not a CAPTCHA solver and includes safeguards to prevent use with CAPTCHA or verification images (it blocks URLs that appear to be related to CAPTCHA/verification systems).
- For remote URLs, Cross-Origin Resource Sharing (CORS) must be allowed by the image host, otherwise loading may fail. You can download the image and upload it locally as a workaround.

## Setup

- No build step required. Just open index.html in a modern browser with internet access (to load Tesseract.js from a CDN).
- If you need offline use, download Tesseract.js and serve index.html and the library from a local web server.

Files:
- index.html — Complete app (HTML/CSS/JS).
- This README — Documentation and license.

## Usage

1) Open the app
- Double-click index.html or serve it locally (e.g., using a static file server).

2) Load an image
- Via query parameter: append ?url=YOUR_IMAGE_URL to the page URL. Example:
  - file:///path/to/index.html?url=https://example.com/text-image.png
- Paste a URL into the input and click “Load URL”.
- Drag & drop an image onto the dropzone.
- Click “Upload Image” and choose a file.
- If a URL appears related to CAPTCHA/verification, the app will refuse to process it. A local or non-CAPTCHA image is required.

3) Run OCR
- Click “Run OCR”.
- Watch the progress/status updates.
- When finished, the recognized text appears in the result panel.

4) Copy results
- Click “Copy Text” to copy the recognized text to your clipboard.

Notes:
- For best results, use clear, high-contrast images with legible text.
- Remote images must permit CORS; if they don’t, save the image and upload it locally.

## License

MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.