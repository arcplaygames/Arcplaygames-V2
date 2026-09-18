ARC PLAY GAMES — ARC RACER PLAYABLE PROTOTYPE

WHAT WAS ADDED
- Clicking the Arc Racer poster opens a full-screen futuristic racing game.
- 2, 3 or 4 player grid selection.
- Real EVM wallet connection using the browser wallet provider.
- 1 USDC/player entry is displayed in the UI.
- Speed Up and Brake controls.
- Phone tilt steering (with permission where the browser requires it).
- Keyboard steering for desktop testing.
- Futuristic neon track, cars, HUD and finish state.

IMPORTANT FOR PRODUCTION
This is a playable frontend prototype. It does NOT transfer real USDC.
Before enabling real-money races, configure a verified production escrow/
smart contract, exact USDC token address, chain ID, treasury rules, refunds,
anti-cheat, server-authoritative multiplayer and legal/compliance requirements.

MULTIPLAYER
The current HTML simulates the other racers locally so the game is playable
without a server. True 2–4 player racing across different devices needs a
backend/WebSocket or WebRTC matchmaking layer.

GITHUB
Upload only index.html. The Arc Racer poster and the existing site background
video/logo are embedded in the HTML.
