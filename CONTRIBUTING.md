# Contributing to the Datasets Collection

Thank you for your interest in contributing to this dataset collection! This document provides guidelines for adding datasets and maintaining the catalog.

## How to Contribute

### Adding a New Dataset

1. **Fork and Clone**: Fork this repository and clone it to your local machine
2. **Choose Category**: Determine which category your dataset belongs to:
   - `datasets/text/` - Text-based datasets (NLP, LLM training, etc.)
   - `datasets/image/` - Image datasets
   - `datasets/audio/` - Audio and speech datasets
   - `datasets/video/` - Video datasets
   - `datasets/multimodal/` - Datasets with multiple modalities
   - `datasets/structured/` - Structured data (tables, knowledge graphs, etc.)

3. **Create Dataset Info**: Create a markdown file in the appropriate subdirectory with the following structure:

```markdown
# Dataset Name

## Overview
Brief description of the dataset

## Specifications
- **Size**: Approximate size
- **Format**: File formats (JSON, CSV, Parquet, etc.)
- **License**: License type
- **Language**: If applicable
- **Domain**: Application domain

## Source
- Official website: [link]
- Download: [link]
- Paper/Documentation: [link]

## Statistics
- Number of samples
- Data distribution
- Other relevant metrics

## Usage
Brief description of how to download and use the dataset

### Example Code
```python
# Example of loading the dataset
```

## Citation
```
BibTeX citation if available
```

## Notes
Any additional notes, limitations, or considerations
```

4. **Update CATALOG.md**: Add an entry to the main `CATALOG.md` file in the appropriate section

5. **Test Links**: Verify all links work correctly

6. **Submit PR**: Create a pull request with a clear description of the dataset being added

### Dataset Information Guidelines

When adding a dataset, please ensure:

- **Accuracy**: All information is accurate and up-to-date
- **Completeness**: Include all required fields
- **License Compliance**: Clearly state the license and any usage restrictions
- **Ethical Considerations**: Note any ethical concerns or biases
- **Accessibility**: Provide clear instructions for accessing the dataset
- **Citations**: Include proper citations to original sources

### What to Include

✅ **DO Include**:
- Publicly available datasets
- Datasets with clear licensing
- Datasets commonly used in research/industry
- Open-source datasets
- Datasets with proper documentation
- Links to official sources

❌ **DON'T Include**:
- Proprietary datasets without permission
- Datasets with unclear licensing
- Datasets containing private/personal information without consent
- Illegal or unethically collected data
- Direct file uploads (use links instead)
- Datasets with restrictive terms that prevent sharing information about them

## Dataset Categories

### Text Datasets
- Language models and LLM training data
- Question answering
- Instruction and chat datasets
- Code datasets
- Translation datasets
- Summarization datasets
- Classification datasets

### Image Datasets
- Classification
- Object detection
- Segmentation
- Generation
- Face recognition
- Medical imaging

### Audio Datasets
- Speech recognition
- Speaker identification
- Music analysis
- Audio classification
- Text-to-speech

### Video Datasets
- Action recognition
- Video classification
- Temporal analysis
- Video captioning

### Multimodal Datasets
- Image-text pairs
- Video-text pairs
- Audio-visual datasets

### Structured Data
- Knowledge graphs
- Tables
- Benchmarks
- Scientific data

## Quality Standards

Contributions should:
- Use clear, concise language
- Follow the markdown format guidelines
- Include working links
- Provide accurate information
- Follow proper citation practices

## Review Process

1. Submissions will be reviewed for:
   - Accuracy of information
   - Appropriate categorization
   - License compliance
   - Link validity
   - Documentation quality

2. Feedback will be provided via PR comments

3. Once approved, your contribution will be merged

## Code of Conduct

- Be respectful and constructive
- Follow ethical data practices
- Respect intellectual property rights
- Ensure compliance with all applicable laws
- Be inclusive and welcoming to all contributors

## Questions?

If you have questions about contributing, please:
- Open an issue for discussion
- Check existing issues for similar questions
- Review the CATALOG.md for examples

Thank you for contributing to the community!
