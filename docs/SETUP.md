# How 07 fits together

[Public showcase](SHOWCASE.md) · [Full feature guide](FEATURES.md) · [Back to the first page](../README.md)

07 has three parts:

1. **Discord bot:** reads events it has permission to see, runs setup and community commands, posts panels, updates roles and channels, and handles tickets.
2. **Private Control Room:** lets the owner and approved developers manage each approved server and review ticket/guard activity. The bot and the website communicate through a separate authenticated connection.
3. **Member transcript website:** stores readable closed-ticket copies away from the private operator dashboard. Each ticket has an unlisted link meant for its member and authorized staff.

```text
Discord server ⇄ 07 bot ⇄ private Control Room
                      └─────→ separate transcript website
```

The public screenshots show the real interface filled with invented demonstration data. They do not show a production server, member, ticket, or login. The source, deployment settings, and actual credentials remain private. This public repository is a portfolio and feature guide; it cannot be used to operate the bot or sign in to the Control Room.

Discord role order, channel permissions, enabled intents, and a running host determine whether each feature can act in a server. A current bot heartbeat is the reliable sign that the live dashboard is connected.
