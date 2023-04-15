#Extension connecting text-generator to telegram bot api.
-

REQUIREMENTS:
- python-telegram-bot==13.15
- pyyaml

This is extension for [oobabooga/text-generation-webui](https://github.com/oobabooga/text-generation-webui) providing cai-chat like telegram bot interface.
[Image1](https://github.com/innightwolfsleep/storage/raw/main/textgen_telegram.PNG)

HOW TO INSTALL:
1) clone this repo to "text-generation-webui\extensions"
2) install telegram module to your textgen envivroment. (Easiest way is run webui.bat with additional string "call pip install -r extensions\telegram_bot\requirements.txt" before "call python server.py"

HOW TO USE:
1) place to your bot token to text-generation-webui\extensions\telegram_bot\telegram_token.txt
1) add your bot token to "text-generation-webui\extensions\telegram_bot\telegram_token.txt" (ask https://t.me/BotFather how to get token)
2) run server.py with "--extensions telegram_bot"

FEATURES:
- chat and notebook modes
- session for all users are separative (by chat_id)
- local session history - conversation won't be lost if server restarts. Separated history between users and chars.
- nice "X typing" during generating (users will not think that bot is stuck)
- regenerate last message, remove last messages from history, reset history button, continue previous message
- you can load new characters from text-generation-webui\characters with "/loadX" command!!!
- chatting # prefix for impersonate: "#You" or "#Castle guard" or "#Alice thoughts about me"


TBC:
- replace "X typing" by yield from generator
- group chat mode (need to be tested, does current workflow is ok?)
