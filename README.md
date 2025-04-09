# 🧼 PDFWipe

_Bash script to convert a PDF into an image-based PDF to disable text selection and copy-paste._

<p align="center">
  <img src="pdfwipe.png" alt="PDFWipe Logo" width="400"/>
</p>

---

## 📄 What is PDFWipe?

**PDFWipe** converts any PDF into a version where each page is rendered as an image and recompiled into a new PDF.  
This makes the content non-selectable and disables standard text copying.

⚠️ This is **not** a secure or foolproof method — tools with OCR can still extract the content. It’s just a quick workaround for basic protection needs.

---

## 🔧 Requirements

Make sure you have the following installed:

- 🐚 `bash`
- 🧩 `pdftoppm` (from `poppler-utils`)
- 🖼️ `convert` (from `ImageMagick`)
- 🔍 `fzf` (optional, for file selection)

### 📦 Install on Ubuntu/Debian:

```bash
sudo apt update
sudo apt install -y poppler-utils imagemagick fzf
```

---

## 🚀 Usage

### 🖱️ Interactive Mode

```bash
./pdfwipe
```

Opens a file selector using `fzf` and guides you through the process.

---

### 📂 Direct File Mode

```bash
./pdfwipe yourfile.pdf
```

Processes `yourfile.pdf` and outputs `yourfile-pdfwipe.pdf` in the parent directory.

If that file already exists, it will be overwritten.

---

## 👨‍💻 Author

Developed by [mgrl39](https://github.com/mgrl39)

---

## 📝 Notes

- ✅ Original PDF is not modified.
- 🚫 Text selection and copying are disabled in the new PDF.
- 🔍 This does **not** prevent OCR or other advanced extraction methods.
