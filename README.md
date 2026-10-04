# 07 — visual and feature showcase

This public page shows the 07 Discord bot, its private owner/developer Control Room, and the separate transcript website for members. The images are real project artwork. Dashboard screenshots use the actual interface with invented sample data; no real server, member, ticket, key, or transcript is shown. The runnable bot and dashboard source remain in a separate private repository.

**Want 07 in your server? Contact me on Discord: `082_0`.** The bot and website source code are closed; this public page shows what I built.

[Full feature guide](docs/FEATURES.md) · [Project notes](docs/SETUP.md) · [Change history](docs/CHANGELOG.md) · [Showcase document](docs/SHOWCASE.md)

## The 07 look

![Purple 07 Colors self-role banner](assets/art/07-colors-panel.png)

The color-role panel uses purple 07 artwork. A member can pick one color at a time; selecting the current color again removes it. The bot switches between buttons and a dropdown based on the number of choices, and the member's confirmation is private.

![Black 07 Pings self-role banner](assets/art/07-pings-panel.png)

The ping panel uses the black 07 version. Members opt in to announcement, release, poll, or other configured ping roles. These are notification roles, never staff or premium access.

| Welcome | Verification |
| --- | --- |
| ![07 welcome panel art](assets/art/07-welcome-panel.png) | ![07 verification panel art](assets/art/07-verify-panel.png) |

| Main banner | Avatar |
| --- | --- |
| ![07 main banner](assets/art/07-banner.png) | ![07 avatar](assets/art/07-avatar.png) |

