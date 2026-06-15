# WaitLine

Turn the Claude Code wait line into a single tasteful sponsored slot — and get
**revenue-shared** for it. One quiet "Sponsored" line in your status bar while
Claude thinks. No popups, no tracking pixels, no noise.

- **One slot.** A single sponsored line in the status bar, rotating gently.
- **Opt-in.** Nothing changes until you run `/waitline:setup` and see exactly
  what gets written to your `settings.json`.
- **You earn.** Sign in to attribute impressions to your account and get paid out
  in crypto (USDT on Solana).
- **Reversible.** `/waitline:uninstall` restores your settings from a verbatim
  backup, any time.

## Install

```
/plugin marketplace add waitline/waitline-plugin
/plugin install waitline@waitline-marketplace
```

Then activate it (you'll be shown exactly what will be written to
`~/.claude/settings.json` before anything changes):

```
/waitline:setup
```

The status line appears immediately. The sponsored spinner verb takes effect on
your next Claude Code session.

## Earn

By default impressions accrue to this machine anonymously. To attribute them to
your real account (earnings follow you across machines) and to cash out:

```
/waitline:signin
```

This pairs the machine with your WaitLine account via a browser approval, then
merges any earnings already accrued on this machine into your account.

## Commands

| Command | What it does |
|---------|--------------|
| `/waitline:setup` | Activate — write the sponsored statusLine + spinnerVerbs (with consent + backup). |
| `/waitline:signin` | Pair this machine with your account so impressions become earnings. |
| `/waitline:uninstall` | Deactivate — restore `settings.json` from the backup. |

## Privacy

WaitLine only ever writes two keys to your settings (`statusLine`, `spinnerVerbs`),
and only after you run `/waitline:setup`. A verbatim backup of your original
settings is saved to `~/.waitline/settings.backup.json`. All WaitLine state lives
under `~/.waitline/`. Uninstall restores everything.

## License

Proprietary. See [LICENSE](./LICENSE). © 2026 WaitLine — https://getwaitline.com
