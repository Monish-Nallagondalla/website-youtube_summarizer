# Website & YouTube Summarizer

A Streamlit application that summarizes text content from YouTube videos or websites using LangChain and the Groq API. The app allows users to input a URL (YouTube or website) and a Groq API key, then generates a 300-word summary of the content.

## Features
- **Summarize YouTube Videos**: Extracts transcripts from YouTube videos using `YoutubeLoader` and generates concise summaries.
- **Summarize Websites**: Scrapes text from websites using `UnstructuredURLLoader` and summarizes the content.
- **Groq API Integration**: Leverages the `gemma2-9b-it` model from Groq for fast and accurate text summarization.
- **User-Friendly Interface**: Built with Streamlit for an intuitive web-based experience.
- **Error Handling**: Validates URLs, API keys, and content loading with clear error messages.

## Prerequisites
- Python 3.8+
- A valid Groq API key (obtain from [Groq](https://groq.com/))
- Install required packages:
  ```bash
  pip install streamlit validators langchain langchain-groq langchain-community
  ```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Monish-Nallagondalla/website-youtube_summarizer.git
   cd website-youtube_summarizer
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create a `requirements.txt` file with:
   ```
   streamlit
   validators
   langchain
   langchain-groq
   langchain-community
   ```

## Usage
1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```
2. Open the app in your browser (typically at `http://localhost:8501`).
3. Enter your Groq API key in the sidebar.
4. Input a valid YouTube or website URL.
5. Click "Summarize the Content from YT or Website" to generate a 300-word summary.

## Example URLs
- YouTube: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
- Website: `https://example.com`

## Project Structure
- `app.py`: Main Streamlit application with summarization logic.
- `requirements.txt`: List of required Python packages.

## Error Handling
- Validates Groq API key and URL inputs.
- Handles invalid URLs, inaccessible content, and API errors with user-friendly messages.
- Logs errors for debugging using Python's `logging` module.

## Troubleshooting
- **HTTP Error 400**: Ensure the Groq API key is valid and the model `gemma2-9b-it` is supported. Check the URL for accessibility.
- **Empty Content**: Verify the URL contains extractable text or a valid YouTube transcript.
- **Large Content**: For large websites, consider switching to `map_reduce` chain type in the code.

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/new-feature`).
3. Commit changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a pull request.

## License
This project is licensed under the MIT License.

## Acknowledgments
- Built with [LangChain](https://www.langchain.com/) for text processing.
- Powered by [Groq](https://groq.com/) for fast LLM inference.
- Uses [Streamlit](https://streamlit.io/) for the web interface.

## Contact
For issues or suggestions, open an issue on [GitHub](https://github.com/Monish-Nallagondalla/website-youtube_summarizer/issues) or contact [Monish Nallagondalla](https://github.com/Monish-Nallagondalla).
