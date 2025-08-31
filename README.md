# Review Scraper

This project scrapes Google reviews and summarises them using Google Generative AI.

## Structure
- `google-reviews/main.py`: Robust, interactive script. Scrapes reviews from a Google page, summarizes them, and allows multiple runs in one session. Uses custom user-agent and error handling.
- `reviews-summary/summarise.py`: Minimal, single-use script. Prompts for a URL, scrapes reviews, and prints a summary. Simpler scraping logic.
- `config.example.py`: Example configuration file. Copy to `config.py` and add your API key.

## Setup
1. **Install dependencies**
   - Use [uv](https://github.com/astral-sh/uv) for dependency management:
     ```sh
     uv pip install
     ```
   - Or add packages individually:
     ```sh
     uv add pyppeteer google-generativeai google-ai-generativelanguage google-api-core google-auth
     ```

2. **Configuration**
   - Copy `google-reviews/config.example.py` to `google-reviews/config.py`.
   - Add your Google API key to `config.py`:
     ```python
     API_KEY = "your-google-api-key"
     ```
   - `config.py` is listed in `.gitignore` and will not be uploaded to git.

## Usage
  ```sh
  python google-reviews/main.py
  ```
  ```sh
  python reviews-summary/summarise.py
  ```

## Recommendation
For most users, `google-reviews/main.py` is recommended due to its robustness and interactive features. Use `summarise.py` for quick, single-run summaries.

## Security
- **Do not upload your real API keys.**
- Only `config.example.py` is included in the repository for demonstration.

## Contributing
Feel free to open issues or submit pull requests!
