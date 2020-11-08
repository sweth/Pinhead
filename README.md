**Pinhead** is a simple Discord bot that pins messages to a specific channel. This is a
workaround for Discord's per-channel 50 pin limit.

(SVC fork to ease setting up by someone else for potted plant)

# Installation

1. `git clone https://github.com/sweth/Pinhead.git pinhead && cd pinhead`
1. `npm install` - Installs dependencies
1. `node index.js` - Runs the bot

See https://github.com/RoyCurtis/Pinhead for more general install notes

# Usage

1. User posts something that needs feedback, and reacts to it with :feedbackpin: emoji
1. Bot goes ahead and copies the message to #feedback-queue
1. AutoDelete bot at https://top.gg/bot/314230903872421889 will delete copy in #feedback-queue after 7 days

# Limitations

* The bot will not unpin messages; that is up to anybody with message management perms
* [Due to issues with Discord.js][1], only the previous 100 messages + any the bot has
seen since running, are pinnable

[1]: https://github.com/hydrabolt/discord.js/issues/1675
