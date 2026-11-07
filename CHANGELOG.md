# NexaTabs changelog

What changed in each public release of NexaTabs, written for users. NexaTabs supports Chrome and Edge, and both use the same build.

## 1.0.3

**Chrome Web Store:** submitted 7 November 2026, in review.
**Edge Add-ons:** submitted 7 November 2026, in review.

No new permissions.

### New

- **Glass cards in Zen Mode:** Over a wallpaper, workspace cards are frosted glass in a 4-column grid that drops to 3, 2 or 1 column in narrower windows, including with Chrome's vertical tabs. Each card shows the name, then the action buttons, then the tab count and tags.
- **Cards that match your photo:** Over a dark photo the cards turn smoky grey with light text; over a bright photo they stay light with dark text. NexaTabs checks the photo's brightness once, on your device. To choose for yourself, go to Settings, then Dashboard, then **Card style**, and pick Auto, Light or Dark.
- **Click a Zen card to open it:** Click anywhere on a card to open that workspace, or to jump to it if it is already open. With the keyboard, Tab to the workspace name and press Enter.
- **Add current tab from a dashboard card:** Cards have a plus button that adds your most recent tab to that workspace. Its tooltip names the tab and its site.
- **A one-time request for a review:** After a few days of use, the popup asks once whether you would like to rate NexaTabs. Rate NexaTabs opens the store page; Not now ends it. If you ignore it, it stops after three popups and does not come back. Nothing is sent anywhere.

### Improved

- **Workspace order:** In the dashboard and the popup, the workspace you are in comes first, then other open workspaces, then pinned ones, then the rest by most recently used.
- **Wallpaper visibility** is now a slider from "More photo" to "Easier to read", with a live preview. Your earlier setting carries over.
- **Default background:** A new quiet blue and violet gradient, with light and dark versions.
- **Saved workspaces** show a neutral grey ring instead of a coloured one, so a red workspace no longer looks like an error. Open workspaces keep the green dot.
- **Create tile:** The "Create a new workspace" tile is a clear dashed button with readable text.
- **Right-click menu:** The item is now called **Save page to NexaTabs workspace**. The page stays open.
- **Bookmark import (beta):** Folders with more than 100 links are split into several workspaces, such as Folder (1) and Folder (2). Links already in NexaTabs are skipped.
- **Appearance settings:** Long image names are shortened, and Choose image and Remove image are clear buttons.

### Fixed

- **Duplicate workspace names** are now blocked when you create or rename a workspace. Two workspaces with the same name could make Switch or Save and Close act on the wrong one.
- **Esc in Zen Mode** closes the innermost open item first, such as a card menu, rename or a text field, and exits Zen only when nothing is open.
- In Zen Mode, a card's menu no longer opens underneath the next row of cards, and the ⋯ button no longer spills past the card edge at mid widths.
- Zen Mode fills narrow windows instead of shrinking to one column.
- Dashboard search no longer shows duplicate cards while you type quickly.
- Bookmark import no longer drops links after the first 100 in a folder.
- Right-click menu titles and notifications are now translated.

## 1.0.2

**Chrome Web Store:** live from 22 October 2026.
**Edge Add-ons:** live from 29 October 2026.

### New

- **Add current tab to this workspace:** In the popup, use the icon on a workspace row, or choose "Add current tab to this workspace" in the workspace's menu. It works like right-clicking a page and choosing Add to NexaTabs workspace. If that workspace is open in any window, the tab moves into its tab group. Bookmarking stays separate as "Save current tab as bookmark".
- **Duplicate workspace:** The copy keeps the tabs, notes and bookmarks and gets a clear name, such as "Research (copy)" and then "Research (copy 2)". The copy starts closed and unpinned. If the original uses Accounts (same site · multiple logins), the copy keeps the Accounts setting but not the signed-in sessions, so sign in again where a site asks.
- **Export workspace:** Save one workspace as its own JSON file, with its name, colour, tabs, notes, bookmarks and Accounts setting. The file does not contain passwords, cookies or page content.
- **Import workspace:** In Settings, import a single workspace file. It is always added as a new workspace and never overwrites or merges into an existing one. NexaTabs skips invalid URLs, keeps at most 500 tabs, and tells you what it skipped.
- **Load website icons from the internet:** A new setting, on by default. See [PRIVACY.md](PRIVACY.md) for what it does.

### Improved

- **Stash:** Stash now saves only loose tabs (not in a tab group and not pinned) into the selected workspace. It asks before closing them and closes only the tabs it saved. A short message tells you how many were saved and skipped. If the selected workspace is already open, Stash works as Save and Close for it.
- **Switch:** Switch labels now match the selected workspace, and the default selection prefers a workspace that is not already open.
- **Quick switch (Alt+Q):** Alt+Q saves your current workspace and switches to your Quick target. If no Quick target is set, NexaTabs shows a short hint asking you to set one, or to create a workspace if you have none. Alt+Q follows the in-app language, and the dashboard ignores Alt+Q while you type in a text field.
- **Dashboard:** Action tooltips update when you select a card, and an unused bookmark control on cards was removed.
- **Translations:** German, French and Spanish (Latin America) now match the English wording.

### Permissions

- **New permission, favicon:** NexaTabs now reads website icons from the browser's local icon cache first. The permission is read-only. When NexaTabs updates, your browser may ask you to approve it.

### Good to know

- The icon on a workspace row in the popup now adds the current tab to that workspace's tabs, not to its bookmarks.
- Single-workspace export and import are separate from the full backup. Import backup still replaces all NexaTabs data after you confirm.

## 1.0.1

**Chrome Web Store:** live from 21 September 2026.
**Edge Add-ons:** live from 25 September 2026.

- **One workspace per context:** Client work, research, personal browsing and AI tools each get their own named set of tabs, with optional notes and bookmarks that stay with that workspace.
- **Switch from the popup:** Pin the workspaces you use every day, set a Quick target, and stash-and-switch with Alt+Q without hunting through a crowded tab strip.
- **Accounts (same site · multiple logins):** Each login gets its own cookie jar inside its workspace, so you can use more than one account on the same site in one browser. Site support varies.
- **A calmer first run:** Start from Work, Social, AI and Personal templates.

## 1.0.0

First public release, March 2026.

---

NexaTabs is developed and maintained by Nebula Personalization Tech Solutions Pvt. Ltd.
