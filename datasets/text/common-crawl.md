# Common Crawl

## Overview
Common Crawl is a non-profit organization that crawls the web and freely provides its archives and datasets to the public. It contains petabytes of web crawl data collected since 2008.

## Specifications
- **Size**: ~250-300 TB per monthly crawl
- **Format**: WARC (Web ARChive format), WET (extracted text), WAT (metadata)
- **License**: Data is available to everyone, with various licenses for the content itself
- **Language**: Multilingual (100+ languages)
- **Domain**: World Wide Web

## Source
- Official website: [https://commoncrawl.org/](https://commoncrawl.org/)
- Download: [https://commoncrawl.org/the-data/get-started/](https://commoncrawl.org/the-data/get-started/)
- Documentation: [https://commoncrawl.org/documentation](https://commoncrawl.org/documentation)
- AWS Public Dataset: [https://registry.opendata.aws/commoncrawl/](https://registry.opendata.aws/commoncrawl/)

## Statistics
- **Crawl Frequency**: Monthly
- **Pages per Crawl**: ~3-4 billion web pages
- **Total Archive**: 250+ petabytes (cumulative since 2008)

### Recent Crawl Stats (example):
- Web pages: ~3.5 billion
- Hosts: ~50 million
- TLDs: 1,000+

## Usage

### Using Python with warcio
```python
from warcio.archiveiterator import ArchiveIterator
import requests

# Download a WARC file segment
warc_url = "https://data.commoncrawl.org/crawl-data/CC-MAIN-2024-10/segments/[segment].warc.gz"
response = requests.get(warc_url, stream=True)

# Iterate through records
for record in ArchiveIterator(response.raw):
    if record.rec_type == 'response':
        url = record.rec_headers.get_header('WARC-Target-URI')
        content = record.content_stream().read()
        print(f"URL: {url}")
```

### Using AWS S3 (no egress fees)
```bash
# List available crawls
aws s3 ls --no-sign-request s3://commoncrawl/crawl-data/

# Download a specific WARC file
aws s3 cp --no-sign-request \
  s3://commoncrawl/crawl-data/CC-MAIN-2024-10/segments/.../file.warc.gz \
  ./
```

### Using Common Crawl Index
```python
import requests

# Search the index
url = "https://index.commoncrawl.org/CC-MAIN-2024-10-index"
params = {
    "url": "example.com",
    "output": "json"
}
response = requests.get(url, params=params)
results = response.json()
```

## Data Format

### WARC Format
Contains full HTTP response including headers and content

### WET Format
Extracted plain text from web pages (easier to process)

### WAT Format
Metadata and extracted information (links, language, etc.)

## Citation
```bibtex
@misc{commoncrawl,
  title={Common Crawl},
  author={{Common Crawl}},
  howpublished={\url{https://commoncrawl.org/}},
  year={2024}
}
```

## Notes
- Common Crawl is one of the largest publicly available web datasets
- Widely used for training large language models (GPT-3, LLaMA, etc.)
- Available on AWS with no egress fees when accessed from AWS services
- Data quality varies significantly; filtering and cleaning are usually necessary
- Contains copyrighted content, so be mindful of usage restrictions
- PII (Personally Identifiable Information) may be present
- Consider using pre-processed/filtered versions like C4 or RefinedWeb for easier usage
- Processing full crawls requires significant computational resources
