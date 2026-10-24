# Opening Builder
Static site (no build step). Open `index.html` locally, or deploy:
1. Push this folder to a GitHub repo.
2. vercel.com → Add New Project → import the repo → Framework "Other" → Deploy.
3. Open the site and click **Log in with Lichess** (the login token is stored only in your browser).
Your White and Black trees each autosave to browser storage; use Save/Load for JSON backups (`white-opening-tree.json` / `black-opening-tree.json`; old notebook files load too).

Board UI: [Chessground](https://github.com/lichess-org/chessground) from Lichess (GPL-3.0), brown board and cburnett pieces, loaded from jsDelivr.
