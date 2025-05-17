# QuickAgent - Voice Conversation Bot

QuickAgent is an interactive voice conversation bot that uses Speech-to-Text, Text-to-Speech, and a language model to have natural conversations with users. The application streams audio in both directions for a responsive experience.

## Features

- Real-time speech recognition using Deepgram
- Natural language processing with OpenAI or Groq models
- High-quality text-to-speech with customizable voice options
- Streaming capabilities for fast response times

## Prerequisites

- Python 3.8 or higher
- ffplay (part of FFmpeg) for audio playback
- API keys for Deepgram and either OpenAI or Groq

## Setup Instructions

### 1. Install Dependencies

```bash
# Install required Python packages
pip install -r requirements.txt

# If you don't have ffplay installed (macOS)
brew install ffmpeg
```

### 2. Configure API Keys

Create a `.env` file in the project root with your API keys:

```
DEEPGRAM_API_KEY=your_deepgram_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
# GROQ_API_KEY=your_groq_api_key_here  # Uncomment if using Groq instead of OpenAI
```

- Get a Deepgram API key at [deepgram.com](https://deepgram.com/)
- Get an OpenAI API key at [openai.com](https://platform.openai.com/)
- Get a Groq API key at [groq.com](https://groq.com/) (optional)

### 3. Voice Model Configuration

The application is configured to use the "aura-zeus-en" voice model from Deepgram. You can change this in the `QuickAgent.py` file by modifying the `MODEL_NAME` variable in the `TextToSpeech` class.

Available voice options:
- `aura-helios-en` - Default male voice
- `aura-athena-en` - Female voice
- `aura-zeus-en` - Deeper male voice (currently selected)
- `aura-hera-en` - Another female voice option

## Running the Application

Start the application with:

```bash
python QuickAgent.py
```

The bot will listen for your voice input. Speak naturally, and the bot will respond with synthesized speech. Say "goodbye" to exit the application.

## Project Structure

- `QuickAgent.py` - Main application file
- `system_prompt.txt` - Contains the system prompt for the language model
- `requirements.txt` - Python dependencies
- `building_blocks/` - Directory containing isolated components for reference and learning

## Troubleshooting

- If you encounter audio issues, ensure ffplay is installed and working correctly
- Check that your microphone is properly configured and has necessary permissions
- Verify your API keys are correct in the `.env` file

## License

This project is provided as an educational demo.
