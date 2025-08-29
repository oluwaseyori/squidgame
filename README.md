# Red Light • Green Light — Telegram Game Bot (Docs)

<p align="center">
  <img src="https://files.catbox.moe/64yrc4.png" alt="Bot description banner" width="100%" style="max-width:960px;">
</p>

This repository explains how to use the **Red Light / Green Light** Telegram game bot in your group chats — no source code is published here.

<p align="center">
  <a href="https://t.me/seyorisquidgamebot?startgroup=true"
     style="display:inline-block;padding:10px 16px;background:#2ea44f;color:#fff;border-radius:8px;text-decoration:none;font-weight:600;margin-right:8px;">
    ➕ Add to Group
  </a>
  <a href="https://t.me/seyorisquidgamebot"
     style="display:inline-block;padding:10px 16px;background:#111827;color:#fff;border:1px solid #333;border-radius:8px;text-decoration:none;font-weight:600;margin-right:8px;">
    Open Bot
  </a>
  <a href="https://t.me/s3yori"
     style="display:inline-block;padding:10px 16px;background:#0b5fff;color:#fff;border-radius:8px;text-decoration:none;font-weight:600;">
    Contact Owner
  </a>
</p>

---

## What this bot does

- Flips between **GREEN** and **RED** at random intervals within a range you set.
- During **RED**, any non-admin who sends a message is **muted** until the round ends.
- On **/stopgame**, the bot **un-mutes** violators and posts a summary that *tags* them  
  (`@username` when available, otherwise a clickable first name).

---

## Quick Start

1. Open the bot: **[@seyorisquidgamebot](https://t.me/seyorisquidgamebot)**
2. Tap **Add to Group** and select your group.
3. Make the bot **Admin** with **Restrict Members** permission.
4. Use the commands below to run a round.

> Works in groups/supergroups. The owner has configured privacy so the bot can see messages and enforce RED.

---

## Commands

- `/startgame <min> <max>` — Start a round. Bot switches GREEN/RED at random within `min..max` seconds  
  (example: `/startgame 5 20`).
- `/stopgame` — End the round, un-mute violators, and post the summary.
- `/status` — Show current phase and muted count.
- `/commands` — Show the command list.

**Who can control the game?** The **Owner** or **any group admin**.

---

## Tips & Notes

- The bot must be **Admin** with **Restrict Members**.
- Admins cannot be muted by Telegram; admin violations are ignored.
- Mentions: uses `@username` if present; otherwise a **clickable first name** via `tg://user?id=...`.
- Switching is randomized with a secure RNG so it can’t be predicted.
- Live demo link for reference: **[t.me/seyorisquidgamebot](https://t.me/seyorisquidgamebot)**

---

## FAQ

**The bot didn’t mute someone on RED — why?**  
• They might be an **admin** (admins can’t be restricted).  
• The bot may lack **Restrict Members**.  
• They may have sent the message during **GREEN**.  
• If you just added the bot, ensure it’s admin and try again.

**Does the bot store data?**  
• It keeps minimal per-round info (session + violator IDs) to produce the summary and basic stats. No message content is stored.

**Can I see the source code?**  
• Not in this repository. This is **documentation-only**.

---

## Contact

- Owner: **[@s3yori](https://t.me/s3yori)**
- Live Bot: **[@seyorisquidgamebot](https://t.me/seyorisquidgamebot)**
- Add to Group: **[link](https://t.me/seyorisquidgamebot?startgroup=true)**

---

### License

Documentation © Seyori. All rights reserved. This repository contains **no source code**.
