# Like Bot

Telegram auto-like bot built with `pyTelegramBotAPI`.

## Setup

1. Install Python 3.10+.
2. Install dependencies: `pip install -r requirements.txt`.
3. Set the environment variable `TELEGRAM_BOT_TOKEN` using your hosting provider's Secrets/Environment Variables settings. Do not commit a real token or upload `.env`.
4. Review and configure `OWNER_ID`, `LIKE_API_URL`, `LIKE_API_URL_2`, `BOT_NAME`, support/group URLs, payment text, and timezone in `main.py` before running.
5. Start with `python main.py`.

For local use, copy `.env.example` to `.env` and set the token there; load it using your preferred environment loader or export the variable in your shell. `.env` is ignored by Git.

## Security

The bot token was shared in chat and should be considered compromised. Revoke/regenerate it with Telegram's @BotFather, then save the replacement only in your hosting environment secrets. Never put the token in source code, commits, screenshots, or chat.

## Notes

- The bot uses a JSON database under `database/`; it is excluded from Git to avoid committing runtime data.
- Configure a working like API endpoint before using like-related commands.
