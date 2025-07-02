# 🧠 AI-Mashup: Professional Model Merger

**AI-Mashup** is a sophisticated model merging platform that combines multiple AI models into powerful custom hybrids. Features a professional 3-panel interface with real-time progress tracking and advanced merge algorithms.

![AI-Mashup Interface](https://img.shields.io/badge/Interface-Professional%203--Panel-blue?style=for-the-badge)
![Model Support](https://img.shields.io/badge/Models-GPT2%20%7C%20Mistral%20%7C%20Llama-green?style=for-the-badge)
![Merge Methods](https://img.shields.io/badge/Methods-Linear%20%7C%20SLERP%20%7C%20TIES%20%7C%20DARE-orange?style=for-the-badge)

## ✨ Features

### 🎯 **Professional Model Training Studio**
- **3-Panel Interface**: Model Library, Merge Configuration, and Experiments tracking
- **Real-time Progress**: Live updates on merge operations with visual progress bars
- **Dark Theme**: Professional dark UI optimized for long working sessions

### 🤖 **Advanced Merge Methods**
- **Linear (Model Soup)**: Simple averaging of model weights
- **SLERP**: Spherical Linear Interpolation for geometry preservation
- **TIES**: Task Interference Elimination via Sparsification
- **DARE**: Drop And REscale with advanced dropout techniques

### 📊 **Experiment Management**
- **Progress Tracking**: Real-time monitoring of merge operations
- **Experiment History**: Complete log of all merge attempts
- **Model Download**: Direct download of merged models
- **Status Indicators**: Visual status for running and completed experiments

### 🔧 **Model Library**
- **Architecture Filtering**: Filter by GPT, Mistral, Llama architectures
- **Search Functionality**: Quick model discovery
- **Size Information**: Model size and download requirements
- **Tag System**: Organized categorization of models

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- CUDA-compatible GPU (recommended)
- 8GB+ RAM

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Frankenbuild-labs/AI-Mashup.git
cd AI-Mashup
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Start the backend API**
```bash
python start.py
```

4. **Open the Model Training Studio**
- Open `frontend/model-training-studio-modal.html` in your browser
- Or access via: `http://localhost:5007`

## 🏗️ Architecture

```
AI-Mashup/
├── app.py                    # Main Flask API application
├── start.py                  # Application launcher
├── download_models.py        # Model download utilities
├── requirements.txt          # Python dependencies
├── frontend/
│   └── model-training-studio-modal.html  # Professional UI
├── experiments/
│   └── experiments.json      # Experiment tracking
├── merged_models/           # Output directory for merged models
└── models/                  # Downloaded model storage
```

## 🔧 API Endpoints

### Models
- `GET /api/model-merger/models` - List available models
- `POST /api/model-merger/models/download` - Download a model

### Experiments
- `GET /api/model-merger/experiments` - List experiments
- `POST /api/model-merger/experiments` - Create merge experiment
- `GET /api/model-merger/experiments/{id}` - Get experiment details
- `GET /api/model-merger/experiments/{id}/download` - Download merged model

## 🎮 Usage

### 1. **Select Models**
- Browse the Model Library panel
- Filter by architecture or search by name
- Click "Add to Merge" for 2+ models

### 2. **Configure Merge**
- Set experiment name
- Choose merge method (Linear, SLERP, TIES, DARE)
- Review selected models

### 3. **Start Merge**
- Click "Start Merge" to begin
- Monitor progress in Experiments panel
- Download completed models

## 🧪 Merge Methods Explained

### **Linear (Model Soup)**
Simple averaging of model weights. Best for:
- General purpose merging
- Similar architecture models
- Quick experimentation

### **SLERP (Spherical Linear Interpolation)**
Preserves model geometry during interpolation. Best for:
- Maintaining model characteristics
- Smooth transitions between models
- Similar training domains

### **TIES (Task Interference Elimination)**
Reduces task interference through sparsification. Best for:
- Multi-task models
- Reducing negative transfer
- Specialized domain merging

### **DARE (Drop And REscale)**
Advanced merging with dropout techniques. Best for:
- Large model merging
- Robust performance
- Experimental approaches

## 📈 Performance

- **Merge Speed**: 2-10 minutes per experiment (GPU dependent)
- **Memory Usage**: 4-16GB RAM (model size dependent)
- **Supported Models**: GPT-2, DistilGPT-2, Mistral, Llama families
- **Output Formats**: SafeTensors, HuggingFace compatible

## 🛠️ Configuration

### Environment Variables
```bash
# Optional: Set custom ports
export MODEL_MERGER_PORT=5007
export MODEL_MERGER_HOST=0.0.0.0

# Optional: Set model storage path
export MODEL_STORAGE_PATH=./models
```

### Model Configuration
Edit `app.py` to add custom models:
```python
AVAILABLE_MODELS = {
    'custom-model': {
        'name': 'Custom Model',
        'size': '7B',
        'architecture': 'custom',
        'description': 'Custom model description'
    }
}
```

## 🔬 Advanced Usage

### Custom Merge Parameters
```python
# Example: Custom weight distribution
{
    "name": "Custom Experiment",
    "method": "linear",
    "models": ["gpt2", "distilgpt2"],
    "parameters": {
        "weights": [0.7, 0.3],  # Custom weights
        "normalize": true,
        "dtype": "float16"
    }
}
```

### Batch Processing
```bash
# Process multiple merge configurations
python batch_merge.py --config configs/batch_config.json
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎯 Roadmap

- [ ] **MoE (Mixture of Experts)** merge support
- [ ] **LoRA adapter** merging
- [ ] **Quantization** support (4-bit, 8-bit)
- [ ] **Distributed merging** for large models
- [ ] **Model evaluation** metrics
- [ ] **A/B testing** framework
- [ ] **Docker containerization**
- [ ] **Cloud deployment** guides

## 🆘 Support

- **Issues**: [GitHub Issues](https://github.com/Frankenbuild-labs/AI-Mashup/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Frankenbuild-labs/AI-Mashup/discussions)
- **Wiki**: [Project Wiki](https://github.com/Frankenbuild-labs/AI-Mashup/wiki)

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/Frankenbuild-labs/AI-Mashup?style=social)
![GitHub forks](https://img.shields.io/github/forks/Frankenbuild-labs/AI-Mashup?style=social)
![GitHub issues](https://img.shields.io/github/issues/Frankenbuild-labs/AI-Mashup)
![GitHub license](https://img.shields.io/github/license/Frankenbuild-labs/AI-Mashup)

---

**Made with ❤️ by [Frankenbuild Labs](https://github.com/Frankenbuild-labs)**

*Transform your AI models into something greater than the sum of their parts.*
