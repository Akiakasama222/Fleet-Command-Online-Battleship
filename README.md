# Fleet Command – Online Battleship

A static, two-player Battleship game. Players connect directly browser-to-browser
with WebRTC (via PeerJS), so there is no backend to run or pay for.

## Run locally
Open `index.html` in a browser (or `npx serve .`). Open it in two tabs to test.

## Deploy
1. Create a GitHub repo and push these files (`index.html`, `README.md`).
2. In Vercel: **Add New → Project → import the repo**. Framework preset: *Other*. No build command, no output directory.
3. Deploy. Share the URL; one player clicks **Create game**, the other joins with the 5-letter code or the copied link.

## How to play
Place 5 ships (Carrier 5, Battleship 4, Cruiser 3, Submarine 3, Destroyer 2), press **Ready**, then take turns firing. First to sink the whole enemy fleet wins.

## Notes
- Uses PeerJS's free public signaling server. For heavy use, self-host a PeerJS server or switch to Ably/Pusher/Supabase Realtime.
- Each browser keeps its own ship positions and only reveals hit/miss, but a determined player could inspect their own JS. Moving rules to a server is the next step if you need anti-cheat.
