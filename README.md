# 🎮 Backlog Shelf

A single-file, dependency-free game tracker with drag & drop shelves.
Everything lives in your browser's `localStorage` — no server, no account, no database.

## Features

- **Four shelves:** Now Playing · Completed · Dropped · Backlog
- **Drag & drop:** move a card to another shelf; its badge updates automatically and the card lands at the bottom of the target shelf. On touch devices, press and hold a card for a moment to pick it up, then drag it onto another shelf
- **Favorites:** only *completed* games can be starred, and favorites float to the top of the shelf
- **Quick add:** pick a shelf and add — the shelf sets the badge. A ★ Favorite checkbox appears
  when the shelf is Completed
- **Edit:** click ✎ (or double-click a card) to change its title and note; Enter saves, Esc cancels
- Per-card delete
- Item counts next to each shelf heading

- **Profiles:** several people can share the same browser — create, switch, rename and delete profiles from the header. Each profile keeps its own four shelves, and a new profile starts empty

## Usage

Open `index.html` in a browser — that's it. No install, no build step.

## Data

Everything is stored locally: the profile list lives under `backlogShelf_profiles`, and each
profile's games under `backlogShelf_v1:<profile name>`. Which means:

- Shelves are **per browser / per device** and are never shared with anyone. Two people using
  their own phones each get their own storage — profiles are for sharing one browser, not for
  syncing between devices.
- The first visit creates a profile named `Me`, seeded with an example list; delete those cards
  and add your own, or rename the profile. Profiles created afterwards start empty.
- Clearing browser data clears every profile.

To start from scratch, run this in the browser console:

```js
Object.keys(localStorage)
  .filter(k => k.startsWith('backlogShelf'))
  .forEach(k => localStorage.removeItem(k));
location.reload();
```

## Deploying

It is a static page, so any static host works. On [Vercel](https://vercel.com), import the
repository and deploy with the default settings — no framework, no build command and no
output directory needed.
