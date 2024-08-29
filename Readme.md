# A Question-Driven Approach to Claim Decomposition and Verification Using LLMs

## Abstract

Automated fact-checking has emerged as a safeguard against the spread of false information. Existing fact-checking approaches aim to determine whether a news claim is true or false, and they have achieved decent accuracy of veracity prediction. However, the current state-of-the-art models still face challenges, such as ambiguity in the claims and lack of contextual information. This paper proposes a question-driven approach to enhance the accuracy and reliability of fact-checking processes. Initially, the approach focuses on disambiguating the claim. Subsequently, the claim is decomposed into multiple sub-claims, each of which is evaluated using a combination of large language models (LLMs) and external knowledge sources like search engines and knowledge graphs. The final assessment of the original claim is derived through the reasoning and verification of these sub-claims. Our approach demonstrates improved performance compared to baseline approaches, contributing to the advancement of fact-checking by combining systematic decomposition, advanced reasoning, and human oversight. 

## Datasets

This repository uses data from the [RawFC](https://github.com/Nicozwy/CofCED/tree/main/Datasets/RAWFC) and [LIAR](https://huggingface.co/datasets/liar) datasets. 

## Setup

### API Keys

1. Obtain an OpenAI API key and save it to the variable `OPENAI_API_KEY` in `config.py`.

2. Obtain a [SerpApi](https://serpapi.com/) key and save it to the variable `SERPAPI_KEY` in `config.py`.

### Prerequisites

```sh
python3 -m venv myenv
source myenv/bin/activate

pip install openai serpapi google-search-results sklearn
```

## Usage

```
python 3DFC.py --data_set RAWFC
```

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

## Acknowledgments

Some code are modified from [HiSS](https://github.com/jadeCurl/HiSS), we thank their work.
