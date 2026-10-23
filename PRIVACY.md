# NexaTabs permissions and privacy

This page explains, in plain words, what each NexaTabs permission is used for and how NexaTabs loads website icons. It applies to NexaTabs 1.0.2 on Chrome and Edge. For the full legal text, read the [NexaTabs Privacy Policy](https://www.nexatabs.com/privacy-policy).

## Where your data lives

- Your workspaces, saved tabs, notes, workspace bookmarks and settings are stored locally in your browser's extension storage (`chrome.storage.local`).
- No NexaTabs account is needed for the core features, and there is no NexaTabs cloud sync.
- Backups are files you create yourself. Export backup saves all workspaces and settings as a JSON file, and Export workspace saves one workspace as its own JSON file. These files are plain JSON and are not encrypted, so anyone who has the file can read it. Check your notes before you share a file.
- Local storage is not disk encryption. Use your operating system's encryption if you need stronger protection at rest.
- Websites you open in your tabs still run their own scripts and make their own network requests, and follow their own privacy practices. NexaTabs does not change that.
- Uninstalling NexaTabs removes its local storage from your browser.

## Permissions

NexaTabs uses Manifest V3. These are the permissions listed in the 1.0.2 manifest and what each one is for.

| Permission | What NexaTabs uses it for |
|---|---|
| `tabs` | Read the open tabs (address and title) so NexaTabs can save them into a workspace, reopen them when you switch, and close them when you choose Save and Close or Stash. |
| `tabGroups` | Put each open workspace into a browser tab group, name and collapse it, and ungroup it when you ask. |
| `windows` | Find the right browser window when you switch, save or restore a workspace, so tabs open in a normal window and not in the NexaTabs dashboard window. |
| `storage` | Save your workspaces, notes, bookmarks and settings locally in your browser. |
| `bookmarks` | Read your browser bookmarks when you choose to import them with the Import Wizard. |
| `contextMenus` | Add the right-click menu items, such as adding the current page to a workspace or saving a link as a workspace bookmark. |
| `notifications` | Show a short confirmation after you add a tab to a workspace from the right-click menu, or tell you the tab is already there. |
| `declarativeNetRequest` | Accounts (same site · multiple logins): attach the right sign-in cookies to each Accounts tab so different logins on the same site stay apart. |
| `webRequest` | Accounts (same site · multiple logins): see the cookies a site sets in an Accounts tab so they can be kept with that login. |
| `favicon` (new in 1.0.2) | Read website icons from the browser's own local icon cache, so saved tabs show the right icon. This permission is read-only. |

### Site access (host permissions)

NexaTabs asks for access to `http` and `https` pages. This is needed because:

- Accounts (same site · multiple logins) has to work on the sites where you use it, and keeps each login's cookies and site storage separate.
- In Accounts workspaces, NexaTabs adds the workspace name to the tab title so similar account tabs are easy to tell apart.
- With the icon setting on, NexaTabs may load a missing website icon from that website (see below).

## What the install prompt means

When you install or update NexaTabs, your browser lists what the extension can do. The wording comes from the browser, not from NexaTabs, and it is written for the widest possible use of each permission. The exact lines can differ between Chrome and Edge and between browser versions. This is what each line means for NexaTabs.

| What the browser shows | Manifest permission | Why NexaTabs needs it |
|---|---|---|
| Read your browsing history | `tabs` | NexaTabs reads the address and title of your open tabs so it can save them into a workspace and reopen them later. It does not use the browser's History API (`history` is not in the manifest), and it does not read your past browsing history. |
| Block content on any page | `declarativeNetRequest` | Used only for Accounts (same site · multiple logins). NexaTabs sets short-lived session rules that attach the right sign-in cookies to each Accounts tab. It is not used to block ads or page content. |
| Read and change your favorites (Edge) or bookmarks (Chrome) | `bookmarks` | Used when you choose to import browser bookmarks with the Import Wizard. NexaTabs reads your bookmark tree for that import. Workspace Bookmarks are a separate list stored inside NexaTabs, not in your browser bookmarks. |
| View and manage your tab groups | `tabGroups` | Each open workspace is shown as a named browser tab group, which NexaTabs creates, renames, collapses and ungroups for you. |
| Read the icons of the websites you visit (may be shown on Chrome) | `favicon` | Reads website icons from the browser's local icon cache. Read-only. |
| Display notifications | `notifications` | Short confirmations, such as when you add a tab to a workspace from the right-click menu. |
| On all sites, or Read and change all your data on all websites | host permissions for all http and https sites, used with `webRequest` | Accounts (same site · multiple logins) has to work on whichever site you use it on: NexaTabs reads the cookies a site sets in an Accounts tab and keeps each login's cookies and site storage separate. NexaTabs scripts on pages also add the workspace name to tab titles in Accounts workspaces. With the icon setting on, a missing icon may be loaded from the website. |

`storage`, `contextMenus` and `windows` do not usually show a line in the install prompt. They are explained in the table above.

These explanations come from the NexaTabs developer, Nebula Personalization Tech Solutions Pvt. Ltd. They describe how the current version uses each permission. The browser cannot check that for you, so if you need more assurance, you can review the permissions on the extension's details page in your browser and remove any extension you do not trust.

## Website icons

NexaTabs shows website icons next to saved tabs so you can recognise them at a glance. It handles icons in this order:

1. It reads the icon from the browser's local icon cache first, or uses an icon it already saved.
2. If the icon is missing and **Load website icons from the internet** is on (the default), NexaTabs may load it from the website itself or from Google's favicon service. Google's favicon service receives the website's hostname. Icon requests are sent without your cookies. Your workspace data, notes and settings are not sent with these requests.
3. If you turn **Load website icons from the internet** off, NexaTabs makes no network requests for icons. It uses only the browser's local icon cache and icons it already saved, does not store new remote icons, and shows a simple fallback icon when none is available.

To change it, open Settings in the NexaTabs popup or dashboard and find **Load website icons from the internet**. Turning it off does not change your tabs, notes, bookmarks or settings; only how icons are shown. With the setting off, some tabs may show a generic icon when the browser has no cached icon for that site.

This setting covers icons inside NexaTabs only. It does not make the websites you visit private.

## Practical notes

- **Keep backups private.** Backup and workspace files are plain, unencrypted JSON. They can contain sensitive addresses, such as links to internal tools, documents or account pages, and anything in your notes. Store them somewhere private and share them only on purpose.
- **Export before you uninstall.** Uninstalling NexaTabs removes its local data from your browser. Export a backup first if you want to keep your workspaces.
- **Backups do not carry logins.** A backup or exported workspace does not include passwords, cookies or signed-in sessions. After you import, sign in again where a site asks, including in Accounts workspaces.

## Optional wallpapers

Zen Mode can show an optional wallpaper on the dashboard. As the Privacy Policy explains, if you choose a remote wallpaper, the image is loaded from Unsplash. The default gradient wallpaper needs no download.

## Questions

See the [NexaTabs Privacy Policy](https://www.nexatabs.com/privacy-policy), the [privacy Answers on nexatabs.com](https://www.nexatabs.com/answers/privacy-%26-security/is-nexatabs-private-data-security), or email support@nebulatech.in.

NexaTabs is developed and maintained by Nebula Personalization Tech Solutions Pvt. Ltd.
