# Data Analyst Telegram Bot

A Telegram bot that answers data-analysis questions using an LLM via AI Pipe and returns responses as JSON.

## Features

* Receives questions through Telegram
* Uses AI Pipe (`https://aipipe.org/openai/v1`) for reasoning
* Returns exactly one JSON object as the response
* Logs every interaction to `run.jsonl`
* Includes a public `log_url` in every response

## Project Structure

```text
.
├── bot.py
├── requirements.txt
├── run.jsonl
└── README.md
```

## Installation

1. Clone the repository.

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Set the required environment variables:

* `TELEGRAM_BOT_TOKEN`
* `AIPIPE_TOKEN`

Example:

```bash
export TELEGRAM_BOT_TOKEN="your_telegram_bot_token"
export AIPIPE_TOKEN="your_aipipe_token"
```

On Windows (Command Prompt):

```cmd
set TELEGRAM_BOT_TOKEN=your_telegram_bot_token
set AIPIPE_TOKEN=your_aipipe_token
```

## Run the Bot

```bash
python bot.py
```

## Deployment

The bot is intended to run continuously on a hosting platform such as Render or Railway.

## Logging

Every incoming message and outgoing response is appended to `run.jsonl`. The public raw GitHub URL of this file is used as the `log_url` in responses.

## Repository

This repository is for the IIT Madras TDS Project 1 Data Analyst Telegram Bot assignment.
