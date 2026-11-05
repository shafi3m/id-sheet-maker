# ID Sheet Maker

Create a print-ready **A4 landscape PDF** containing your ID documents, passport pages, and photo in one neatly arranged sheet.

ID Sheet Maker is a browser-based tool for uploading documents, checking their detected positions, adjusting images, reviewing the final sheet, and exporting it as a PDF.

> **Your files stay on your device. 100% private.**

## Features

- **Multiple file uploads** — add images or PDF documents together.
- **Supported formats** — JPG, JPEG, PNG, WebP, and PDF.
- **Document detection** — searches uploaded files for document regions and suggests document types.
- **PDF support** — reads PDF pages, including password-protected PDFs when the correct password is provided.
- **Document organization** — assign or change the type of each detected document.
- **Image adjustment** — fine-tune document boundaries, positioning, and rotation.
- **A4 landscape preview** — review the arranged sheet before exporting.
- **Name recognition** — uses English OCR to help read the name on the PAN card.
- **Editable PDF filename** — automatically suggests a filename from the entered or detected name.
- **Validation checks** — highlights missing documents and potential issues.
- **PDF export** — generates a downloadable A4 landscape PDF.
- **WhatsApp sharing** — uses the device/browser share sheet when file sharing is supported.
- **Responsive interface** — designed for desktop and mobile screens.

## Getting started

This project is provided as a standalone HTML file.

### Option 1: Open directly

1. Download or clone this repository.
2. Open `id-sheet-maker.html` in a modern browser.
3. Upload your documents and follow the three steps:
   - Add documents.
   - Check and adjust.
   - Review and export.

### Option 2: Run with VS Code Live Server

1. Open the project folder in Visual Studio Code.
2. Install the **Live Server** extension if it is not already installed.
3. Right-click `id-sheet-maker.html`.
4. Select **Open with Live Server**.

No build step or package installation is required for the standalone HTML version.

## How to use

1. **Add documents:** Select or drag in your JPG, JPEG, PNG, WebP, or PDF files.
2. **Review detected items:** Check the detected document types and change a type if necessary.
3. **Check and adjust:** Review each document, replace it if needed, or use the adjustment tool to fine-tune it.
4. **Review the sheet:** Check the A4 landscape preview and the validation messages.
5. **Confirm details:** Verify the person's name and edit the suggested PDF filename if required.
6. **Export:** Download the PDF or share it using WhatsApp when your device supports file sharing.

## Technology

The current standalone HTML implementation uses:

- HTML5
- CSS3
- Vanilla JavaScript
- [PDF.js](https://mozilla.github.io/pdf.js/) — PDF document reading and page rendering
- [jsPDF](https://github.com/parallax/jsPDF) — PDF generation
- [Tesseract.js](https://tesseract.projectnaptha.com/) — English OCR for text recognition
- IBM Plex Sans and IBM Plex Mono — interface typography

The PDF.js and jsPDF libraries are loaded from cdnjs. Tesseract.js and its OCR worker/language resources are loaded from jsDelivr when OCR is needed. The interface font is loaded from Google Fonts.

## Privacy

Uploaded documents are processed in the browser for document detection, image adjustment, preview, and PDF generation. The application does not include a project-owned upload server or backend API for storing your documents.

**Important:** The optional **Check with Claude** feature, when available and enabled in a supported Claude environment, sends reduced copies of the document crops to Claude for additional checks. External libraries and fonts are also loaded from their respective CDNs. For the most private use, do not enable optional external analysis and review your browser's network activity and deployment configuration.

## Browser support

Use a recent version of a modern browser such as:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

Some features depend on browser support:

- Direct file sharing requires a browser/device that supports sharing files through the Web Share API.
- When direct file sharing is unavailable, the PDF is downloaded so it can be attached manually in WhatsApp.
- An internet connection is required to load the externally hosted libraries, OCR resources, and web font unless you configure local copies.

## Project structure

```text
id-sheet-maker/
└── id-sheet-maker.html
```

If you add local assets, scripts, stylesheets, or documentation later, update this section to reflect the actual repository structure.

## Contributing

Suggestions, bug reports, and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test uploads, document adjustment, preview, PDF export, and mobile layouts.
5. Open a pull request describing your changes.

Please avoid committing real identity documents, personal information, API credentials, or other sensitive files.

## License

No license is currently specified. Add a `LICENSE` file before presenting this project as open source or granting reuse rights.
