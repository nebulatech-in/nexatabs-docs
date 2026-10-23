# NexaTabs changelog

What changed in each public release of NexaTabs, written for users. NexaTabs supports Chrome and Edge, and both use the same build.

## 1.0.2

**Chrome Web Store:** live from 22 October 2026.
**Edge Add-ons:** still on 1.0.1 for now.

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
