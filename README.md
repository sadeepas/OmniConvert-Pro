# OmniConvert-Pro
A modern, privacy-focused, client-side file converter built with vanilla JavaScript. Features drag-and-drop batch processing, image optimization, image-to-PDF conversion, and automatic ZIP bundling—all without a server.

# ⚡ OmniConvert Pro

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Web-orange)
![Privacy](https://img.shields.io/badge/privacy-100%25%20Local-green)

**OmniConvert Pro** is a lightweight, browser-based file conversion tool that runs entirely on the client side. It allows users to convert images and documents, process files in batches, and download results as a ZIP archive—ensuring data privacy since files never leave the user's device.

## ✨ Features

- **🚀 100% Client-Side:** No server uploads required. All processing happens locally in the browser for maximum privacy and speed.
- **📂 Batch Processing:** Upload multiple files at once and convert them in a single click.
- **📦 Auto-ZIP Bundling:** Automatically zips multiple converted files for a single, convenient download.
- **🖼️ Image Conversion:** Supports PNG, JPG, WEBP, BMP, GIF, and ICO (Favicon).
- **📄 Document Support:** Instantly converts Images and Text files to PDF.
- **🎨 Modern UI:** Fully responsive Dark Mode design with glassmorphism effects and smooth animations.
- **🎛️ Quality Control:** Adjustable output quality settings (Low, Medium, High, Original) to manage file size.

## 🛠️ Tech Stack

- **HTML5 & CSS3** (CSS Variables, Flexbox, Grid, Animations)
- **Vanilla JavaScript** (ES6+)
- **External Libraries (via CDN):**
  - [jsPDF](https://github.com/parallax/jsPDF) (PDF Generation)
  - [JSZip](https://github.com/Stuk/jszip) (File Bundling)
  - [FileSaver.js](https://github.com/eligrey/FileSaver.js) (Download Handling)
  - [FontAwesome](https://fontawesome.com/) (Icons)
  - [Google Fonts](https://fonts.google.com/) (Plus Jakarta Sans)

## 🚀 Getting Started

### Prerequisites
You need a modern web browser (Chrome, Firefox, Edge, Safari). No Node.js or backend server is required.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/omniconvert-pro.git
   ```

2. **Open the project:**
   Simply double-click `index.html` to open it in your browser.

   *Note: For the best experience (and to avoid local CORS issues with some specific canvas operations), it is recommended to run it via a local server.*

   **Using VS Code Live Server:**
   - Right-click `index.html` -> "Open with Live Server".

   **Using Python:**
   ```bash
   cd omniconvert-pro
   python -m http.server 8000
   ```

## 📖 How It Works

1. **Upload:** Users drag and drop files into the drop zone.
2. **Select Format:** The user selects the target format (e.g., JPG to PNG, or Image to PDF).
3. **Processing:**
   - **Images:** Uses the HTML5 Canvas API to redraw images and export them as blobs with specific MIME types.
   - **PDFs:** Uses `jsPDF` to calculate aspect ratios and embed images onto PDF pages.
4. **Download:** 
   - Single files download immediately.
   - Multiple files are added to a `JSZip` instance and generated as a compressed `.zip` folder.

## ⚠️ Current Limitations

- **Video/Audio Conversion:** The UI includes options for MP4, MP3, etc., but in this lightweight version, these act as **passthrough/demo** modes (files are cloned but not transcoded). Real video encoding requires a heavier library like `ffmpeg.wasm`.
- **Memory:** Since processing is client-side, trying to convert hundreds of high-res files simultaneously may depend on the user's available RAM.

## 🤝 Contributing

Contributions are welcome! If you'd like to integrate `ffmpeg.wasm` for real video transcoding or add more document formats:

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

  Built with ❤️ by [Your Name]
</p>
```
