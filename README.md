# InviSent

![InviSent logo](./whatsapp-link-generator.svg)

**InviSent** is a browser-based tool for preparing personalized WhatsApp Web links from a contact list. It builds a pre-filled message for each contact and opens the matching WhatsApp Web chat so you can review and send it yourself.

## Project layout

```text
.
├── index.html                    # Single-page app: markup, styles, and JavaScript
├── whatsapp-link-generator.svg   # Shared logo, favicon, and Open Graph image
└── README.md                     # Project documentation
```

## Features

- Paste contact names and WhatsApp numbers as comma-separated values or one entry per line.
- Automatically add India's `+91` country code to 10-digit numbers; accept country-coded numbers too.
- Validate missing names, malformed numbers, and duplicate phone numbers.
- Personalize the first-line `Dear ...` or `Hi ...` greeting with `{{name}}`.
- Generate a WhatsApp Web link with the contact's pre-filled message.
- Search, select, and review generated contacts before opening chats.
- Copy an individual WhatsApp Web link or personalized message.
- Optionally preview a local image in the browser; the image is not uploaded.
- Save names, numbers, and the message template in the browser's local storage.
- Use the responsive, neumorphic interface on desktop and mobile.

## Interface layout

1. **Contact Input** — paste matching name and number lists.
2. **Message Template** — edit the invitation and use `{{name}}` to insert each contact's name.
3. **Optional Image** — preview an image locally.
4. **Contact List** — search, select, and open valid contacts in WhatsApp Web.
5. **Personalized Preview** — inspect the selected contact's message, then open WhatsApp or copy its link/message.
6. **Dashboard statistics** — see total, valid, selected, and invalid contact counts.

## Run locally

Open `index.html` in a modern browser, or serve the folder with a local static web server. No build step or package installation is required. Tailwind utility classes are loaded from the Tailwind CDN, so those utilities require an internet connection; the app's own CSS provides its primary layout and theme.

## Data and privacy

The app runs in the browser. Contact lists and the message template are saved in that browser's local storage for convenience. Uploaded images are only previewed locally and are not uploaded. Opening a WhatsApp link navigates to WhatsApp Web with the message pre-filled; the user must review and send it manually.

## Branding and sharing

`whatsapp-link-generator.svg` is used in the app header and as the SVG favicon. `og-image.jpg` is used for Open Graph and Twitter social previews. The page metadata points to the live site at <https://invisent.kryzo.space/>. Social crawlers can display the preview only when the site and image are publicly accessible.