# YouTube Video Summarizer

This is a small Python project I built while learning LLM Engineering through Ed Donner's course. I wanted to practice working with APIs, prompts, and responses by creating a tool that summarizes YouTube videos.

## About the project

The program takes a public YouTube video URL, extracts the video ID, and retrieves its available transcript. It combines the transcript into text and sends that text to an OpenAI model, which generates a summary of the video.

## How it works

1. Enter a public YouTube video link.
2. Extract the video ID from the URL.
3. Fetch the transcript using `youtube-transcript-api`.
4. Combine the transcript snippets into one string.
5. Create system and user prompts for the LLM.
6. Call the OpenAI Chat Completions API and display the summary.

## Tools and libraries

- Python
- Jupyter Notebook in VS Code
- `urllib.parse` for handling YouTube URLs
- `youtube-transcript-api` for retrieving transcripts
- `openai` for making the model request
- `python-dotenv` for loading the API key

## What I learned

Through this project, I practiced:

- Taking user input and working with strings
- Parsing URLs and extracting query parameters
- Using Python loops and `join()` to prepare transcript text
- Understanding system and user messages
- Sending a request with `chat.completions.create()`
- Accessing the model's reply with `response.choices[0].message.content`

## Running the project

Install the required packages:

```bash
pip install openai python-dotenv youtube-transcript-api
```

Set `OPENAI_API_KEY` in a local `.env` file, then run the notebook cells in order and enter a public YouTube video URL when prompted. Do not commit your `.env` file or API key to GitHub.

## Notes

This is a learning project, not an official Ed Donner course project. Some videos may not have accessible transcripts, and long transcripts may exceed a model's context limit. API usage may incur charges.
