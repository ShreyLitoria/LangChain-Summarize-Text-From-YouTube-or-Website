# LangChain-Summarize-Text-From-YouTube-or-Website


This Streamlit app uses LangChain to summarize text content from YouTube videos or websites. By simply providing a URL (either a YouTube video link or a website URL), the app will fetch the content and summarize it using a HuggingFace model via the Groq API.

## Features

- Summarize text from a YouTube video or any valid website URL.
- Uses the **HuggingFace** model for text summarization.
- User-friendly interface with **Streamlit** for easy interaction.
- Supports text summarization in up to **300 words**.

## Requirements

To run this app, you need the following Python packages:

- `streamlit`
- `validators`
- `langchain`
- `langchain_groq`
- `langchain_huggingface`
- `langchain_community`

You can install these packages via `pip`:

```bash
pip install streamlit validators langchain langchain_groq langchain_huggingface langchain_community
```

## How to Use
- Clone the repository to your local machine.
- Run the app with the following command:
```bash
streamlit run app.py
```
- Enter a valid YouTube or website URL in the provided text input.
- Enter your HuggingFace API token (you can get it from HuggingFace's website).
- Click the "Summarize the Content from YT or Website" button to get the summary.

## Components of the App
1. HuggingFace API Token: Required to access the HuggingFace model for text summarization.
2. Generic URL: You can input either a YouTube video URL or any website URL for summarization.

## How It Works
- The app takes the HuggingFace API key and a URL as input from the user.
- If the URL is from YouTube, it uses the YoutubeLoader to fetch the video data.
- If it's a website URL, it uses the UnstructuredURLLoader to extract text from the website.
- The content is then passed through the summarization chain, using a model like Mistral-7B-Instruct.
- Finally, the summary is displayed in the app.

## Error Handling
1. If any of the required fields (API token or URL) are missing or invalid, the app will show an error message.
2. If there is an issue with fetching the URL content, the app will display an exception error.


## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](./LICENSE) file for more details.

## Credits
- LangChain: For creating a flexible framework for language model-based applications.
- HuggingFace: For providing pre-trained models for natural language processing tasks.
- Streamlit: For enabling easy and interactive web apps in Python.