The [Design Studio gallery](#full-artwork-catalog) also contains 37 selectable banner designs and 37 matching avatars. **Those older selectable designs still contain Eclipse text**, so they are preserved as legacy artwork rather than presented as current 07 branding. The four large 07 panel images above are the current art. See [the full artwork catalog](#full-artwork-catalog) below.

## Control Room previews

These screenshots show the real dashboard layout with invented names and counts. They are **previews**, not proof of a live bot connection or a view into a real server. The screenshots were made from the real interface with sample data. This public showcase has no login or bot API access.

<!-- DASHBOARD_SCREENSHOTS -->

| Overview | Server switching and setup codes |
| --- | --- |
| <img width="640" alt="Synthetic 07 Control Room overview with bot status and server metrics" src="SCREEN_OVERVIEW" /> | <img width="640" alt="Synthetic server selector and shareable setup codes" src="SCREEN_SERVERS" /> |

| Ticket desk | Separate member transcript website |
| --- | --- |
| <img width="640" alt="Synthetic support and purchase ticket desk" src="SCREEN_TICKETS" /> | <img width="640" alt="Synthetic readable member transcript on separate 07 site" src="SCREEN_TRANSCRIPT" /> |

| Welcome and automatic join role | Bot voice and AFK presence |
| --- | --- |
| <img width="640" alt="Synthetic welcome cards and automatic Unverified role settings" src="SCREEN_WELCOME" /> | <img width="640" alt="Synthetic bot voice and presence controls" src="SCREEN_CONTROL" /> |

| Server guard | Activity and routed events |
| --- | --- |
| <img width="640" alt="Synthetic server guard configuration" src="SCREEN_SECURITY" /> | <img width="640" alt="Synthetic activity log with verification and ticket events" src="SCREEN_LOGS" /> |

<img width="960" alt="Synthetic 07 Design Studio with banner and avatar gallery" src="SCREEN_STUDIO" />

The private Control Room includes the remaining pages for invite tracking, XP, community, member lookup, command aliases, blackout, connections, updates, and settings.

### Private operator access

The Control Room has separate owner and developer sign-in. The public showcase is read-only; it does not expose an operator login or member transcript links.

## Everything the bot covers

| Area | What 07 does |
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

The owner-only `orbit help` menu documents the active commands. Setup actions answer privately where supported; public panels, welcome posts and logs remain visible in their intended channels. Discord permissions and role order still determine what 07 can actually change.

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

The six 07 core images are shown above. Every selectable Design Studio banner and matching avatar is retained in [the public artwork folder](assets/art/). The 37 older designs are clearly marked as legacy until they are redesigned with 07 text. These are actual project files; no image is a recreated mockup.

<!-- ARTWORK_CATALOG -->

<details>
<summary>Colors — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Colors 1 | <img width="320" alt="Colors 1 legacy banner" src="assets/art/colors-1.png" /> | <img width="96" alt="Colors 1 legacy avatar" src="assets/art/colors-1-avatar.png" /> |
| Colors 2 | <img width="320" alt="Colors 2 legacy banner" src="assets/art/colors-2.png" /> | <img width="96" alt="Colors 2 legacy avatar" src="assets/art/colors-2-avatar.png" /> |
| Colors 3 | <img width="320" alt="Colors 3 legacy banner" src="assets/art/colors-3.png" /> | <img width="96" alt="Colors 3 legacy avatar" src="assets/art/colors-3-avatar.png" /> |
| Colors 4 | <img width="320" alt="Colors 4 legacy banner" src="assets/art/colors-4.png" /> | <img width="96" alt="Colors 4 legacy avatar" src="assets/art/colors-4-avatar.png" /> |
| Colors 5 | <img width="320" alt="Colors 5 legacy banner" src="assets/art/colors-5.png" /> | <img width="96" alt="Colors 5 legacy avatar" src="assets/art/colors-5-avatar.png" /> |

</details>

<details>
<summary>Pings — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Pings 1 | <img width="320" alt="Pings 1 legacy banner" src="assets/art/pings-1.png" /> | <img width="96" alt="Pings 1 legacy avatar" src="assets/art/pings-1-avatar.png" /> |
| Pings 2 | <img width="320" alt="Pings 2 legacy banner" src="assets/art/pings-2.png" /> | <img width="96" alt="Pings 2 legacy avatar" src="assets/art/pings-2-avatar.png" /> |
| Pings 3 | <img width="320" alt="Pings 3 legacy banner" src="assets/art/pings-3.png" /> | <img width="96" alt="Pings 3 legacy avatar" src="assets/art/pings-3-avatar.png" /> |
| Pings 4 | <img width="320" alt="Pings 4 legacy banner" src="assets/art/pings-4.png" /> | <img width="96" alt="Pings 4 legacy avatar" src="assets/art/pings-4-avatar.png" /> |
| Pings 5 | <img width="320" alt="Pings 5 legacy banner" src="assets/art/pings-5.png" /> | <img width="96" alt="Pings 5 legacy avatar" src="assets/art/pings-5-avatar.png" /> |

</details>

<details>
<summary>Welcome — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Welcome 1 | <img width="320" alt="Welcome 1 legacy banner" src="assets/art/welcome-1.png" /> | <img width="96" alt="Welcome 1 legacy avatar" src="assets/art/welcome-1-avatar.png" /> |
| Welcome 2 | <img width="320" alt="Welcome 2 legacy banner" src="assets/art/welcome-2.png" /> | <img width="96" alt="Welcome 2 legacy avatar" src="assets/art/welcome-2-avatar.png" /> |
| Welcome 3 | <img width="320" alt="Welcome 3 legacy banner" src="assets/art/welcome-3.png" /> | <img width="96" alt="Welcome 3 legacy avatar" src="assets/art/welcome-3-avatar.png" /> |
| Welcome 4 | <img width="320" alt="Welcome 4 legacy banner" src="assets/art/welcome-4.png" /> | <img width="96" alt="Welcome 4 legacy avatar" src="assets/art/welcome-4-avatar.png" /> |
| Welcome 5 | <img width="320" alt="Welcome 5 legacy banner" src="assets/art/welcome-5.png" /> | <img width="96" alt="Welcome 5 legacy avatar" src="assets/art/welcome-5-avatar.png" /> |

</details>

<details>
<summary>Giveaways — 5 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Giveaways 1 | <img width="320" alt="Giveaways 1 legacy banner" src="assets/art/giveaways-1.png" /> | <img width="96" alt="Giveaways 1 legacy avatar" src="assets/art/giveaways-1-avatar.png" /> |
| Giveaways 2 | <img width="320" alt="Giveaways 2 legacy banner" src="assets/art/giveaways-2.png" /> | <img width="96" alt="Giveaways 2 legacy avatar" src="assets/art/giveaways-2-avatar.png" /> |
| Giveaways 3 | <img width="320" alt="Giveaways 3 legacy banner" src="assets/art/giveaways-3.png" /> | <img width="96" alt="Giveaways 3 legacy avatar" src="assets/art/giveaways-3-avatar.png" /> |
| Giveaways 4 | <img width="320" alt="Giveaways 4 legacy banner" src="assets/art/giveaways-4.png" /> | <img width="96" alt="Giveaways 4 legacy avatar" src="assets/art/giveaways-4-avatar.png" /> |
| Giveaways 5 | <img width="320" alt="Giveaways 5 legacy banner" src="assets/art/giveaways-5.png" /> | <img width="96" alt="Giveaways 5 legacy avatar" src="assets/art/giveaways-5-avatar.png" /> |

</details>

<details>
<summary>Original series — 17 legacy banner/avatar pairs</summary>

| Design | Banner | Avatar |
| --- | --- | --- |
| Original series 01 | <img width="320" alt="Original series 01 legacy banner" src="assets/art/eclipse-01.png" /> | <img width="96" alt="Original series 01 legacy avatar" src="assets/art/eclipse-01-avatar.png" /> |
| Original series 02 | <img width="320" alt="Original series 02 legacy banner" src="assets/art/eclipse-02.png" /> | <img width="96" alt="Original series 02 legacy avatar" src="assets/art/eclipse-02-avatar.png" /> |
| Original series 03 | <img width="320" alt="Original series 03 legacy banner" src="assets/art/eclipse-03.png" /> | <img width="96" alt="Original series 03 legacy avatar" src="assets/art/eclipse-03-avatar.png" /> |
| Original series 04 | <img width="320" alt="Original series 04 legacy banner" src="assets/art/eclipse-04.png" /> | <img width="96" alt="Original series 04 legacy avatar" src="assets/art/eclipse-04-avatar.png" /> |
| Original series 05 | <img width="320" alt="Original series 05 legacy banner" src="assets/art/eclipse-05.png" /> | <img width="96" alt="Original series 05 legacy avatar" src="assets/art/eclipse-05-avatar.png" /> |
| Original series 06 | <img width="320" alt="Original series 06 legacy banner" src="assets/art/eclipse-06.png" /> | <img width="96" alt="Original series 06 legacy avatar" src="assets/art/eclipse-06-avatar.png" /> |
| Original series 07 | <img width="320" alt="Original series 07 legacy banner" src="assets/art/eclipse-07.png" /> | <img width="96" alt="Original series 07 legacy avatar" src="assets/art/eclipse-07-avatar.png" /> |
| Original series 08 | <img width="320" alt="Original series 08 legacy banner" src="assets/art/eclipse-08.png" /> | <img width="96" alt="Original series 08 legacy avatar" src="assets/art/eclipse-08-avatar.png" /> |
| Original series 09 | <img width="320" alt="Original series 09 legacy banner" src="assets/art/eclipse-09.png" /> | <img width="96" alt="Original series 09 legacy avatar" src="assets/art/eclipse-09-avatar.png" /> |
| Original series 10 | <img width="320" alt="Original series 10 legacy banner" src="assets/art/eclipse-10.png" /> | <img width="96" alt="Original series 10 legacy avatar" src="assets/art/eclipse-10-avatar.png" /> |
| Original series 11 | <img width="320" alt="Original series 11 legacy banner" src="assets/art/eclipse-11.png" /> | <img width="96" alt="Original series 11 legacy avatar" src="assets/art/eclipse-11-avatar.png" /> |
| Original series 12 | <img width="320" alt="Original series 12 legacy banner" src="assets/art/eclipse-12.png" /> | <img width="96" alt="Original series 12 legacy avatar" src="assets/art/eclipse-12-avatar.png" /> |
| Original series 13 | <img width="320" alt="Original series 13 legacy banner" src="assets/art/eclipse-13.png" /> | <img width="96" alt="Original series 13 legacy avatar" src="assets/art/eclipse-13-avatar.png" /> |
| Original series 14 | <img width="320" alt="Original series 14 legacy banner" src="assets/art/eclipse-14.png" /> | <img width="96" alt="Original series 14 legacy avatar" src="assets/art/eclipse-14-avatar.png" /> |
| Original series 15 | <img width="320" alt="Original series 15 legacy banner" src="assets/art/eclipse-15.png" /> | <img width="96" alt="Original series 15 legacy avatar" src="assets/art/eclipse-15-avatar.png" /> |
| Original series 16 | <img width="320" alt="Original series 16 legacy banner" src="assets/art/eclipse-16.png" /> | <img width="96" alt="Original series 16 legacy avatar" src="assets/art/eclipse-16-avatar.png" /> |
| Original series 17 | <img width="320" alt="Original series 17 legacy banner" src="assets/art/eclipse-17.png" /> | <img width="96" alt="Original series 17 legacy avatar" src="assets/art/eclipse-17-avatar.png" /> |

</details>


## About this public copy

This repository contains the shareable docs, artwork, and sample screenshots. It contains no bot source, dashboard implementation, deployment settings, login keys, real Discord IDs, member data, or private ticket transcripts. The live Control Room and member transcript pages remain separate.
