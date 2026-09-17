# Arc Play Games V2

## What changed
- Your supplied MP4 is now the primary visual background.
- Two synchronized video layers are used: a full-screen blurred layer and an uncropped original layer. This keeps the whole portrait video visible while still filling the entire page.
- Added a clear **Tap to enable cinematic audio** control. Mobile browsers normally block autoplay with sound, so sound cannot be forced on reliably without a user gesture.
- Uses your Arc Play Games logo in the navigation.
- Premium purple/cyan GameFi styling, larger readable text and a more cinematic layout.
- X Follow links go directly to https://x.com/ArcPlayGames.
- Wallet connect uses an injected EVM wallet and requests Arc mainnet.
- X username submission + optional wallet field.
- `admin.html` shows locally saved submissions and exports CSV.
- `google-apps-script.gs` can send submissions to your Google Sheet.

## IMPORTANT FOR YOUR LIVE DOMAIN
Upload the **entire package**, not only `index.html`.

Your hosting must have:
- `/index.html`
- `/assets/arc-play-bg.mp4`
- `/assets/arc-play-logo.jpg`

If `assets/arc-play-bg.mp4` is missing from the live server, the background video will not appear.

## Audio
Browsers such as Chrome on Android generally block autoplaying audio before a user gesture. The website therefore starts the video muted and lets the visitor tap **Tap to enable cinematic audio**. After that, the video plays with sound.

## Google Sheet
1. Create a Google Sheet.
2. Extensions → Apps Script.
3. Paste `google-apps-script.gs`.
4. Deploy as Web app; execute as you and allow access to anyone.
5. Copy the `/exec` URL.
6. In `index.html`, change:
   `const CONFIG={submissionEndpoint:""};`
   to:
   `const CONFIG={submissionEndpoint:"YOUR_EXEC_URL"};`
7. Redeploy the website.

## Wallet
The package uses Arc mainnet configuration:
- Chain ID: 5042 (`0x13b2`)
- RPC: `https://rpc.mainnet.arc.io`
- Explorer: `https://explorer.arc.io`

Always test wallet behavior before production use. Never ask users for seed phrases/private keys.
