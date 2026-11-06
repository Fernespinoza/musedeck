# Muse Deck

A personal command deck for [Muse](https://muse.ai) on Windows.

Meta doesn't ship a Windows app for Muse, and a browser tab never felt
like a home for it — so I built one. Muse Deck is a desktop window with
the real muse.ai chat on the left and a working deck on the right:
glanceable tiles, a notes board, a whiteboard, a big-screen Stage, my
Obsidian vault, and themes. One hotkey summons it, one hotkey puts it
away.

**Win+Shift+D** — that's the whole interaction model.

> Not affiliated with Meta. Muse Deck is a personal project, built for
> one person (me) and shared as-is. It needs a Muse account, because
> the chat pane *is* muse.ai, signed in as you.
>
> Name note: this is Muse **Deck** — tiles, board, stage. Other
> projects with similar names are different apps.

## Install

1. Download the latest zip from [Releases](../../releases/latest).
2. Unzip it into a **permanent folder** (e.g. `Documents\MuseDeck`).
   Don't run it from the zip or a temp folder — the auto-updater swaps
   the program files in that folder.
3. Run `MuseDeck.exe`.

Windows will warn that the app is unsigned (SmartScreen: "More info" →
"Run anyway"). That's expected for a community build; the releases here
are the only official source.

Requirements: Windows 10/11, and the WebView2 runtime (built into
Windows 11 and current Windows 10; if the window opens blank, install
the [Evergreen WebView2 runtime](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)
from Microsoft).

All your data — settings, notes, whiteboard — lives in
`%LocalAppData%\MuseDeck`, never in the program folder, so updates
can't touch it. The Deck sends no telemetry anywhere.

## What's in the deck

- **The chat pane** — the real muse.ai in WebView2, signed in as you.
  A blue dot lands on the taskbar and tray icons when a reply finishes
  while you're in another app, so you can ask something, go work, and
  get pulled back when it's done.
- **The daily ribbon** — six tiles under the chat: clock, local weather
  (National Weather Service), calendar, top headline, projects, and
  device battery. Tap a tile and its full detail opens big on the
  Stage. A drag divider trades ribbon height for chat height.
- **Board** — notes (add, edit, pin, delete) and a whiteboard that
  auto-saves and exports PNG.
- **Stage** — the big screen. Ribbon details land here as real text,
  never a picture of text.
- **Vault** — if you keep an Obsidian vault, point the Deck at the
  folder once: browse and read your notes big, `[[links]]` as tappable
  chips, edit with autosave, quick-capture into the vault's Inbox, and
  a note map (the vault graph) one toggle away.
- **Tray + hotkey** — closing the window parks it in the tray; it's
  always one **Win+Shift+D** away. It remembers its layout and focus.
- **Auto-update** — the Deck checks the latest release here on launch.
  The ☰ menu's Update applies a staged build in one click, and a
  one-time "What's new" popup tells you what changed.
- **Crash logging** — if the Deck ever dies, `%LocalAppData%\MuseDeck`
  holds `health.log` and `crash.log` that say why.

## Themes

Themes live in the ☰ menu, under **Themes**, and a theme owns the
*whole* window — tiles, tab strip, lists, editors, scrollbars, menus.
Four ship today:

- **Deck Classic** — the original dark look.
- **Avatar Match** — derived from my Muse avatar (a holographic
  creature in a crimson beanie and gold shades): cyan-blue glow over
  charcoal, crimson as the quiet secondary, gold for highlights.
- **Neon Rain** — city-pop indigo and violet, sky blue, magenta.
- **Golden Hour** — neo-soul espresso, brass gold, cream text.

## The channel (optional, personal)

The Deck can poll a **private** GitHub repo — your own — every 30
seconds for a small JSON file: calendar summary, project counts, phone
battery, notes from your agent, items for the Stage, and a snapshot of
your whiteboard flowing the other way. Setup is one fine-grained
GitHub token scoped to that single repo, pasted once (the ☰ menu's
"Channel setup...", or just choose "Not now" and it never asks again).

Two honest notes:

- The channel is the personal layer of *my* setup — the writer on the
  other end is part of my own agent infrastructure and isn't included
  here. The Deck's side is complete, but unless you run a similar
  setup, this section is a curiosity, not a feature. Everything above
  works fully without it.
- The channel's privacy line is hard: headlines and status only —
  never email or message contents, health details, or financial
  figures.

## Status

Built in the open, one build at a time, since November 2026. Current
feature set: shell, ribbon, Board, Stage, Vault, channel, themes.
A phone companion is designed but not built.

<!-- Screenshots — add with the community post (Fernando's captures,
     Avatar Match theme):
     docs/shot-1-hero.png     full window, ribbon + Board
     docs/shot-2-stage.png    Stage detail view
     docs/shot-3-vault.png    Vault tab with note map
     docs/shot-4-themes.png   hamburger menu, Themes expanded
     docs/shot-5-golden.png   full window, Golden Hour theme
     Then replace this comment with:
     ## Screenshots
     ![The deck](docs/shot-1-hero.png)
     ![Stage](docs/shot-2-stage.png)
     ![Vault note map](docs/shot-3-vault.png)
     ![Themes menu](docs/shot-4-themes.png)
     ![Golden Hour](docs/shot-5-golden.png)
-->
