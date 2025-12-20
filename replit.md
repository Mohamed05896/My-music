# AnonXMusic - Telegram Music Bot

## Overview
A Telegram music bot that allows playing music/videos in Telegram voice chats. Built with Python using Pyrogram (kurigram) and py-tgcalls.

## Project Structure
- `anony/` - Main application package
  - `core/` - Core functionality (bot, userbot, MongoDB, YouTube, calls)
  - `helpers/` - Utility functions and classes
  - `plugins/` - Bot command handlers and plugins
  - `locales/` - Multi-language support JSON files
  - `cookies/` - YouTube cookies storage
- `config.py` - Configuration loader from environment variables

## Required Environment Variables
The following secrets must be configured for the bot to run:

| Variable | Description |
|----------|-------------|
| `API_ID` | Telegram API ID from my.telegram.org/apps |
| `API_HASH` | Telegram API Hash from my.telegram.org/apps |
| `BOT_TOKEN` | Bot token from @BotFather on Telegram |
| `MONGO_URL` | MongoDB connection URL from cloud.mongodb.com |
| `LOGGER_ID` | Telegram chat/channel ID for logging |
| `OWNER_ID` | Your Telegram user ID |
| `SESSION` | Pyrogram session string from @StringFatherBot |

### Optional Variables
- `SESSION2`, `SESSION3` - Additional session strings for multiple assistants
- `DURATION_LIMIT` - Max song duration in minutes (default: 60)
- `QUEUE_LIMIT` - Max queue size (default: 20)
- `PLAYLIST_LIMIT` - Max playlist size (default: 20)
- `SUPPORT_CHANNEL`, `SUPPORT_CHAT` - Support links
- `AUTO_END`, `AUTO_LEAVE` - Auto behavior settings
- `VIDEO_PLAY` - Enable/disable video playback
- `COOKIES_URL` - YouTube cookies URL (batbin.me links)
- `DEFAULT_THUMB`, `PING_IMG`, `START_IMG` - Image URLs

## Running the Bot
```bash
python -m anony
```

## Dependencies
- Python 3.11
- kurigram (Pyrogram fork)
- py-tgcalls (voice calls)
- pymongo (MongoDB)
- yt-dlp (YouTube downloads)
- ffmpeg (audio/video processing)
