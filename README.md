# Opening Builder
Static site (no build step). Open `index.html` locally, or deploy:
1. Push this folder to a GitHub repo.
2. vercel.com → Add New Project → import the repo → Framework "Other" → Deploy.
3. Open the site and click **Log in with Lichess** (the login token is stored only in your browser).
Your White and Black trees each autosave to browser storage; use Save/Load for JSON backups (`white-opening-tree.json` / `black-opening-tree.json`; old notebook files load too).

Board UI: [Chessground](https://github.com/lichess-org/chessground) from Lichess (GPL-3.0), brown board and cburnett pieces, loaded from jsDelivr.

## Engine (Build mode)
Evaluations come from Lichess's cloud database, and from a local Stockfish when there is none (or when you click the tick). Download the engine files from the [Stockfish.js releases](https://github.com/nmrugg/stockfish.js/releases) (v19) and put each `.js` with its `.wasm` in an `engine/` folder:
`stockfish-19-lite-single`, `stockfish-19-lite`, `stockfish-19-single`, `stockfish-19` (the last two are about 94MB each; use GitHub Desktop or git for those). `vercel.json` makes the page cross-origin isolated, which the multi-threaded engines need. Delete it if it causes trouble: the single-threaded engines still work.
