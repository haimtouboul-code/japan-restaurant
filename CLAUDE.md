
# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the app

Open `index.html` directly in a browser — no build step, no server required.

```
start sakura-crm/index.html        # Windows
open sakura-crm/index.html         # macOS
```

## Architecture

Everything lives in a single file (`index.html`) with three self-contained sections:

**Inline `<style>`** — all CSS using CSS custom properties defined on `:root`. Layout is sidebar-fixed + scrollable main content. The sidebar is `position: fixed; right: 0` (RTL). Each UI primitive (card, badge, modal, toast, table map cell) has its own class block.

**HTML body** — five `<div class="page">` sections (dashboard, reservations, menu, kitchen, customers) that are toggled via `display:none/block`. A single `<aside class="sidebar">` holds navigation. Three modal overlays sit at the bottom of `<body>`.

**Inline `<script>`** — no frameworks, no modules. Organized as:

| Section | What it does |
|---|---|
| `DATA` | Plain arrays: `TABLES`, `MENU`, `reservations`, `kitchenOrders`, `customers` — these are the in-memory store |
| `NAVIGATION` | `showPage(name)` swaps `.active` class on pages and nav items |
| `TABLE MAP` | `renderMap(containerId)` renders `TABLES[]` as clickable grid cells |
| `RESERVATIONS` | `renderReservations()` writes three separate `<tbody>` targets; `saveReservation()` / `deleteRes()` / `confirmRes()` mutate the array then re-render |
| `MENU` | `renderMenu(cat)` filters `MENU[]` by category and re-renders the card grid |
| `KITCHEN` | `renderKitchen()` renders four kanban columns; `advanceOrder(id)` moves an order through `new → preparing → ready → served` |
| `CUSTOMERS` | `renderCustomers()` / `selectCustomer(id)` / `saveCustomer()` / `deleteCust(id)` |
| `MODAL` | `openModal(id)` / `closeModal(id)` toggle `.open` class on overlay divs |
| `TOAST` | `toast(msg, icon, type)` appends a toast element and removes it after 3.2 s |

## Key conventions

- **RTL Hebrew UI** — `<html dir="rtl">`, sidebar is on the right, flex/grid layouts flow right-to-left naturally.
- **No persistence** — all data resets on page reload. Mutate the in-memory arrays and call the relevant `render*()` function to update the DOM.
- **Re-render pattern** — every write operation (save/delete/confirm) calls `renderX()` directly; there is no reactive state. Always call `renderX()` after mutating its data array.
- **Sidebar badges** (`badge-res`, `badge-kitch`) are updated inside `renderReservations()` and `renderKitchen()` respectively.
- **Google Fonts** (`Heebo`) is loaded from the network; the app degrades gracefully to system fonts offline.
- **Menu categories**: `all`, `starters`, `sushi`, `ramen`, `main`, `tempura`, `dessert`, `drinks` — used as `data-cat` on tab buttons and as the `cat` field in `MENU[]`.
- **Kitchen status flow**: `new → preparing → ready → served` (one-way, enforced by `STATUS_NEXT` map).
