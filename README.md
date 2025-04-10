# AI Conversation With Voice

A Node.js application that simulates an argumentative conversation between two AI characters (Maverick and Blaze) with voice output using Google Cloud Text-to-Speech.

## Features

- Generates a back-and-forth argument between two AI personalities
- Converts AI responses to speech using Google Cloud TTS
- Plays audio responses in real-time
- Saves all audio files for later reference

## Requirements

- Node.js (v14 or newer)
- OpenRouter API key
- Google Cloud Text-to-Speech API credentials
- Audio playback capability on your system (Windows, macOS, or Linux with mpg123)

## Installation

1. Clone this repository
2. Install dependencies:

```bash
npm install
```

3. Copy the example environment file and fill in your API keys:

```bash
cp .env.example .env
```

## Environment Setup

Edit the `.env` file and add your API credentials:

```
OPENROUTER_API_KEY=your_openrouter_api_key_here
GOOGLE_CLIENT_EMAIL=your_google_cloud_service_account_email
GOOGLE_PRIVATE_KEY="your_google_cloud_private_key"
```

Optional settings:

- `SKIP_AUDIO_PLAYBACK=true` - Set this to skip audio playback and only save files

## Usage

Run the application:

```bash
npm start
```

The program will:

1. Prompt you for an initial topic for the AI conversation
2. Ask how many exchanges you want the AIs to have
3. Generate responses from each AI character
4. Convert those responses to speech and play them
5. Save all audio files to the `audio` directory

## Audio Playback Requirements

- **Windows**: Uses the default media player
- **macOS**: Uses the built-in `afplay` command
- **Linux**: Requires `mpg123` to be installed (`sudo apt-get install mpg123`)
