# Dataset Catalog

This catalog provides an overview of datasets collected for AI and LLM training purposes.

## Text Datasets

### Language Models & NLP

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| Common Crawl | Web crawl data | ~250 TB | WARC | [commoncrawl.org](https://commoncrawl.org/) | Open |
| The Pile | Diverse text dataset for LLM training | 825 GB | JSON | [pile.eleuther.ai](https://pile.eleuther.ai/) | Various |
| C4 (Colossal Clean Crawled Corpus) | Cleaned Common Crawl | ~750 GB | Text | [tensorflow.org](https://www.tensorflow.org/datasets/catalog/c4) | ODC-BY |
| Wikipedia | Encyclopedia articles | ~20 GB | XML/SQL | [dumps.wikimedia.org](https://dumps.wikimedia.org/) | CC-BY-SA |
| BookCorpus | Books from unpublished authors | ~5 GB | Text | Various | Research Use |
| OpenWebText | Web content | ~38 GB | Text | [openwebtext2](https://openwebtext2.readthedocs.io/) | Open |
| RedPajama | Open reproduction of LLaMA training data | 1.2 TB | Text | [together.ai](https://www.together.ai/blog/redpajama) | Various |
| ROOTS | Multilingual dataset | 1.6 TB | Text | [BigScience](https://huggingface.co/bigscience) | Various |

### Question Answering

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| SQuAD 2.0 | Stanford Question Answering Dataset | ~45 MB | JSON | [rajpurkar.github.io](https://rajpurkar.github.io/SQuAD-explorer/) | CC-BY-SA |
| Natural Questions | Google's question answering dataset | ~42 GB | JSON | [ai.google.com](https://ai.google.com/research/NaturalQuestions) | CC-BY-SA |
| TriviaQA | Trivia question-answer pairs | ~2.5 GB | JSON | [nlp.cs.washington.edu](http://nlp.cs.washington.edu/triviaqa/) | Apache 2.0 |
| MS MARCO | Microsoft Machine Reading Comprehension | ~11 GB | TSV | [microsoft.github.io](https://microsoft.github.io/msmarco/) | MS Data License |

### Instruction & Chat

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| Alpaca | Instruction-following demonstrations | ~5 MB | JSON | [Stanford](https://github.com/tatsu-lab/stanford_alpaca) | CC-BY-NC |
| Dolly | Instruction dataset by Databricks | ~15 MB | JSON | [Databricks](https://github.com/databrickslabs/dolly) | CC-BY-SA |
| ShareGPT | User-shared ChatGPT conversations | Varies | JSON | Various sources | Varies |
| OpenAssistant Conversations | Crowdsourced assistant conversations | ~600 MB | Parquet | [LAION](https://huggingface.co/datasets/OpenAssistant/oasst1) | Apache 2.0 |

### Code Datasets

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| The Stack | Source code in 358+ languages | 6.4 TB | Parquet | [BigCode](https://huggingface.co/datasets/bigcode/the-stack) | Various |
| CodeParrot | Python code from GitHub | ~50 GB | Text | [CodeParrot](https://huggingface.co/datasets/codeparrot/github-code) | Various |
| CodeSearchNet | Code search dataset | ~5 GB | JSON | [GitHub](https://github.com/github/CodeSearchNet) | Various |

## Image Datasets

### General Vision

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| ImageNet | Image classification benchmark | ~150 GB | JPEG | [image-net.org](http://www.image-net.org/) | Research Use |
| COCO | Common Objects in Context | ~25 GB | JPEG/JSON | [cocodataset.org](https://cocodataset.org/) | CC-BY |
| Open Images | Large-scale image dataset | ~500 GB | JPEG | [Google](https://storage.googleapis.com/openimages/web/index.html) | CC-BY |
| LAION-5B | 5 billion image-text pairs | ~240 TB | Various | [LAION](https://laion.ai/blog/laion-5b/) | Various |
| LAION-400M | 400M image-text pairs | ~20 TB | Various | [LAION](https://laion.ai/blog/laion-400-open-dataset/) | Various |

### Specialized

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| CelebA | Celebrity faces | ~1.4 GB | JPEG | [mmlab.ie.cuhk.edu.hk](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) | Research Use |
| Places365 | Scene recognition | ~105 GB | JPEG | [places2.csail.mit.edu](http://places2.csail.mit.edu/) | Research Use |

## Audio Datasets

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| LibriSpeech | Speech recognition | ~60 GB | FLAC | [openslr.org](https://www.openslr.org/12) | CC-BY |
| Common Voice | Multilingual speech | ~100 GB | MP3 | [Mozilla](https://commonvoice.mozilla.org/) | CC-0 |
| VoxCeleb | Speaker recognition | ~150 GB | WAV | [robots.ox.ac.uk](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) | Research Use |
| AudioSet | Audio event classification | N/A (YouTube links) | YouTube | [Google](https://research.google.com/audioset/) | CC-BY |

## Video Datasets

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| Kinetics | Action recognition | ~450 GB | MP4 | [deepmind.com](https://www.deepmind.com/open-source/kinetics) | Research Use |
| YouTube-8M | Video classification | ~1.5 TB | TFRecord | [research.google.com](https://research.google.com/youtube8m/) | CC-BY |
| ActivityNet | Human activity understanding | ~500 GB | MP4 | [activity-net.org](http://activity-net.org/) | Research Use |

## Multimodal Datasets

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| Conceptual Captions | Image-caption pairs | ~10 GB | TSV | [Google](https://ai.google.com/research/ConceptualCaptions/) | CC-BY |
| CLIP Dataset | Used to train CLIP | ~400M pairs | Various | [OpenAI](https://github.com/openai/CLIP) | Various |
| WebVid | Video-text pairs | ~10M videos | Various | [m-bain.github.io](https://m-bain.github.io/webvid-dataset/) | Research Use |

## Structured Data

| Dataset Name | Description | Size | Format | Source | License |
|-------------|-------------|------|--------|--------|---------|
| WikiData | Structured knowledge base | ~100 GB | JSON | [wikidata.org](https://www.wikidata.org/) | CC-0 |
| DBpedia | Structured Wikipedia data | ~50 GB | RDF | [dbpedia.org](https://www.dbpedia.org/) | CC-BY-SA |
| GLUE | Language understanding benchmark | ~1 GB | Various | [gluebenchmark.com](https://gluebenchmark.com/) | Various |
| SuperGLUE | Advanced language understanding | ~500 MB | Various | [super.gluebenchmark.com](https://super.gluebenchmark.com/) | Various |

## Notes

- Sizes are approximate and may vary based on version and format
- Always verify license terms before using datasets
- Many datasets require registration or agreement to terms of service
- Some datasets are available through HuggingFace Datasets, TensorFlow Datasets, or PyTorch datasets libraries
- Cloud providers (AWS, Google Cloud, Azure) often host popular datasets with free egress

## How to Add a Dataset

To add a new dataset to this catalog:

1. Determine the appropriate category (text, image, audio, video, multimodal, structured)
2. Add an entry to the relevant table with:
   - Dataset Name
   - Brief Description
   - Approximate Size
   - Format (file types)
   - Source (link to official page)
   - License information
3. Ensure the information is accurate and up-to-date
4. Submit a pull request with your addition
