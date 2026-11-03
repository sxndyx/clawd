# Security and privacy

## Reporting a problem

If you find a security issue in Clawd, please don't open a public issue. Use **Send feedback** in Clawd's menu or on [getclawd.dev](https://getclawd.dev) and choose **Bug**, mentioning that it's security related, and I'll get back to you. Please include the Clawd version (shown under Updates in his menu) and your macOS version.

Only the latest version is supported. Clawd updates himself, so fixes reach everyone automatically.

## What Clawd touches

**On your Mac**

- `~/.claude/settings.json`: Connect adds hook entries for a few Claude Code events, pointing at Clawd. Your original file is saved first as `settings.json.before-clawd`, and nothing else in it is changed. Disconnect removes them again.
- Clawd's own settings, stats and finds, in his preferences and `~/Library/Application Support/Clawd`.
- Optionally, a login item, so he opens when you log in (on by default, off in Advanced Settings).

**What the hooks tell him**

When a prompt starts and stops, which tool Claude is using and a short label for it (like a file name), and when Claude needs you. Your prompts, Claude's replies and your code are never sent anywhere.

**On the network**

| What | Where | When |
|---|---|---|
| Update check | getclawd.dev | Every few hours |
| Update download | GitHub Releases | When there's a new version, checked against a published SHA-256 |
| Album art | iTunes Search, Spotify | While a song is playing |
| Lyrics | lrclib.net | While a song plays, if Sing the Lyrics is on |
| Rare find counts | Firebase | When you find one: an anonymous count per find, nothing about you |
| Feedback | Firebase | Only when you send it |

There's no account, analytics, advertising or tracking.

**Permissions**

- **Accessibility:** only if you turn on following Claude app chats, to see when a chat is replying.
- **Window positions:** read to dodge full-screen videos and hop onto screenshot thumbnails. What's in your windows is never read.
