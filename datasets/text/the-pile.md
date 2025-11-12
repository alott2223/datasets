# The Pile

## Overview
The Pile is a 825 GiB diverse, open-source language modeling dataset consisting of 22 smaller, high-quality datasets combined together. Created by EleutherAI, it's designed for training large-scale language models.

## Specifications
- **Size**: 825 GB (uncompressed)
- **Format**: JSON Lines (JSONL)
- **License**: Various (see component datasets)
- **Language**: Primarily English
- **Domain**: Multi-domain (web, books, code, scientific papers, etc.)

## Source
- Official website: [https://pile.eleuther.ai/](https://pile.eleuther.ai/)
- Download: [https://the-eye.eu/public/AI/pile/](https://the-eye.eu/public/AI/pile/)
- Paper: [https://arxiv.org/abs/2101.00027](https://arxiv.org/abs/2101.00027)
- GitHub: [https://github.com/EleutherAI/the-pile](https://github.com/EleutherAI/the-pile)

## Statistics
- **Total Documents**: ~210M documents
- **Total Tokens**: ~300B tokens

### Component Datasets:
1. Pile-CC (web content)
2. PubMed Central (biomedical literature)
3. Books3 (books)
4. OpenWebText2 (web content)
5. ArXiv (scientific papers)
6. GitHub (code)
7. FreeLaw (legal documents)
8. Stack Exchange (Q&A)
9. USPTO Backgrounds (patents)
10. PubMed Abstracts (medical abstracts)
11. Gutenberg (books)
12. OpenSubtitles (movie subtitles)
13. Wikipedia (encyclopedia)
14. DM Mathematics (math Q&A)
15. Ubuntu IRC (chat logs)
16. BookCorpus2 (books)
17. EuroParl (parliamentary proceedings)
18. HackerNews (tech forum)
19. NIH ExPorter (research abstracts)
20. Enron Emails
21. PhilPapers (philosophy papers)
22. YoutubeSubtitles

## Usage

### Using HuggingFace Datasets
```python
from datasets import load_dataset

# Load the full dataset
dataset = load_dataset("EleutherAI/pile", split="train")

# Or load specific components
dataset = load_dataset("EleutherAI/pile", split="train", name="pubmed_central")
```

### Direct Download
The dataset is available as tar files that can be downloaded and extracted. Each tar file contains JSONL files.

### Data Format
Each line in the JSONL files contains:
```json
{
  "text": "The actual text content...",
  "meta": {"pile_set_name": "PubMed Central"}
}
```

## Citation
```bibtex
@article{gao2020pile,
  title={The Pile: An 800GB Dataset of Diverse Text for Language Modeling},
  author={Gao, Leo and Biderman, Stella and Black, Sid and Golding, Laurence and Hoppe, Travis and Foster, Charles and Phang, Jason and He, Horace and Thite, Anish and Nabeshima, Noa and others},
  journal={arXiv preprint arXiv:2101.00027},
  year={2020}
}
```

## Notes
- The dataset includes diverse content types which helps models generalize better
- Some components have restrictive licenses, so verify licensing for your use case
- The dataset has been influential in training many open-source LLMs
- Consider using streaming mode if you don't have sufficient disk space
- Some components may contain offensive or biased content
