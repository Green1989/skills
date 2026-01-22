---
name: document-word-frequency
description: Analyze and visualize word frequency patterns in documents. Use when users need to extract, count, and analyze word occurrences from .doc, .docx, .pdf, .md, or .txt files. Uses jieba for professional Chinese word segmentation with full mode tokenization (cut_all=True) to maximize word detection coverage. For Chinese text, only counts words with 2+ consecutive characters; single characters are excluded. Pure numbers are filtered out and not counted. English words are counted as complete words. Generates comprehensive markdown reports with tables, charts, and frequency distributions.
---

# Document Word Frequency Analyzer

Analyzes word frequency in document files and generates formatted markdown reports with statistical visualizations.

## Supported Formats

- `.docx` - Microsoft Word documents (XML-based)
- `.pdf` - Portable Document Format
- `.doc` - Legacy Microsoft Word documents (requires textract)
- `.md` - Markdown files (plain text)
- `.txt` - Plain text files (supports multiple encodings: UTF-8, GBK, GB2312)

## Quick Start

### Basic Analysis

```bash
# Analyze a Word document
python scripts/analyze_word_frequency.py path/to/document.docx

# Analyze a PDF file
python scripts/analyze_word_frequency.py path/to/document.pdf

# Analyze a Markdown file
python scripts/analyze_word_frequency.py path/to/document.md

# Analyze a plain text file
python scripts/analyze_word_frequency.py path/to/document.txt
```

This outputs a complete markdown report to stdout with:
- Document statistics (total words, unique words)
- Top 100 most frequent words in a formatted table
- Pie chart showing distribution
- Bar chart visualization

### Save Report to File

```bash
# Save report to a markdown file
python scripts/analyze_word_frequency.py document.docx --output report.md

# Analyze Markdown and save report
python scripts/analyze_word_frequency.py speech.md --output speech_report.md
```

### Custom Analysis

```bash
# Show top 50 words instead of default 100
python scripts/analyze_word_frequency.py file.pdf --top 50

# Specify language for better tokenization
python scripts/analyze_word_frequency.py file.docx --language chinese
python scripts/analyze_word_frequency.py file.pdf --language english
python scripts/analyze_word_frequency.py file.md --language mixed
```

## Language Modes

- **chinese**: Counts Chinese words with 2+ consecutive characters
- **english**: Counts alphanumeric words
- **mixed**: Default - handles both Chinese multi-character words and English words

## Report Format

Generated markdown reports include:

1. **Document Information** - File name, path, total words, unique words
2. **Frequency Table** - Ranked list with counts and percentages
3. **Visualizations** - Mermaid pie chart and ASCII bar chart
4. **Statistics Summary** - Methodology and scope information

## Key Features

- **Full-mode tokenization** - Uses jieba cut_all=True for comprehensive Chinese word coverage, including all possible word combinations
- **Smart tokenization** - Chinese words (2+ characters), English words (complete)
- **Single character exclusion** - Single Chinese characters are not counted
- **Number filtering** - Pure numbers (including dates, IDs) are excluded
- **Multi-language support** - Handles Chinese, English, and mixed content
- **Rich visualizations** - Tables, pie charts, and bar charts
- **Flexible output** - Console or file output

## Dependencies

Install required packages:

```bash
pip install python-docx pypdf jieba
```

For `.doc` support (optional):
```bash
pip install textract
```

**Note**: `jieba` is required for accurate Chinese word segmentation. If not installed, the script will fall back to regex-based tokenization with reduced accuracy.

## Tokenization Method

This tool uses **jieba full-mode tokenization** (`cut_all=True`) for Chinese text processing:

- **What it does**: Scans all possible word combinations in the text, maximizing word detection coverage
- **Why use it**: Captures words that might be merged in precise mode (e.g., "什么" in "什么样" is counted separately)
- **Trade-off**: May generate some redundant tokens, but ensures comprehensive word frequency matching similar to manual search tools

**Example comparison**:
- Precise mode (`cut_all=False`): "什么样的人" → `['什么样', '的', '人']` (3 tokens)
- Full mode (`cut_all=True`): "什么样的人" → `['什么样', '什么', '样', '的', '人']` (5 tokens)

Full mode produces results closer to manual string search tools (like grep), making it more suitable for general word frequency analysis.

## Common Issues

**DOC files not working**: Install textract for legacy `.doc` format support. Modern `.docx` files work out of the box.

**Chinese characters split**: Use `--language mixed` for documents with both Chinese and English content.

**Large file processing**: For very large documents, reduce `--top` number to speed up report generation.

**TXT file encoding errors**: The script automatically tries multiple encodings (UTF-8, GBK, GB2312, UTF-8-sig). If all fail, ensure your text file is saved in a standard encoding.
