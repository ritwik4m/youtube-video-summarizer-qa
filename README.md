# YouTube Transcript Summarizer + QnA

A Python + OpenAI-powered tool that extracts YouTube video transcripts, adds punctuation, summarizes content, and answers structured questions using GPT-3.5 or GPT-4.

---

## Features

- Fetches transcripts from any YouTube video (with captions enabled)
- Adds punctuation for readability using multilingual models
- Summarizes long transcripts using OpenAI or Hugging Face models
- Answers key questions (what, why, how) about the video using GPT
- Works in both Google Colab and local environments

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/youtube-video-summarizer-qa.git
cd youtube-video-summarizer-qa
```

---

### 2. Install Dependencies

If running locally:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install openai youtube_transcript_api deepmultilingualpunctuation python-dotenv
```

---

### 3. Set up `.env` (for local use)

Create a `.env` file:

```
OPENAI_API_KEY=your-openai-key-here
```

Or in **Colab**, use:

```python
from getpass import getpass
import os

os.environ["OPENAI_API_KEY"] = getpass("Enter your OpenAI API key: ")
```

---

## How to Use

### Google Colab

1. Open the notebook `youtubeSummarizerNotebook.ipynb` in Colab  
2. Paste your OpenAI key when prompted  
3. Enter a YouTube video ID  
4. Run all cells to get a summary and structured QnA

---

### Run Locally

```bash
python run_prompt.py
```

Make sure your `.env` is present with the API key.

---

## Example Questions Answered

```markdown
Q: What is this video about?
A: The video introduces the basic parts of a personal computer...

Q: What are the key takeaways?
A: Computers consist of hardware and software, each playing specific roles...

Q: Who is this video for?
A: Beginners or non-technical users...
```

---

## Models Used

- `youtube_transcript_api` — for pulling subtitles
- `deepmultilingualpunctuation` — to clean and punctuate text
- `openai.ChatCompletion` — for GPT-3.5/GPT-4 QnA
- (Optional) `pegasus-xsum` — for summarizing long chunks

---

## Roadmap / TODO

- [ ] Add Whisper API for audio-only transcripts
- [ ] Improve language detection & handling
- [ ] Export summary to PDF or markdown
- [ ] Build a basic web UI

---

## Acknowledgments

- [OpenAI](https://openai.com/) — for GPT models
- [Hugging Face](https://huggingface.co/) — for pretrained NLP models
- [YouTube Transcript API](https://pypi.org/project/youtube-transcript-api/) — for subtitle extraction

---

## License

MIT License. Feel free to use, adapt, and share.