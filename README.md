This project provides a Python script to translate Qualtrics survey content into multiple target languages using OpenAI's GPT-4 API. It automates the translation workflow by combining survey questions and answer options for better context, translating via GPT-4, and generating files ready for proofreading and import back into Qualtrics.

# Key Features

- Context-aware translation: Combines related question and answer texts to improve translation quality.
- Proofreading support: Exports translation drafts into Excel and Word documents to facilitate manual review and correction by native speakers.
- Rebuilds Qualtrics format: Converts proofread translations back into CSV files ready for Qualtrics import.
- HTML-aware: Preserves HTML tags in survey text during translation and proofreading export.
- Extensible: Easily customize target languages and translation parameters.

# How it works

- Load the original English Qualtrics survey CSV export.
- Group and concatenate question and response texts to provide GPT-4 with sufficient context.
- Use GPT-4 chat completion API to translate survey text into target languages.
- Save intermediate translations for proofreading in Excel files.
- Generate Word documents from translation Excel files for convenient native-speaker proofreading.
- Convert reviewed translations back into Qualtrics-compatible CSV files.

# Requirements

- Python 3.8+
- pandas
- openai (or openai compatible client)
- python-docx
- htmldocx
- Qualtrics survey CSV export file

# Usage

- Set your OpenAI API keys in the openAI_key.py file.
- Run translation functions for your desired target languages.
- Optionally, generate Word documents for proofreading ease.
- Review and edit the generated Excel translation files.
- Convert the final translations back to Qualtrics format.
