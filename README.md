# AI & LLM Datasets Collection

A curated collection of datasets for AI and Large Language Model (LLM) training, covering text, images, audio, video, and multimodal data.

## 📚 Overview

This repository serves as a comprehensive catalog and reference guide for publicly available datasets used in AI research and development. Whether you're training large language models, building computer vision systems, or working on multimodal AI, you'll find relevant datasets organized by category.

## 🗂️ Dataset Categories

- **[Text](datasets/text/)** - Language models, NLP, code, instruction datasets
- **[Image](datasets/image/)** - Computer vision, object detection, segmentation
- **[Audio](datasets/audio/)** - Speech recognition, speaker identification, music
- **[Video](datasets/video/)** - Action recognition, video classification, temporal analysis
- **[Multimodal](datasets/multimodal/)** - Image-text, video-text, audio-visual datasets
- **[Structured](datasets/structured/)** - Knowledge graphs, tables, benchmarks

## 🚀 Quick Start

1. Browse the **[Dataset Catalog](CATALOG.md)** for a comprehensive list of all datasets
2. Navigate to category-specific directories for detailed information
3. Check individual dataset markdown files for specifications, usage examples, and citations

## 📖 Documentation

- **[CATALOG.md](CATALOG.md)** - Complete dataset catalog with descriptions and links
- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Guidelines for adding new datasets

## 🔍 Popular Datasets

### For Training LLMs
- [Common Crawl](datasets/text/common-crawl.md) - Web-scale text data
- [The Pile](datasets/text/the-pile.md) - 825GB diverse text corpus
- RedPajama - Open reproduction of LLaMA training data
- C4 - Cleaned Common Crawl

### For Vision Models
- [ImageNet](datasets/image/imagenet.md) - 14M+ labeled images
- COCO - Object detection and segmentation
- LAION-5B - 5 billion image-text pairs

### For Speech & Audio
- LibriSpeech - 1000 hours of speech
- Common Voice - Multilingual speech dataset

## 💡 How to Use

### Finding Datasets
1. Identify your task (classification, generation, etc.)
2. Check the relevant category directory
3. Review dataset specifications and licenses
4. Follow download instructions from official sources

### Using Datasets
Most datasets can be accessed through:
- **HuggingFace Datasets**: `datasets.load_dataset()`
- **TensorFlow Datasets**: `tfds.load()`
- **PyTorch Datasets**: `torchvision.datasets`, `torchaudio.datasets`
- **Direct Download**: From official sources

## 🤝 Contributing

We welcome contributions! Please read [CONTRIBUTING.md](CONTRIBUTING.md) to learn how to:
- Add new datasets to the catalog
- Update existing dataset information
- Report broken links or outdated information

## ⚖️ License & Ethics

- This repository catalogs publicly available datasets and links to their sources
- Each dataset has its own license terms - always verify before use
- Be mindful of ethical considerations: bias, privacy, copyright
- Respect terms of service and usage restrictions

## 🔗 Additional Resources

- [HuggingFace Datasets](https://huggingface.co/datasets)
- [TensorFlow Datasets](https://www.tensorflow.org/datasets)
- [Papers With Code Datasets](https://paperswithcode.com/datasets)
- [Google Dataset Search](https://datasetsearch.research.google.com/)
- [AWS Open Data](https://registry.opendata.aws/)

## 📝 Notes

- Dataset sizes are approximate and may vary by version
- Links and availability may change over time
- Always cite original sources when using datasets
- Some datasets require registration or approval

---

**Disclaimer**: This repository provides references and information about publicly available datasets. We do not host or distribute the datasets themselves. Users are responsible for complying with individual dataset licenses and terms of use.
