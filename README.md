# RAG-LLM Lossless Data Compressor

A web-based and CLI interface for lossless data compression using RAG (Retrieval-Augmented Generation) and Large Language Models.

## 📋 Features

- **Instant Web Compression** - Fast gzip-based compression with beautiful UI
- **LLM-Based Compression** - Natural language compression using GPT-2/DistilGPT2
- **RAG-Enhanced Compression** - Context-aware compression with retrieval
- **Image/Audio Compression** - Multimedia compression using BGPT
- **Download Results** - Export compressed files easily
- **Statistics Dashboard** - View compression ratios and performance metrics

## 🎯 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/RAG-compressor.git
cd RAG-compressor

# Install dependencies
pip install -r requirements.txt

# Launch web interface
python gradio_app_instant.py
```

### Usage

**Web Interface (Instant):**
```bash
python gradio_app_instant.py
```

**CLI - LLM Compression:**
```bash
python LLMCompress.py input.txt output.llmzip
```

**CLI - RAG Compression:**
```bash
python RAG_LLMCompress.py input.txt output.llmzip
```

**CLI - Image/Audio Compression:**
```bash
python BGPTCompress.py input.bmp output.bgpt
```

## 📊 Performance

| Method | Speed | Ratio (text) | Use Case |
|--------|-------|--------------|----------|
| gzip (web) | < 1s | 2-4x | Quick testing, demos |
| LLM (CLI) | 5-30s | 2-5x | Natural language |
| RAG-LLM (CLI) | 10-60s | 2-6x | Context-rich text |
| BGPT (CLI) | Variable | Varies | Images, audio |

## 🛠️ Technology Stack

- **Frontend:** Gradio 3.50.2
- **Backend:** Python 3.9+
- **ML Models:** GPT-2, DistilGPT2, BGPT
- **Compression:** Arithmetic coding, gzip
- **RAG:** Custom retrieval implementation

## 📁 Project Structure

```
RAG-compressor/
├── gradio_app_instant.py    # Web interface (instant gzip)
├── gradio_app.py             # Web interface (LLM-based)
├── LLMCompress.py            # CLI LLM compression
├── RAG_LLMCompress.py        # CLI RAG compression
├── BGPTCompress.py           # CLI image/audio compression
├── naive_rag.py              # RAG implementation
├── arithmetic_coder/         # Arithmetic coding utilities
├── bgpt/                     # BGPT model implementation
├── notebooks/                # Jupyter notebooks
├── requirements.txt          # Python dependencies
├── DEPLOYMENT.md            # Deployment guide
└── QUICKSTART.md            # Quick start guide
```

## 🔧 Configuration

Edit `gradio_app_instant.py` to customize:
- Server port (default: 7862)
- Max text length (default: 50,000 chars)
- Compression level
- UI theme colors

## 🐛 Known Issues

- LLM compression is slow on CPU (requires GPU for optimal performance)
- Large files may cause memory issues
- Some models require significant disk space

## 🔮 Future Work

- [ ] GPU acceleration for web interface
- [ ] Support for more file formats
- [ ] Improved RAG retrieval algorithms
- [ ] Deploy to Hugging Face Spaces
- [ ] Add user authentication
- [ ] Batch processing support


---
