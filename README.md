# 🎮 Backlog Shelf

A single-file, dependency-free game tracker with drag & drop shelves.
Everything lives in your browser's `localStorage` — no server, no account, no database.

## Features

- **Four shelves:** Now Playing · Completed · Dropped · Backlog
- **Drag & drop:** move a card to another shelf; its badge updates automatically and the card lands at the bottom of the target shelf
- **Favorites:** only *completed* games can be starred, and favorites float to the top of the shelf
- **Quick add** form and per-card delete
- Item counts next to each shelf heading

## Usage

Open `index.html` in a browser — that's it. No install, no build step.

## Data

Everything is stored locally under the `backlogShelf_v1` key, which means:

- Your shelf is **per browser / per device** and is never shared with anyone.
- The first visit seeds an example list; delete those cards and add your own.
- Clearing browser data clears the shelf.

To start from scratch, run this in the browser console:

```js
localStorage.removeItem('backlogShelf_v1'); location.reload();
```

## Deploying

It is a static page, so any static host works. On [Vercel](https://vercel.com), import the
repository and deploy with the default settings — no framework, no build command and no
output directory needed.
