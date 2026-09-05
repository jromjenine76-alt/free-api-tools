# Free API Tools - PDF to Video & Text-to-Speech

A comprehensive collection of **free API tools** for converting PDFs to videos and text-to-speech applications.

---

## 📹 PDF to Video Tools

### PDF Extraction (First Step)

| Tool | Description | Free Tier | Link |
|------|-------------|-----------|------|
| **PDF.co API** | Extracts text and images from PDFs | Limited free usage | [Documentation](https://apidocs.pdf.co/) |
| **PDF.js** | Open-source JS library for PDF extraction | Unlimited (self-hosted) | [GitHub](https://github.com/mozilla/pdf.js) |

### Video Creation APIs

| Tool | Description | Free Tier | Link |
|------|-------------|-----------|------|
| **Shotstack** | Create videos combining images, text, and audio | Free tier available | [Shotstack API](https://shotstack.io/) |
| **Pictory API** | Convert text to video with free trials | Free trial credits | [Pictory API](https://pictory.ai/api/) |
| **Invideo API** | Text-to-video automation | Free credits included | [Invideo API](https://invideo.io/api/) |

---

## 🎙️ Text-to-Speech (TTS) APIs

| Tool | Description | Free Tier | Pricing Details | Link |
|------|-------------|-----------|-----------------|------|
| **Google Text-to-Speech (gTTS)** | Python library, no signup required | Unlimited (rate limited) | Unofficial, works as-is | [GitHub](https://github.com/pndurette/gTTS) |
| **Google Cloud TTS API** | High-quality voices, multiple languages | 4 million chars/month | Requires Google Cloud account | [Google Cloud TTS](https://cloud.google.com/text-to-speech) |
| **IBM Watson TTS** | Professional quality voices | 10,000 chars/month | IBM Cloud account required | [IBM Watson TTS](https://cloud.ibm.com/apidocs/text-to-speech) |
| **TTSMP3 API** | Simple REST API | 3,000 chars/day | No signup required | [TTSMP3 API](https://ttsmp3.com/api/) |
| **ResponsiveVoice API** | Browser-based TTS | Free plan available | Includes watermark in free tier | [ResponsiveVoice API](https://responsivevoice.org/api/) |

---

## 🌐 Free Advanced APIs (Comprehensive Collection)

### 🤖 Artificial Intelligence & NLP

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **OpenAI (ChatGPT, DALL-E, Whisper)** | AI-powered text, image, and speech models | Limited usage | [OpenAI API](https://openai.com/api/) |
| **Hugging Face Inference API** | Access to pretrained NLP models | Free tier available | [Hugging Face](https://huggingface.co/inference-api) |
| **DeepAI** | Text and image processing endpoints | Free tier with limits | [DeepAI](https://deepai.org/api) |

### 📊 Data & Search

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **OpenWeatherMap** | Real-time weather data | Generous free tier | [OpenWeatherMap API](https://openweathermap.org/api) |
| **NewsAPI** | News headlines and article search | Free plan available | [NewsAPI](https://newsapi.org/) |
| **Google Books API** | Access to millions of book records | Unlimited | [Google Books API](https://developers.google.com/books) |

### 🛠️ Productivity & Collaboration

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **Notion API** | Integration and automation with Notion | Free to use | [Notion API](https://developers.notion.com/) |
| **Trello API** | Access to boards, cards, and lists | Free tier | [Trello API](https://developer.atlassian.com/cloud/trello/rest/api-group-actions/) |
| **Airtable API** | Database automation and integration | Free with storage limits | [Airtable API](https://airtable.com/api) |

### 💰 Finance & Cryptocurrency

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **CoinGecko API** | Real-time cryptocurrency data | Completely free | [CoinGecko API](https://www.coingecko.com/en/api) |
| **Alpha Vantage** | Stock market and forex data | Free tier available | [Alpha Vantage](https://www.alphavantage.co/) |

### 🖼️ Image & Media

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **Pexels API** | Millions of free stock photos | Unlimited | [Pexels API](https://www.pexels.com/api/) |
| **Unsplash API** | High-quality free images | Unlimited | [Unsplash API](https://unsplash.com/developers) |
| **Remove.bg** | Background removal for images | Free monthly allowance | [Remove.bg API](https://www.remove.bg/api) |

### 🗺️ Maps & Geolocation

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **Mapbox** | Map tiles and geolocation services | Free tier with quota | [Mapbox API](https://www.mapbox.com/developers) |
| **Positionstack** | Forward and reverse geocoding | 25,000 requests/month | [Positionstack](https://positionstack.com/) |
| **IPinfo.io** | IP geolocation information | Free tier | [IPinfo.io](https://ipinfo.io/) |

### 🎭 Miscellaneous

| API | Description | Free Tier | Link |
|-----|-------------|-----------|------|
| **JokeAPI** | Random jokes and humor content | Unlimited free | [JokeAPI](https://jokeapi.dev/) |

---

## 🔄 Recommended Workflow

1. **Extract PDF Content**
   - Use **PDF.js** (open-source, unlimited) or **PDF.co API** (limited free tier)
   - Extract text and images from your PDF

2. **Generate Voiceover (Optional)**
   - Use **Google Cloud TTS** (4M chars/month free) or **TTSMP3 API** (3K chars/day, no signup)
   - Convert extracted text to audio

3. **Create Video**
   - Use **Shotstack** (free tier with good limits)
   - Combine extracted images, text, and audio into a video

---

## 💡 Quick Start Examples

### Using PDF.js (Extract PDF)
```javascript
import * as pdfjsLib from 'pdfjs-dist';

const pdf = await pdfjsLib.getDocument('document.pdf').promise;
const page = await pdf.getPage(1);
const text = await page.getTextContent();
```

### Using gTTS (Text-to-Speech)
```python
from gtts import gTTS

tts = gTTS(text="Hello World", lang='en')
tts.save("output.mp3")
```

### Using Google Cloud TTS
```python
from google.cloud import texttospeech

client = texttospeech.TextToSpeechClient()
synthesis_input = texttospeech.SynthesisInput(text="Hello World")
voice = texttospeech.VoiceSelectionParams(language_code="en-US")
audio_config = texttospeech.AudioConfig(audio_encoding=texttospeech.AudioEncoding.MP3)

response = client.synthesize_speech(
    input=synthesis_input, voice=voice, audio_config=audio_config
)
```

### Using Shotstack (Create Video)
```bash
curl -X POST https://api.shotstack.io/v1/render \
  -H "Content-Type: application/json" \
  -H "x-api-key: YOUR_API_KEY" \
  -d '{
    "timeline": {
      "tracks": [{
        "clips": [{
          "asset": {
            "type": "image",
            "src": "https://example.com/image.jpg"
          },
          "start": 0,
          "length": 5
        }]
      }]
    },
    "output": {
      "format": "mp4",
      "resolution": "1080p"
    }
  }'
```

---

## 📊 Comparison Table

| Feature | PDF.js | PDF.co | Google TTS | IBM Watson | TTSMP3 | Shotstack |
|---------|--------|--------|-----------|-----------|--------|-----------|
| **Free Tier** | ✅ Unlimited | ⚠️ Limited | ✅ 4M chars/mo | ⚠️ 10K chars/mo | ✅ 3K chars/day | ✅ Free tier |
| **No Signup** | ✅ Yes | ❌ No | ❌ No | ❌ No | ✅ Yes | ❌ No |
| **Quality** | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **Language Support** | N/A | Limited | ✅ 30+ | ✅ 30+ | ✅ Multiple | N/A |
| **API Documentation** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ |

---

## 🚀 Getting Started

Choose your stack based on your needs:

- **Fastest Setup**: PDF.js + TTSMP3 + Shotstack (minimal signup)
- **Best Quality**: PDF.co + Google Cloud TTS + Shotstack (requires accounts)
- **Most Affordable**: PDF.js + gTTS + Shotstack (lowest cost)

---

## ✅ Tips for Using Free APIs

- Check **rate limits** and fair usage policies for each API
- Most require **API key registration**
- Usage beyond the free tier is typically paid
- Always review the **terms of service** for each API

---

## 📝 License

This repository is a collection of references to third-party services. Please refer to each service's terms of use.

---

## 🤝 Contributing

Feel free to add more free API tools! Submit a PR with:
- Tool name and description
- Free tier limits
- Link to documentation
- Example code snippet

---

**Last Updated**: September 2026
