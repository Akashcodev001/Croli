# Croli

Jump to older dates in Instagram Web chats without manually scrolling through
months or years of shared content.

## Why I built this

Croli is a small browser extension created primarily for personal use.

I often share study reels, notes, references, and other useful reels with
myself on Instagram. Some of these saved conversations contain content shared
more than a year ago, while others are only a few months old. When I want to
revisit something, I usually remember approximately when I shared it and want
to start from that date.

Instagram does not make this experience especially convenient. Finding an old
reel by scrolling manually can take a long time because:

- older messages and media load progressively;
- repeated scrolling becomes slow and tiring;
- the mouse wheel or trackpad may need to be used continuously;
- the conversation can become difficult to navigate when it contains a large
  amount of shared content; and
- a small mistake may require scrolling through the same section again.

Croli was made to reduce that friction. Instead of repeatedly scrolling by
hand, I can enter a date and let the extension move through the Instagram Web
conversation until it reaches the relevant time period. This makes it easier
to revisit study reels, references, and other personal content shared in the
past.

## What Croli does

- Finds the message list in a supported Instagram Web conversation.
- Accepts a target date so older content can be located more directly.
- Scrolls the conversation automatically instead of requiring continuous
  manual scrolling.
- Waits for additional conversation content to load while navigating.
- Provides progress and status information while a search is running.
- Allows a running search to be stopped or paused when needed.
- Runs locally in the browser.

Croli is intended to help locate a time period, not to download, copy, or
organize Instagram media.

## Privacy

Croli is designed for local, personal use:

- it runs in the browser;
- it does not use a remote backend;
- it does not send conversation data to an external service; and
- date and timeline text are inspected locally only to identify the relevant
  conversation position.

The extension requires access to Instagram Web pages so it can identify the
conversation scroll area, detect date markers locally, and control scrolling
on the active page. It does not upload message text or media.

## Requirements

- Google Chrome 110 or later
- Instagram Web
- An open Instagram Direct conversation

## Installation

Croli is currently loaded as an unpacked Chrome extension:

1. Download or clone this project.
2. Open `chrome://extensions` in Google Chrome.
3. Enable **Developer mode**.
4. Select **Load unpacked**.
5. Choose the project folder containing `manifest.json`.
6. Keep the extension enabled.

After installation, pin Croli to the Chrome toolbar if you want quick access.

## How to use it

1. Open Instagram Web.
2. Open the Direct conversation containing the content you want to revisit.
3. Select the Croli extension from the Chrome toolbar.
4. Enter the date you want to reach.
5. Start the search.
6. Let Croli automatically navigate through the conversation.
7. Stop or pause the search when the relevant content is visible.

Because Instagram can load conversation content dynamically, the time required
depends on the amount of history between the current position and the target
date, as well as the network connection.

## Supported date formats

Croli accepts common date formats, including:

- `YYYY-MM-DD`
- `Month Day, Year`
- `Day Month Year`
- dates with an omitted year when the year can be inferred from the
  conversation
- relative dates such as `today` and `yesterday`

For the most predictable result, use the ISO format `YYYY-MM-DD`, for example
`2025-08-15`.

## Limitations

- Croli is designed for Instagram Web conversations and is not a general
  Instagram search tool.
- The target conversation must be open before starting a search.
- Instagram can change its page structure, which may affect how the extension
  detects the message list.
- Very large conversations may take time to load.
- The extension does not guarantee that a specific reel or message will be
  identified; it navigates to the relevant date or nearby content.
- It does not replace Instagram's own search, bookmarking, or saving features.

## Project structure

```text
croli-extension-v1.0.4/
├── manifest.json   # Chrome extension configuration
├── popup.html      # Extension popup entry point
├── popup.js        # Popup interface and date-search controls
├── popup.css       # Popup styling
├── content.js      # Instagram conversation detection and auto-scrolling
└── icons/          # Extension icons
```

## Project status

Croli is a personal utility built to solve a specific day-to-day problem:
reaching old self-shared Instagram content without exhausting manual
scrolling. It may evolve as Instagram's Web interface changes and as new
personal-use improvements become useful.
