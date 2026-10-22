# Sakura — visuals and features

Sakura grew from the 07 bot. This page keeps earlier 07 artwork and previews alongside the new [Sakura profile](../README.md). The dashboard screenshots use invented sample data, not real members or tickets. The runnable bot and private sites are not published here.

[Add Sakura to your server](https://discord.com/oauth2/authorize?client_id=1555856888367947796). Review the permissions Discord shows before you approve the invite.

[Public home](../README.md) · [Full feature guide](FEATURES.md) · [Project notes](SETUP.md) · [Change history](CHANGELOG.md)

## Earlier 07 artwork

![Purple 07 Colors self-role banner](../assets/art/07-colors-panel.png)

The color-role panel uses purple 07 artwork. A member can pick one color at a time; selecting the current color again removes it. The bot switches between buttons and a dropdown based on the number of choices, and the member's confirmation is private.

![Black 07 Pings self-role banner](../assets/art/07-pings-panel.png)

The ping panel uses the black 07 version. Members opt in to announcement, release, poll, or other configured ping roles. These are notification roles, never staff or premium access.

| Welcome | Verification |
| --- | --- |
| ![07 welcome panel art](../assets/art/07-welcome-panel.png) | ![07 verification panel art](../assets/art/07-verify-panel.png) |

| Main banner | Avatar |
| --- | --- |
| ![07 main banner](../assets/art/07-banner.png) | ![07 avatar](../assets/art/07-avatar.png) |

The [Design Studio gallery](#full-artwork-catalog) also contains 37 selectable banner designs and 37 matching avatars. These designs still say Eclipse or 07, so they are kept as earlier artwork, not Sakura's current profile. See [the new Sakura avatar and banner](../README.md#the-look).

## Control Room previews

These screenshots show the real dashboard layout with invented names and counts. They are **previews**, not proof of a live bot connection or a view into a real server. The screenshots were made from the real interface with sample data. This public showcase has no login or bot API access.

<!-- DASHBOARD_SCREENSHOTS -->

| Overview | Server switching and setup codes |
| --- | --- |
| <img width="640" alt="Synthetic 07 Control Room overview with bot status and server metrics" src="https://github.com/user-attachments/assets/66aa9d40-e26a-42da-8414-e731fb2402ab" /> | <img width="640" alt="Synthetic server selector and shareable setup codes" src="https://github.com/user-attachments/assets/5f47d42a-0693-4950-a64b-b1128ae59cbe" /> |

| Ticket desk | Separate member transcript website |
| --- | --- |
| <img width="640" alt="Synthetic support and purchase ticket desk" src="https://github.com/user-attachments/assets/2c63ee06-914b-40b7-acb2-a35d81dccfaf" /> | <img width="640" alt="Synthetic readable member transcript on separate 07 site" src="https://github.com/user-attachments/assets/6dcbf294-5b39-453a-b232-e692b9043f6a" /> |

| Welcome and automatic join role | Bot voice and AFK presence |
| --- | --- |
| <img width="640" alt="Synthetic welcome cards and automatic Unverified role settings" src="https://github.com/user-attachments/assets/b8fddb2e-f5f4-4713-a337-845d92f57d7c" /> | <img width="640" alt="Synthetic bot voice and presence controls" src="https://github.com/user-attachments/assets/42b3d04d-a10c-4a85-ae99-c5df4cfdf7f8" /> |

| Server guard | Activity and routed events |
| --- | --- |
| <img width="640" alt="Synthetic server guard configuration" src="https://github.com/user-attachments/assets/9c91a67c-1328-447a-b3cd-a5e58f72d06c" /> | <img width="640" alt="Synthetic activity log with verification and ticket events" src="https://github.com/user-attachments/assets/9cb95663-c172-4b25-aed1-893f4fd511ad" /> |

<img width="960" alt="Synthetic 07 Design Studio with banner and avatar gallery" src="https://github.com/user-attachments/assets/8927e2a3-167b-4883-a6fd-07e62deb0eaa" />

The private Control Room includes the remaining pages for invite tracking, XP, community, member lookup, command aliases, blackout, connections, updates, and settings.

### Private operator access

The Control Room has separate owner and developer sign-in. The public showcase is read-only; it does not expose an operator login or member transcript links.

## Everything the bot covers

| Area | What Sakura does |
| --- | --- |
| Server layout | Preview and apply a designed role/channel layout; check missing permissions; back up and restore. A separate owner-only reset previews a full wipe before applying it. |
| Verification and rules | Publish rules and a verification button. New members can receive Unverified; verifying changes them to Lunar, never to premium or staff. |
| Welcome | Custom greeting, invite attribution when identifiable, and 07 banner artwork. Preview and configure the welcome channel and wording. |
| Self roles | Color and ping panels, buttons or dropdowns, 07 banners, private selection feedback. |
| Member count and voice | A visible voice-channel count in the configured category; optional muted/deafened bot presence with reconnect. |
| Invite tracking | Counts member invites and can create a public read-only invite tracker; unknown/ambiguous joins are identified as such. |
| XP and ranks | Conversation XP with cooldown/cap, six purple rank stages, leaderboard and image rank cards. |
| Community | Away status, giveaways with restart recovery, random rolls, presence and public server information. |
| Moderation | Ban, kick, timeout, mute, custom moderation words, channel locks, alerts and member lookup. |
| Guard and blackout | Audit-log-backed protection, anti-bot/role checks, trust list and saved blackouts enforced on joins and catch-up scans. |
| Routed logs | Configure existing channels for moderation, bans, kicks, timeouts, mutes, deleted messages, joins/leaves, anti-bot, support and purchases. |
| Tickets | Separate support and purchase setups. Customize panel heading, description, buttons, categories, staff roles, archive location and log destination. Staff can reply from Discord or the dashboard. |
| Ticket archives | Close/reopen; export a readable transcript; route support and purchase logs separately. Owners get an archive copy; members get a private link on an independent site. Deleting an archived Discord channel does not revoke that member link. |
| Multiple servers | Only allowlisted servers are connected. Each approved server has separate community and ticket settings; the dashboard server selector changes the active scope. |
| Design Studio | Gallery of 37 banners and 37 matching avatars, plus profile image controls. |
| Private operations | Bot health, heartbeat, recent actions, server switching, updates, command aliases, owner/developer access. |

Start with `$setup` or use `$help` for the command guide. Setup actions answer privately where supported; public panels, welcome posts and logs remain visible in their intended channels. Discord permissions and role order determine what Sakura can actually change.

## Tickets and transcript separation

```text
Member opens support or purchase ticket
             │
             ▼
Private Discord channel ⇄ 07 bot ⇄ Control Room ticket desk
             │                        │
             └────── close ticket ────┘
                         │
               Save two separate copies
                 ┌───────┴────────┐
                 ▼                ▼
        Owner dashboard archive   Member transcript site
        (owner/developer access)  (private link for that ticket)
```

The separate transcript site has its own Worker and database. The dashboard does not link members back into its sign-in flow. A transcript link is private by possession: anyone with that URL can read the ticket, so it belongs in the member DM and authorized logs only.

## Full artwork catalog

The earlier 07 images are shown above. Every selectable Design Studio banner and matching avatar is retained in [the public artwork folder](../assets/art/). These are project files, not recreated mockups; the [Sakura profile artwork](../README.md#the-look) is separate.

<!-- ARTWORK_CATALOG -->

<details>
<summary>Colors — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Colors 1 | <img width="320" alt="Colors 1 legacy banner" src="../assets/art/colors-1.png" /> | <img width="96" alt="Colors 1 legacy avatar" src="../assets/art/colors-1-avatar.png" /> |
| Colors 2 | <img width="320" alt="Colors 2 legacy banner" src="../assets/art/colors-2.png" /> | <img width="96" alt="Colors 2 legacy avatar" src="../assets/art/colors-2-avatar.png" /> |
| Colors 3 | <img width="320" alt="Colors 3 legacy banner" src="../assets/art/colors-3.png" /> | <img width="96" alt="Colors 3 legacy avatar" src="../assets/art/colors-3-avatar.png" /> |
| Colors 4 | <img width="320" alt="Colors 4 legacy banner" src="../assets/art/colors-4.png" /> | <img width="96" alt="Colors 4 legacy avatar" src="../assets/art/colors-4-avatar.png" /> |
| Colors 5 | <img width="320" alt="Colors 5 legacy banner" src="../assets/art/colors-5.png" /> | <img width="96" alt="Colors 5 legacy avatar" src="../assets/art/colors-5-avatar.png" /> |

</details>

<details>
<summary>Pings — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Pings 1 | <img width="320" alt="Pings 1 legacy banner" src="../assets/art/pings-1.png" /> | <img width="96" alt="Pings 1 legacy avatar" src="../assets/art/pings-1-avatar.png" /> |
| Pings 2 | <img width="320" alt="Pings 2 legacy banner" src="../assets/art/pings-2.png" /> | <img width="96" alt="Pings 2 legacy avatar" src="../assets/art/pings-2-avatar.png" /> |
| Pings 3 | <img width="320" alt="Pings 3 legacy banner" src="../assets/art/pings-3.png" /> | <img width="96" alt="Pings 3 legacy avatar" src="../assets/art/pings-3-avatar.png" /> |
| Pings 4 | <img width="320" alt="Pings 4 legacy banner" src="../assets/art/pings-4.png" /> | <img width="96" alt="Pings 4 legacy avatar" src="../assets/art/pings-4-avatar.png" /> |
| Pings 5 | <img width="320" alt="Pings 5 legacy banner" src="../assets/art/pings-5.png" /> | <img width="96" alt="Pings 5 legacy avatar" src="../assets/art/pings-5-avatar.png" /> |

</details>

<details>
<summary>Welcome — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Welcome 1 | <img width="320" alt="Welcome 1 legacy banner" src="../assets/art/welcome-1.png" /> | <img width="96" alt="Welcome 1 legacy avatar" src="../assets/art/welcome-1-avatar.png" /> |
| Welcome 2 | <img width="320" alt="Welcome 2 legacy banner" src="../assets/art/welcome-2.png" /> | <img width="96" alt="Welcome 2 legacy avatar" src="../assets/art/welcome-2-avatar.png" /> |
| Welcome 3 | <img width="320" alt="Welcome 3 legacy banner" src="../assets/art/welcome-3.png" /> | <img width="96" alt="Welcome 3 legacy avatar" src="../assets/art/welcome-3-avatar.png" /> |
| Welcome 4 | <img width="320" alt="Welcome 4 legacy banner" src="../assets/art/welcome-4.png" /> | <img width="96" alt="Welcome 4 legacy avatar" src="../assets/art/welcome-4-avatar.png" /> |
| Welcome 5 | <img width="320" alt="Welcome 5 legacy banner" src="../assets/art/welcome-5.png" /> | <img width="96" alt="Welcome 5 legacy avatar" src="../assets/art/welcome-5-avatar.png" /> |

</details>

<details>
<summary>Giveaways — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Giveaways 1 | <img width="320" alt="Giveaways 1 legacy banner" src="../assets/art/giveaways-1.png" /> | <img width="96" alt="Giveaways 1 legacy avatar" src="../assets/art/giveaways-1-avatar.png" /> |
| Giveaways 2 | <img width="320" alt="Giveaways 2 legacy banner" src="../assets/art/giveaways-2.png" /> | <img width="96" alt="Giveaways 2 legacy avatar" src="../assets/art/giveaways-2-avatar.png" /> |
| Giveaways 3 | <img width="320" alt="Giveaways 3 legacy banner" src="../assets/art/giveaways-3.png" /> | <img width="96" alt="Giveaways 3 legacy avatar" src="../assets/art/giveaways-3-avatar.png" /> |
| Giveaways 4 | <img width="320" alt="Giveaways 4 legacy banner" src="../assets/art/giveaways-4.png" /> | <img width="96" alt="Giveaways 4 legacy avatar" src="../assets/art/giveaways-4-avatar.png" /> |
| Giveaways 5 | <img width="320" alt="Giveaways 5 legacy banner" src="../assets/art/giveaways-5.png" /> | <img width="96" alt="Giveaways 5 legacy avatar" src="../assets/art/giveaways-5-avatar.png" /> |

</details>

<details>
<summary>Original series — 17 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Original series 01 | <img width="320" alt="Original series 01 legacy banner" src="../assets/art/eclipse-01.png" /> | <img width="96" alt="Original series 01 legacy avatar" src="../assets/art/eclipse-01-avatar.png" /> |
| Original series 02 | <img width="320" alt="Original series 02 legacy banner" src="../assets/art/eclipse-02.png" /> | <img width="96" alt="Original series 02 legacy avatar" src="../assets/art/eclipse-02-avatar.png" /> |
| Original series 03 | <img width="320" alt="Original series 03 legacy banner" src="../assets/art/eclipse-03.png" /> | <img width="96" alt="Original series 03 legacy avatar" src="../assets/art/eclipse-03-avatar.png" /> |
| Original series 04 | <img width="320" alt="Original series 04 legacy banner" src="../assets/art/eclipse-04.png" /> | <img width="96" alt="Original series 04 legacy avatar" src="../assets/art/eclipse-04-avatar.png" /> |
| Original series 05 | <img width="320" alt="Original series 05 legacy banner" src="../assets/art/eclipse-05.png" /> | <img width="96" alt="Original series 05 legacy avatar" src="../assets/art/eclipse-05-avatar.png" /> |
| Original series 06 | <img width="320" alt="Original series 06 legacy banner" src="../assets/art/eclipse-06.png" /> | <img width="96" alt="Original series 06 legacy avatar" src="../assets/art/eclipse-06-avatar.png" /> |
| Original series 07 | <img width="320" alt="Original series 07 legacy banner" src="../assets/art/eclipse-07.png" /> | <img width="96" alt="Original series 07 legacy avatar" src="../assets/art/eclipse-07-avatar.png" /> |
| Original series 08 | <img width="320" alt="Original series 08 legacy banner" src="../assets/art/eclipse-08.png" /> | <img width="96" alt="Original series 08 legacy avatar" src="../assets/art/eclipse-08-avatar.png" /> |
| Original series 09 | <img width="320" alt="Original series 09 legacy banner" src="../assets/art/eclipse-09.png" /> | <img width="96" alt="Original series 09 legacy avatar" src="../assets/art/eclipse-09-avatar.png" /> |
| Original series 10 | <img width="320" alt="Original series 10 legacy banner" src="../assets/art/eclipse-10.png" /> | <img width="96" alt="Original series 10 legacy avatar" src="../assets/art/eclipse-10-avatar.png" /> |
| Original series 11 | <img width="320" alt="Original series 11 legacy banner" src="../assets/art/eclipse-11.png" /> | <img width="96" alt="Original series 11 legacy avatar" src="../assets/art/eclipse-11-avatar.png" /> |
| Original series 12 | <img width="320" alt="Original series 12 legacy banner" src="../assets/art/eclipse-12.png" /> | <img width="96" alt="Original series 12 legacy avatar" src="../assets/art/eclipse-12-avatar.png" /> |
| Original series 13 | <img width="320" alt="Original series 13 legacy banner" src="../assets/art/eclipse-13.png" /> | <img width="96" alt="Original series 13 legacy avatar" src="../assets/art/eclipse-13-avatar.png" /> |
| Original series 14 | <img width="320" alt="Original series 14 legacy banner" src="../assets/art/eclipse-14.png" /> | <img width="96" alt="Original series 14 legacy avatar" src="../assets/art/eclipse-14-avatar.png" /> |
| Original series 15 | <img width="320" alt="Original series 15 legacy banner" src="../assets/art/eclipse-15.png" /> | <img width="96" alt="Original series 15 legacy avatar" src="../assets/art/eclipse-15-avatar.png" /> |
| Original series 16 | <img width="320" alt="Original series 16 legacy banner" src="../assets/art/eclipse-16.png" /> | <img width="96" alt="Original series 16 legacy avatar" src="../assets/art/eclipse-16-avatar.png" /> |
| Original series 17 | <img width="320" alt="Original series 17 legacy banner" src="../assets/art/eclipse-17.png" /> | <img width="96" alt="Original series 17 legacy avatar" src="../assets/art/eclipse-17-avatar.png" /> |

</details>


## About this public copy

This repository contains the shareable docs, artwork, and sample screenshots. It contains no bot source, dashboard implementation, deployment settings, login keys, member data, or private ticket transcripts. The live Control Room and member transcript pages remain separate.

[Add Sakura to your server](https://discord.com/oauth2/authorize?client_id=1555856888367947796).
