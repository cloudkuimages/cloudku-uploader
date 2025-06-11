# ☁️ CloudKu Uploader

**Next-generation file uploader for CloudKuImages - Zero Dependencies, Maximum Performance**

[![npm version](https://img.shields.io/npm/v/cloudku-uploader?style=for-the-badge&logo=npm&color=cb3837)](https://www.npmjs.com/package/cloudku-uploader)
[![downloads](https://img.shields.io/npm/dm/cloudku-uploader?style=for-the-badge&logo=npm&color=blue)](https://www.npmjs.com/package/cloudku-uploader)
[![license](https://img.shields.io/badge/license-Custom%20MIT-green?style=for-the-badge)](LICENSE)
[![bundle size](https://img.shields.io/bundlephobia/minzip/cloudku-uploader?style=for-the-badge&color=orange)](https://bundlephobia.com/package/cloudku-uploader)
[![GitHub stars](https://img.shields.io/github/stars/cloudkuimages/cloudku-uploader?style=for-the-badge&color=yellow)](https://github.com/cloudkuimages/cloudku-uploader)

---

### 🌍 International Support

<div align="center">

[🇺🇸 English](#-english) • [🇮🇩 Bahasa Indonesia](#-bahasa-indonesia) • [🇯🇵 日本語](#-日本語) • [🇵🇹 Português](#-português) • [🇷🇺 Русский](#-русский) • [🇨🇳 中文](#-中文) • [🇪🇸 Español](#-español) • [🇫🇷 Français](#-français) • [🇩🇪 Deutsch](#-deutsch) • [🇰🇷 한국어](#-한국어)

</div>

---

### 🚀 Quick Navigation

<div align="center">
<table>
<tr>
<td align="center" width="120">

**⚡ Quick Start**
<br>
<sub>Get started instantly</sub>

</td>
<td align="center" width="120">

**💡 Examples**
<br>
<sub>Ready-to-use code</sub>

</td>
<td align="center" width="120">

**🔧 API Reference**
<br>
<sub>Complete documentation</sub>

</td>
<td align="center" width="120">

**🌐 Community**
<br>
<sub>Support & discussion</sub>

</td>
<td align="center" width="120">

**🔥 Performance**
<br>
<sub>Speed & reliability</sub>

</td>
</tr>
</table>
</div>

---

## 🇺🇸 English

### ✨ Features

<div align="center">

| 🔧 **Zero Dependencies** | ⚡ **Modern Architecture** | 🛡️ **Smart Fallback** |
|:---:|:---:|:---:|
| Pure JavaScript/TypeScript | Class-based OOP design | Multi-endpoint resilience |

| 🚀 **Native Performance** | 📱 **Universal Compatibility** | 🎯 **Ultra Lightweight** |
|:---:|:---:|:---:|
| Built-in Fetch API | Browser + Node.js + Edge | < 5KB gzipped |

| 🌐 **Global CDN** | 🔒 **Enterprise Security** | ⚡ **Lightning Fast** |
|:---:|:---:|:---:|
| Worldwide availability | Headers & validation | < 100ms response time |

</div>

### 🚀 Installation & Usage

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const result = await uploader.upload(fileBuffer, 'image.jpg')
console.log(`✅ Uploaded: ${result.result.url}`)
```

### 📖 API Reference

```typescript
class CloudKuUploader {
  constructor()
  async upload(fileBuffer: Buffer | Uint8Array, fileName?: string): Promise<UploadResponse>
}

interface UploadResponse {
  status: 'success' | 'error'
  creator: 'AlfiDev'
  information: string
  result?: {
    filename: string
    type: string
    size: string
    url: string
  }
  message?: string
}
```

---

## 🇮🇩 Bahasa Indonesia

### ✨ Fitur Unggulan

<div align="center">

| 🔧 **Zero Dependencies** | ⚡ **Arsitektur Modern** | 🛡️ **Smart Fallback** |
|:---:|:---:|:---:|
| JavaScript/TypeScript murni | Desain OOP berbasis class | Resiliensi multi-endpoint |

| 🚀 **Performa Native** | 📱 **Kompatibilitas Universal** | 🎯 **Sangat Ringan** |
|:---:|:---:|:---:|
| Fetch API bawaan | Browser + Node.js + Edge | < 5KB gzipped |

</div>

### 🚀 Instalasi & Penggunaan

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const hasil = await uploader.upload(fileBuffer, 'gambar.jpg')
console.log(`✅ Terupload: ${hasil.result.url}`)
```

---

## 🇯🇵 日本語

### ✨ 主要機能

<div align="center">

| 🔧 **依存関係ゼロ** | ⚡ **モダンアーキテクチャ** | 🛡️ **スマートフォールバック** |
|:---:|:---:|:---:|
| 純粋JavaScript/TypeScript | クラスベースOOP設計 | マルチエンドポイント対応 |

| 🚀 **ネイティブパフォーマンス** | 📱 **ユニバーサル互換性** | 🎯 **超軽量** |
|:---:|:---:|:---:|
| 組み込みFetch API | ブラウザ + Node.js + Edge | < 5KB gzip圧縮 |

</div>

### 🚀 インストール & 使用法

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const result = await uploader.upload(fileBuffer, 'image.jpg')
console.log(`✅ アップロード完了: ${result.result.url}`)
```

---

## 🇵🇹 Português

### ✨ Recursos Principais

<div align="center">

| 🔧 **Zero Dependências** | ⚡ **Arquitetura Moderna** | 🛡️ **Fallback Inteligente** |
|:---:|:---:|:---:|
| JavaScript/TypeScript puro | Design OOP baseado em classes | Resiliência multi-endpoint |

| 🚀 **Performance Nativa** | 📱 **Compatibilidade Universal** | 🎯 **Ultra Leve** |
|:---:|:---:|:---:|
| Fetch API integrada | Browser + Node.js + Edge | < 5KB comprimido |

</div>

### 🚀 Instalação & Uso

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const resultado = await uploader.upload(fileBuffer, 'imagem.jpg')
console.log(`✅ Enviado: ${resultado.result.url}`)
```

---

## 🇷🇺 Русский

### ✨ Основные возможности

<div align="center">

| 🔧 **Без зависимостей** | ⚡ **Современная архитектура** | 🛡️ **Умный откат** |
|:---:|:---:|:---:|
| Чистый JavaScript/TypeScript | ООП дизайн на основе классов | Устойчивость множественных точек |

| 🚀 **Нативная производительность** | 📱 **Универсальная совместимость** | 🎯 **Ультра легкий** |
|:---:|:---:|:---:|
| Встроенный Fetch API | Браузер + Node.js + Edge | < 5KB сжатый |

</div>

### 🚀 Установка и использование

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const результат = await uploader.upload(fileBuffer, 'изображение.jpg')
console.log(`✅ Загружено: ${результат.result.url}`)
```

---

## 🇨🇳 中文

### ✨ 主要功能

<div align="center">

| 🔧 **零依赖** | ⚡ **现代架构** | 🛡️ **智能回退** |
|:---:|:---:|:---:|
| 纯JavaScript/TypeScript | 基于类的OOP设计 | 多端点弹性 |

| 🚀 **原生性能** | 📱 **通用兼容性** | 🎯 **超轻量级** |
|:---:|:---:|:---:|
| 内置Fetch API | 浏览器 + Node.js + Edge | < 5KB 压缩后 |

</div>

### 🚀 安装和使用

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const 结果 = await uploader.upload(fileBuffer, '图片.jpg')
console.log(`✅ 已上传: ${结果.result.url}`)
```

---

## 🇪🇸 Español

### ✨ Características Principales

<div align="center">

| 🔧 **Cero Dependencias** | ⚡ **Arquitectura Moderna** | 🛡️ **Fallback Inteligente** |
|:---:|:---:|:---:|
| JavaScript/TypeScript puro | Diseño OOP basado en clases | Resistencia multi-endpoint |

| 🚀 **Rendimiento Nativo** | 📱 **Compatibilidad Universal** | 🎯 **Ultra Ligero** |
|:---:|:---:|:---:|
| Fetch API integrado | Navegador + Node.js + Edge | < 5KB comprimido |

</div>

### 🚀 Instalación y Uso

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const resultado = await uploader.upload(fileBuffer, 'imagen.jpg')
console.log(`✅ Subido: ${resultado.result.url}`)
```

---

## 🇫🇷 Français

### ✨ Fonctionnalités Principales

<div align="center">

| 🔧 **Zéro Dépendance** | ⚡ **Architecture Moderne** | 🛡️ **Fallback Intelligent** |
|:---:|:---:|:---:|
| JavaScript/TypeScript pur | Conception OOP basée sur les classes | Résilience multi-endpoint |

| 🚀 **Performance Native** | 📱 **Compatibilité Universelle** | 🎯 **Ultra Léger** |
|:---:|:---:|:---:|
| Fetch API intégré | Navigateur + Node.js + Edge | < 5KB compressé |

</div>

### 🚀 Installation et Utilisation

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const résultat = await uploader.upload(fileBuffer, 'image.jpg')
console.log(`✅ Téléchargé: ${résultat.result.url}`)
```

---

## 🇩🇪 Deutsch

### ✨ Hauptfunktionen

<div align="center">

| 🔧 **Null Abhängigkeiten** | ⚡ **Moderne Architektur** | 🛡️ **Intelligenter Fallback** |
|:---:|:---:|:---:|
| Reines JavaScript/TypeScript | Klassenbasiertes OOP-Design | Multi-Endpoint-Resistenz |

| 🚀 **Native Performance** | 📱 **Universelle Kompatibilität** | 🎯 **Ultra Leicht** |
|:---:|:---:|:---:|
| Eingebaute Fetch API | Browser + Node.js + Edge | < 5KB komprimiert |

</div>

### 🚀 Installation und Verwendung

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const ergebnis = await uploader.upload(fileBuffer, 'bild.jpg')
console.log(`✅ Hochgeladen: ${ergebnis.result.url}`)
```

---

## 🇰🇷 한국어

### ✨ 주요 기능

<div align="center">

| 🔧 **의존성 제로** | ⚡ **모던 아키텍처** | 🛡️ **스마트 폴백** |
|:---:|:---:|:---:|
| 순수 JavaScript/TypeScript | 클래스 기반 OOP 설계 | 다중 엔드포인트 복원력 |

| 🚀 **네이티브 성능** | 📱 **범용 호환성** | 🎯 **초경량** |
|:---:|:---:|:---:|
| 내장 Fetch API | 브라우저 + Node.js + Edge | < 5KB 압축 |

</div>

### 🚀 설치 및 사용법

```bash
npm install cloudku-uploader
```

```javascript
import CloudKuUploader from 'cloudku-uploader'

const uploader = new CloudKuUploader()
const 결과 = await uploader.upload(fileBuffer, '이미지.jpg')
console.log(`✅ 업로드됨: ${결과.result.url}`)
```

---

## 💻 Code Examples

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
      console.log('🎉 Success!')
      console.log('📎 URL:', result.result.url)
      console.log('📊 Size:', result.result.size)
      console.log('📄 Type:', result.result.type)
    }
  } catch (error) {
    console.error('❌ Upload failed:', error.message)
  }
}

uploadImage()
```

### 🔄 Batch Upload

```javascript
import CloudKuUploader from 'cloudku-uploader'
import { readFileSync, readdirSync } from 'fs'
import { join } from 'path'

const uploader = new CloudKuUploader()

async function batchUpload(folderPath) {
  const files = readdirSync(folderPath)
  const results = []
  
  for (const filename of files) {
    try {
      const buffer = readFileSync(join(folderPath, filename))
      console.log(`📤 Uploading: ${filename}`)
      
      const result = await uploader.upload(buffer, filename)
      
      if (result.status === 'success') {
        results.push({
          filename: result.result.filename,
          url: result.result.url,
          size: result.result.size,
          originalName: filename
        })
        console.log(`✅ ${filename} uploaded successfully`)
      }
    } catch (error) {
      console.error(`❌ Failed to upload ${filename}:`, error.message)
    }
  }
  
  return results
}

// Usage
const uploadedFiles = await batchUpload('./uploads')
console.table(uploadedFiles)
```

### ⚡ Express.js Integration

```javascript
import express from 'express'
import multer from 'multer'
import CloudKuUploader from 'cloudku-uploader'
import cors from 'cors'
import helmet from 'helmet'
import rateLimit from 'express-rate-limit'

const app = express()
const upload = multer({ 
  limits: { 
    fileSize: 100 * 1024 * 1024, // 100MB
    files: 10 // Max 10 files
  }
})
const uploader = new CloudKuUploader()

// Security middleware
app.use(helmet())
app.use(cors({
  origin: process.env.ALLOWED_ORIGINS?.split(',') || ['http://localhost:3000'],
  credentials: true
}))

// Rate limiting
const uploadLimiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 100, // Limit each IP to 100 uploads per windowMs
  message: { error: 'Too many uploads, please try again later.' }
})

app.use('/upload', uploadLimiter)

// Single file upload
app.post('/upload', upload.single('file'), async (req, res) => {
  try {
    if (!req.file) {
      return res.status(400).json({ 
        success: false, 
        error: 'No file provided' 
      })
    }

    const result = await uploader.upload(req.file.buffer, req.file.originalname)
    
    if (result.status === 'success') {
      res.json({ 
        success: true, 
        data: {
          url: result.result.url,
          filename: result.result.filename,
          size: result.result.size,
          type: result.result.type,
          uploadedAt: new Date().toISOString()
        }
      })
    } else {
      throw new Error(result.message)
    }
  } catch (error) {
    console.error('Upload error:', error)
    res.status(500).json({ 
      success: false, 
      error: 'Upload failed',
      message: error.message 
    })
  }
})

// Multiple files upload
app.post('/upload-batch', upload.array('files', 10), async (req, res) => {
  try {
    if (!req.files || req.files.length === 0) {
      return res.status(400).json({ 
        success: false, 
        error: 'No files provided' 
      })
    }

    const uploadPromises = req.files.map(file => 
      uploader.upload(file.buffer, file.originalname)
    )
    
    const results = await Promise.allSettled(uploadPromises)
    const successful = results
      .filter(result => result.status === 'fulfilled' && result.value.status === 'success')
      .map(result => ({
        url: result.value.result.url,
        filename: result.value.result.filename,
        size: result.value.result.size,
        type: result.value.result.type
      }))

    const failed = results.filter(result => 
      result.status === 'rejected' || 
      (result.status === 'fulfilled' && result.value.status === 'error')
    ).length

    res.json({ 
      success: true, 
      data: {
        uploaded: successful,
        total: req.files.length,
        successful: successful.length,
        failed: failed,
        uploadedAt: new Date().toISOString()
      }
    })
  } catch (error) {
    console.error('Batch upload error:', error)
    res.status(500).json({ 
      success: false, 
      error: 'Batch upload failed',
      message: error.message 
    })
  }
})

// Health check
app.get('/health', (req, res) => {
  res.json({ 
    status: 'healthy', 
    timestamp: new Date().toISOString(),
    service: 'CloudKu Upload Service'
  })
})

const PORT = process.env.PORT || 3000
app.listen(PORT, () => {
  console.log('🚀 CloudKu Upload Server running on port', PORT)
  console.log('📋 Endpoints available:')
  console.log('  POST /upload - Single file upload')
  console.log('  POST /upload-batch - Multiple files upload')
  console.log('  GET /health - Health check')
})

export default app
```

### 🔧 Advanced Error Handling & Retry Logic

```javascript
import CloudKuUploader from 'cloudku-uploader'

class RobustUploader {
  constructor(options = {}) {
    this.uploader = new CloudKuUploader()
    this.maxRetries = options.maxRetries || 3
    this.retryDelay = options.retryDelay || 1000
    this.backoffMultiplier = options.backoffMultiplier || 2
  }

  async uploadWithRetry(fileBuffer, fileName, options = {}) {
    const { 
      maxRetries = this.maxRetries,
      onProgress = () => {},
      onRetry = () => {}
    } = options

    let lastError
    
    for (let attempt = 1; attempt <= maxRetries; attempt++) {
      try {
        onProgress({ attempt, maxRetries, status: 'uploading' })
        
        const result = await this.uploader.upload(fileBuffer, fileName)
        
        if (result.status === 'success') {
          onProgress({ attempt, maxRetries, status: 'success', result })
          return result
        }
        
        throw new Error(result.message || 'Upload failed')
      } catch (error) {
        lastError = error
        
        if (attempt < maxRetries) {
          const delay = this.retryDelay * Math.pow(this.backoffMultiplier, attempt - 1)
          
          onRetry({ 
            attempt, 
            maxRetries, 
            error: error.message, 
            retryIn: delay 
          })
          
          await this.delay(delay)
        }
      }
    }
    
    throw new Error(`Upload failed after ${maxRetries} attempts: ${lastError.message}`)
  }

  async delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms))
  }

  // Upload with progress tracking
  async uploadWithProgress(fileBuffer, fileName) {
    return this.uploadWithRetry(fileBuffer, fileName, {
      onProgress: ({ attempt, maxRetries, status, result }) => {
        switch (status) {
          case 'uploading':
            console.log(`📤 Attempt ${attempt}/${maxRetries}: Uploading ${fileName}...`)
            break
          case 'success':
            console.log(`✅ Upload successful: ${result.result.url}`)
            break
        }
      },
      onRetry: ({ attempt, maxRetries, error, retryIn }) => {
        console.log(`⚠️  Attempt ${attempt}/${maxRetries} failed: ${error}`)
        console.log(`🔄 Retrying in ${retryIn}ms...`)
      }
    })
  }
}

// Usage
const robustUploader = new RobustUploader({
  maxRetries: 5,
  retryDelay: 1000,
  backoffMultiplier: 2
})

try {
  const result = await robustUploader.uploadWithProgress(fileBuffer, 'important-file.jpg')
  console.log('🎉 Final result:', result)
} catch (error) {
  console.error('💥 Upload completely failed:', error.message)
}
```

## 📊 Supported File Types & Limits

<div align="center">

| Category | File Types | Max Size | Recommended |
|----------|------------|----------|-------------|
| **🖼️ Images** | jpg, jpeg, png, gif, webp, svg, bmp, ico | 100 MB | ✅ Optimized |
| **📄 Documents** | pdf, doc, docx, txt, md, rtf, odt | 50 MB | ✅ Full support |
| **🗜️ Archives** | zip, rar, 7z, tar, gz, bz2 | 200 MB | ✅ All formats |
| **🎵 Audio** | mp3, wav, ogg, flac, aac, m4a | 100 MB | ✅ High quality |
| **🎬 Video** | mp4, avi, mov, mkv, webm, flv | 500 MB | ✅ HD support |
| **💻 Code** | js, ts, py, html, css, json, xml | 10 MB | ✅ Syntax highlight |
| **📊 Data** | csv, xlsx, xls, sql, db | 25 MB | ✅ Structured data |

</div>

## 🌐 Browser & Platform Compatibility

### Modern Browser Support
- ✅ **Chrome/Chromium** 88+ (2021+)
- ✅ **Firefox** 85+ (2021+)
- ✅ **Safari** 14+ (2020+)
- ✅ **Edge** 88+ (2021+)
- ✅ **Opera** 74+ (2021+)

### Runtime Environments
- ✅ **Node.js** 16+ (LTS recommended)
- ✅ **Deno** 1.20+
- ✅ **Bun** 0.6+
- ✅ **Vercel Edge Runtime**
- ✅ **Cloudflare Workers**
- ✅ **AWS Lambda** (Node.js runtime)

### Hosting Platforms
- ✅ **Vercel** - Full support
- ✅ **Netlify** - Full support  
- ✅ **Railway** - Full support
- ✅ **Heroku** - Full support
- ✅ **DigitalOcean** - Full support
- ✅ **AWS** (EC2, Lambda, ECS) - Full support
- ✅ **Google Cloud** (GCE, Cloud Run) - Full support
- ✅ **Azure** (App Service, Functions) - Full support

## ⚡ Performance Metrics

<div align="center">

| Metric | Value | Notes |
|--------|-------|-------|
| **Bundle Size** | < 5KB | Minified + Gzipped |
| **Cold Start** | < 50ms | First upload initialization |
| **Upload Speed** | > 10MB/s | On good connection |
| **Response Time** | < 100ms | Server response average |
| **Success Rate** | > 99.9% | With fallback system |
| **Memory Usage** | < 1MB | Per upload operation |

</div>

## 🔒 Security Features

### Built-in Security Headers
```javascript
{
  'x-content-type-options': 'nosniff',
  'x-frame-options': 'DENY', 
  'x-xss-protection': '0',
  'referrer-policy': 'strict-origin-when-cross-origin',
  'content-security-policy': 'default-src \'self\''
}
```

### File Validation
- ✅ **MIME Type Validation** - Server-side verification
- ✅ **File Size Limits** - Configurable per file type
- ✅ **Extension Checking** - Whitelist approach
- ✅ **Content Scanning** - Malware detection
- ✅ **Rate Limiting** - Abuse prevention

## 🌐 CDN & Infrastructure

### Global Edge Locations
- 🌍 **Primary**: `cloudkuimages.guru`
- 🌎 **Backup**: `cloudkuimages-guru.us.itpanel.app`
- 🗺️ **Coverage**: 200+ locations worldwide
- ⚡ **Latency**: < 50ms average globally

### High Availability
- 🔄 **Auto Failover** - Seamless endpoint switching
- 📊 **Load Balancing** - Intelligent traffic distribution  
- 🛡️ **DDoS Protection** - Enterprise-grade security
- 📈 **99.99% Uptime** - SLA guaranteed

## 📞 Support & Community

<div align="center">

| Resource | Link | Description |
|----------|------|-------------|
| 🌐 **Official Website** | [cloudkuimages.guru](https://cloudkuimages.guru) | Main platform |
| 📦 **NPM Package** | [npm/cloudku-uploader](https://www.npmjs.com/package/cloudku-uploader) | Package repository |
| 💬 **WhatsApp Support** | [Contact Us](https://cloudkuimages.guru/ch) | Direct support |
| 📚 **Documentation** | [GitHub Wiki](https://github.com/cloudkuimages/cloudku-uploader) | Complete guides |
| 🐛 **Bug Reports** | [GitHub Issues](https://github.com/cloudkuimages/uploader/issues) | Report bugs |
| 💡 **Feature Requests** | [GitHub Discussions](https://github.com/cloudkuimages/cloudku-uploader/discussions) | Suggest features |

</div>

## 📜 License

This project is licensed under a **Custom MIT License**.

### ⚠️ Important License Terms:
- ✅ **Personal Use** - Completely free
- ✅ **Open Source Projects** - Free with attribution
- ⚠️ **Commercial Use** - Requires permission
- ❌ **Redistribution** - Contact for licensing

## 🚀 What's New

### Version 2.0+ Features
- 🎯 **Zero Dependencies** - Pure JavaScript implementation
- ⚡ **Modern Architecture** - ES6+ class-based design  
- 🛡️ **Enhanced Security** - Advanced validation & headers
- 🌐 **Global CDN** - Multi-region redundancy
- 📱 **Universal Support** - Browser + Server environments
- 🔧 **TypeScript Ready** - Full Support for TypeScript
- 📊 **Improved Performance** - Optimized for speed & efficiency

<div align="center">

**Made with ❤️ by [AlfiDev](https://github.com/cloudkuimages)**

*Empowering developers with reliable, dependency-free file uploads*

</div>
