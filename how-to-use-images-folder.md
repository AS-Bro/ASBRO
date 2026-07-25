# How to Use the `images` Folder

The page (`as-bro-hub.html`) was already set up to load its logos and pictures from
a local `images` folder instead of the internet. This package now includes that
folder, pre-filled with placeholder art so everything works immediately.

## 1. Keep the folder structure together

Unzip `as-bro-hub-site.zip` — you'll get:

```
as-bro-hub.html
images/
├── branding/
│   ├── logo.png
│   └── favicon.png
├── socials/
│   ├── youtube.png
│   ├── telegram.png
│   ├── discord.png
│   └── instagram.png
├── about/
│   ├── avatar.png
│   ├── milestone-subscribers.png
│   ├── milestone-views.png
│   └── milestone-members.png
├── servers/
│   └── indraneelam-smp-icon.png
└── files/
    ├── survival-world-icon.png
    └── survival-world-banner.png
```

**The `images` folder must always sit in the same folder as `as-bro-hub.html`.**
The page looks for `images/branding/logo.png`, not just `logo.png` — if you move
the html file without the folder, the pictures will disappear.

## 2. To replace a picture, just overwrite the file

You don't need to touch any code. To swap in your own logo, avatar, server icon,
etc., replace the matching file **using the exact same filename**:

| Replace this file | To change |
|---|---|
| `images/branding/logo.png` | Header logo (top-left, next to your name) |
| `images/branding/favicon.png` | Browser tab icon |
| `images/socials/youtube.png` | YouTube icon in the social row |
| `images/socials/telegram.png` | Telegram icon |
| `images/socials/discord.png` | Discord icon |
| `images/socials/instagram.png` | Instagram icon |
| `images/about/avatar.png` | Your profile photo on the About page |
| `images/about/milestone-subscribers.png` | Icon on the "Subscribers" stat card |
| `images/about/milestone-views.png` | Icon on the "Views" stat card |
| `images/about/milestone-members.png` | Icon on the "Members" stat card |
| `images/servers/indraneelam-smp-icon.png` | Server icon on the Servers page |
| `images/files/survival-world-icon.png` | Small tag icon on a file card |
| `images/files/survival-world-banner.png` | Big banner image on a file card |

Just drag your new image in, rename it to match exactly (same name, same
`.png` ending), and overwrite the old one. Refresh the page in your browser —
no code editing required.

## 3. Adding a brand-new server or file card

If you add a new entry to `serversList` or `filesList` in `config.js` (see the
main editing guide), give its image a new filename and drop it in the matching
subfolder — e.g. a second server's icon could be `images/servers/my-second-server-icon.png`.
Then point that entry's `serverLogo` (or `fileIcon` / `image`) field at
`"images/servers/my-second-server-icon.png"` to match.

## 4. Image size tips

Match these dimensions (or the same aspect ratio) so nothing looks stretched:

| File | Recommended size |
|---|---|
| `branding/logo.png` | 128×128 |
| `branding/favicon.png` | 32×32 |
| `socials/*.png` | 64×64 |
| `about/avatar.png` | 400×400 |
| `about/milestone-*.png` | 32×32 |
| `servers/*-icon.png` | 96×96 |
| `files/*-icon.png` | 48×48 |
| `files/*-banner.png` | 600×350 |

## 5. Formats

PNG is recommended (what's already there). JPG works too — if you use `.jpg`,
just make sure the filename in `config.js` ends in `.jpg` to match, since the
filename has to match exactly what the code is looking for.
