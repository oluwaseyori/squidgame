# Red Light • Green Light — Telegram Game Bot (Docs)

This repository explains how to use the **Red Light / Green Light** Telegram game bot in your own group chats — no source code is published here.

**Live bot:** [t.me/seyorisquidgamebot](https://t.me/seyorisquidgamebot)  
**Add to a group:** [➕ Add to Group](https://t.me/seyorisquidgamebot?startgroup=true)  
**Owner:** [Seyori](https://t.me/s3yori)

<p align="center">
  <img src="https://files.catbox.moe/64yrc4.png" alt="Bot description banner" width="640">
</p>
---

## What this bot does

- Flips between **GREEN** and **RED** phases at random intervals within the range you set.
- During **RED**, any non‑admin who sends a message is **muted** until the round ends.
- When you end the round, the bot **un‑mutes** violators and posts a summary that tags them: `@username` when available, otherwise a clickable first name.

---

## Quick Start

1. Open the bot: **[t.me/seyorisquidgamebot](https://t.me/seyorisquidgamebot)**  
2. Tap **➕ Add to Group** and select your group.  
3. Make the bot **Admin** with **Restrict Members** permission.  
4. Use the commands below to run a round.

> Tip: The bot works in **groups/supergroups**. It needs to see messages to enforce RED, so the owner has already configured privacy appropriately.

---

## Commands

- `/startgame <min> <max>` — Start a round. The bot flips GREEN/RED at random within `min..max` seconds (e.g. `/startgame 5 20`).  
- `/stopgame` — End the round, un‑mute violators, and post the summary.  
- `/status` — Show the current phase and number of muted users.  
- `/commands` — Show the commands in chat.

**Who can control the game?** The **Owner** or **any group admin**.

---

## Requirements & Notes

- The bot must be **Admin** with the **Restrict Members** permission.  
- Admins cannot be muted by Telegram, so violations from admins are ignored.  
- The summary tags users as `@username` when available; otherwise it uses a **clickable first name**.  
- Randomness uses a secure RNG to prevent predictable switching.

---

## FAQ

**Q: The bot didn’t mute someone on RED. Why?**  
• They might be an **admin** (admins can’t be restricted).  
• The bot might not have **Restrict Members** permission.  
• The round may have been in **GREEN** when they sent the message.  
• If you just added the bot, ensure it’s **Admin** and try again.

**Q: Does the bot keep data?**  
• It stores a minimal record per round (session + violator IDs) to produce the summary and basic stats. No message content is stored.

**Q: Can I see the source code?**  
• Not in this repository. This repo is **documentation‑only**.

---

## Contact & Support

- Owner: **[@s3yori](https://t.me/s3yori)**  
- Live bot: **[@seyorisquidgamebot](https://t.me/seyorisquidgamebot)**  
- Have feedback? Open an issue explaining your group setup and what happened.

---
<p align="center">
  <a href="https://t.me/seyorisquidgamebot?startgroup=true"
     style="display:inline-block;padding:10px 16px;background:#2ea44f;color:#fff;
            border-radius:8px;text-decoration:none;font-weight:600;margin-right:8px;">
    ➕ Add to Group
  </a>
  <a href="https://t.me/s3yori"
     style="display:inline-block;padding:10px 16px;background:#0b5fff;color:#fff;
            border-radius:8px;text-decoration:none;font-weight:600;">
    Contact Owner
  </a>
</p>

---

### Legal

Documentation © 2025 Seyori. All rights reserved. This repository contains **no source code**.
