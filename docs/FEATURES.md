# Everything 07 does

[See the public showcase](SHOWCASE.md) · [Back to the first page](../README.md)

07 combines a Discord bot, a private owner/developer dashboard, and a separate transcript website for ticket members. The public screenshots use sample data. Features need the bot to be online and to have the required Discord permissions; this page describes the project's capabilities, not a live status report.

## Server setup and multiple servers

- The server owner can preview a role and channel layout before applying it. A separate reset command previews a full rebuild. Backups and recovery offer another way to restore layout after a mistake or incident.
- Only approved servers can use the bot. Each approved server keeps its own tickets, welcome text, guard choices, and community settings. The Control Room has a server picker.
- Shareable setup codes carry reusable settings such as guard rules, welcome text, and ticket category names. They exclude member data, passwords, and server-specific channel or role IDs.
- Discord still limits what the bot can change: its role must be above any role it manages, and a missing permission or deleted channel can interrupt an action.

## Welcome, rules, verification, and roles

- The bot posts rules and a verification panel. A new member can receive the Unverified role; pressing Verify removes it and grants regular community access. It does not grant premium or staff access.
- Welcome cards can show the member, a custom greeting, an optional 07 banner, and the inviter when Discord invite data identifies one.
- Members can choose one color role or remove it, and opt in to ping roles. Smaller panels use buttons; larger sets use a dropdown. Selection feedback is private to the member.
- The Design Studio has 07 panel artwork and an older selectable gallery of 37 banners with matching avatars. That legacy gallery still contains Eclipse lettering, so it is separated and labeled in the showcase.

## Members, voice, and community

- A configurable voice channel displays the current member count in a chosen category. The bot can stay connected to a voice channel while self-muted and self-deafened; it does not record or play audio.
- Invite tracking counts identifiable joins and can publish a read-only tracker. Ambiguous invite changes and offline joins may remain unknown.
- XP comes from normal chat with a cooldown and daily cap. Six purple rank stages, a leaderboard, and image rank cards show progress. Bot messages, commands, and repetitive messages do not earn XP.
- Members can set an away reason. Giveaways support entry buttons, scheduled endings, rerolls, and restart recovery. A random-roll command and server information card are also available.
- Owner tools include a member lookup, custom command words, activity history, alerts, and profile artwork controls.

## Moderation, guard, and logs

- The bot supports bans, kicks, timeouts, mutes, message cleanup, and saved blackouts. A blackout remains in the bot's data and is checked again when the person rejoins.
- Guard uses available Discord audit information to respond to risky role, channel, and server changes. It can record incidents, undo supported changes, and protect Administrator grants. It cannot guarantee restoration of every change made while offline.
- The owner can define trusted operators and choose dedicated channels for moderation, ban, kick, timeout, mute, deleted-message, join/leave, anti-bot, support, and purchase logs.
- Deleted-message logs include the removed text when the bot had access to it. Log messages are routed to private staff channels chosen for that server.

## Support and purchase tickets

- Support and purchases have separate setup modes and log destinations. The owner can change panel heading, bio, description, button text, categories, staff roles, and archive location.
- Members open private tickets using the configured buttons or menu. Staff can answer in Discord or from the private Control Room. The desk supports assignment, priority, tags, searching, closing, and reopening.
- Closing a ticket saves a readable transcript. The operator retains an archive copy; the member receives a private link on a separate transcript website. Support and purchase transcripts can be routed to different staff channels.
- A closed ticket's archived Discord channel can be deleted without deleting the member's transcript link. The dashboard also has a separate action to remove the operator's dashboard copy.

## The two websites

- **Control Room:** private owner/developer sign-in, server picker, ticket desk, bot/voice controls, welcome settings, Design Studio, activity, guard, blackout, health, connections, and updates.
- **Member transcript site:** one private link per saved ticket, a readable conversation, and a text download. The link is unlisted but anyone who has it can read that ticket, so it is sent only to the member and authorized staff destinations.
- Bot-to-dashboard synchronization uses a separate authenticated connection. The dashboard should show a current heartbeat before treating a setting as live.

## Access and limits

`orbit help` is an owner-only guide for the active bot. Member-facing buttons and panels are public where needed; setup responses are private where supported. The actual server permissions, role order, online status, and configured channels determine which feature works at a given moment. This public repository contains no login keys, live IDs, production tickets, or bot source.
