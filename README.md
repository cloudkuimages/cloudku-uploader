# ☁️ CloudKu Uploader

<div align="center">

**Modern class-based file uploader for CloudKuImages - Zero Dependencies**

[![npm version](https://img.shields.io/npm/v/cloudku-uploader?style=for-the-badge&logo=npm&color=cb3837)](https://www.npmjs.com/package/cloudku-uploader)
[![downloads](https://img.shields.io/npm/dm/cloudku-uploader?style=for-the-badge&logo=npm&color=blue)](https://www.npmjs.com/package/cloudku-uploader)
[![license](https://img.shields.io/badge/license-Custom%20MIT-green?style=for-the-badge)](LICENSE)
[![size](https://img.shields.io/bundlephobia/min/cloudku-uploader?style=for-the-badge&color=orange)](https://bundlephobia.com/package/cloudku-uploader)

[🇺🇸 English](#english) • [🇮🇩 Bahasa Indonesia](#bahasa-indonesia) • [🚀 Quick Start](#quick-start) • [💡 Examples](#examples)

</div>

---

## 🇺🇸 English

### ✨ Features

🔧 **Pure JavaScript** - No external dependencies  
⚡ **Class-based** - Modern OOP architecture  
🛡️ **Auto Fallback** - Multiple server endpoints  
🚀 **Native Fetch** - Built-in browser/Node.js support  
📱 **Universal** - Works in browser and Node.js  
🎯 **Lightweight** - Ultra-minimal footprint

### 🚀 Quick Start

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const result = await uploader.upload(fileBuffer, 'image.jpg')
console.log(`Uploaded: ${result.result.url}`)
```

### 📖 API Reference

```javascript
class CloudKuUploader {
  constructor()
  async upload(fileBuffer, fileName = 'upload.jpg')
}
```

**Parameters:**
- `fileBuffer` (Buffer/Uint8Array) - File content
- `fileName` (string) - File name with extension

**Returns:** Promise\<UploadResponse\>

### 🔧 Response Interface

```javascript
{
  status: 'success' | 'error',
  creator: 'AlfiDev',
  information: 'https://cloudkuimages.guru/ch',
  result: {
    filename: 'generated-name.jpg',
    type: 'image/jpeg',
    size: '1.2 MB',
    url: 'https://cloudkuimages.guru/file/xxx'
  }
}
```

---

## 🇮🇩 Bahasa Indonesia

### ✨ Fitur Utama

🔧 **JavaScript Murni** - Tanpa ketergantungan eksternal  
⚡ **Berbasis Class** - Arsitektur OOP modern  
🛡️ **Auto Fallback** - Multiple endpoint server  
🚀 **Native Fetch** - Dukungan browser/Node.js bawaan  
📱 **Universal** - Berfungsi di browser dan Node.js  
🎯 **Ringan** - Ukuran file sangat minimal

### 🚀 Mulai Cepat

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const hasil = await uploader.upload(fileBuffer, 'gambar.jpg')
console.log(`Terupload: ${hasil.result.url}`)
```

### 📖 Referensi API

```javascript
class CloudKuUploader {
  constructor()
  async upload(fileBuffer, fileName = 'upload.jpg')
}
```

**Parameter:**
- `fileBuffer` (Buffer/Uint8Array) - Konten file
- `fileName` (string) - Nama file dengan ekstensi

**Mengembalikan:** Promise\<UploadResponse\>

---

## 💡 Examples

### 🖼️ Basic Image Upload

```javascript
import CloudKuUploader from 'cloudku-uploader'
import { readFileSync } from 'fs'

const uploader = new CloudKuUploader()

async function uploadImage() {
  try {
    const imageBuffer = readFileSync('./photo.jpg')
    const result = await uploader.upload(imageBuffer, 'photo.jpg')
    
    if (result.status === 'success') {
      console.log('Image URL:', result.result.url)
      console.log('File Size:', result.result.size)
    }
  } catch (error) {
    console.error('Upload failed:', error.message)
  }
}

uploadImage()
```

### 📄 Browser File Upload

```html
<!DOCTYPE html>
<html>
<head>
  <title>CloudKu Uploader</title>
</head>
<body>
  <input type="file" id="fileInput" accept="image/*">
  <button onclick="uploadFile()">Upload</button>
  <div id="result"></div>

  <script type="module">
    import CloudKuUploader from './cloudku-uploader.js'
    
    const uploader = new CloudKuUploader()
    
    window.uploadFile = async function() {
      const fileInput = document.getElementById('fileInput')
      const file = fileInput.files[0]
      
      if (!file) return alert('Please select a file')
      
      const arrayBuffer = await file.arrayBuffer()
      const result = await uploader.upload(new Uint8Array(arrayBuffer), file.name)
      
      document.getElementById('result').innerHTML = 
        `<a href="${result.result.url}" target="_blank">View Uploaded File</a>`
    }
  </script>
</body>
</html>
```

### 🔄 Multiple Files Upload

```javascript
import CloudKuUploader from 'cloudku-uploader'
import { readFileSync, readdirSync } from 'fs'
import { join } from 'path'

const uploader = new CloudKuUploader()

async function uploadMultiple(folderPath) {
  const files = readdirSync(folderPath)
  const uploadPromises = files.map(async (filename) => {
    const buffer = readFileSync(join(folderPath, filename))
    return uploader.upload(buffer, filename)
  })
  
  const results = await Promise.all(uploadPromises)
  return results.map(r => r.result.url)
}

const urls = await uploadMultiple('./uploads')
console.log('All files uploaded:', urls)
```

### ⚡ Express.js Integration

```javascript
import express from 'express'
import multer from 'multer'
import CloudKuUploader from 'cloudku-uploader'

const app = express()
const upload = multer()
const uploader = new CloudKuUploader()

app.post('/upload', upload.single('file'), async (req, res) => {
  try {
    const result = await uploader.upload(req.file.buffer, req.file.originalname)
    res.json({ success: true, url: result.result.url })
  } catch (error) {
    res.status(500).json({ success: false, error: error.message })
  }
})

app.listen(3000, () => console.log('Server running on port 3000'))
```

### 🎯 Advanced Error Handling

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()

async function robustUpload(fileBuffer, fileName, maxRetries = 3) {
  for (let attempt = 1; attempt <= maxRetries; attempt++) {
    try {
      const result = await uploader.upload(fileBuffer, fileName)
      
      if (result.status === 'success') {
        return result
      }
      
      throw new Error(result.message || 'Upload failed')
    } catch (error) {
      console.log(`Attempt ${attempt}/${maxRetries} failed:`, error.message)
      
      if (attempt === maxRetries) {
        throw new Error(`Upload failed after ${maxRetries} attempts: ${error.message}`)
      }
      
      await new Promise(resolve => setTimeout(resolve, 1000 * attempt))
    }
  }
}
```

## 📊 Supported File Types

| Category | Extensions | Max Size |
|----------|------------|----------|
| **Images** | jpg, png, gif, webp, svg, bmp | 100MB |
| **Documents** | pdf, doc, docx, txt, md, rtf | 25MB |
| **Archives** | zip, rar, 7z, tar, gz | 50MB |
| **Media** | mp4, mp3, avi, mov, wav | 100MB |
| **Code** | js, ts, py, php, html, css, json | 5MB |

## 🔧 Technical Details

### Auto Fallback System
The uploader automatically tries multiple endpoints:
1. `https://cloudkuimages.guru/upload.php` (Primary)
2. `https://cloudkuimages-guru.us.itpanel.app/upload.php` (Backup)

### Browser Compatibility
- ✅ Chrome 42+
- ✅ Firefox 39+
- ✅ Safari 10.1+
- ✅ Edge 14+
- ✅ Node.js 18+

### Security Headers
All uploads include security headers:
- `x-content-type-options: nosniff`
- `x-frame-options: DENY`
- `x-xss-protection: 0`
- `referrer-policy: strict-origin-when-cross-origin`

## 🌐 Links

| Resource | URL |
|----------|-----|
| 🌐 **CloudKu Images** | [cloudkuimages.guru](https://cloudkuimages.guru) |
| 📦 **NPM Package** | [npmjs.com/package/cloudku-uploader](https://www.npmjs.com/package/cloudku-uploader) |
| 💬 **Support Channel** | [WhatsApp](https://cloudkuimages.guru/ch) |
| 📚 **Documentation** | [GitHub Wiki](https://github.com/cloudkuimages/uploader/wiki) |

## 📜 License

This project is licensed under a **Custom MIT License**.

⚠️ **Important**: Commercial use and redistribution require permission.

---

<div align="center">

**Made with ❤️ by [AlfiDev](https://github.com/cloudkuimages)**

*Empowering developers with reliable, dependency-free file uploads*

</div>
