# nfl-slate-bundles

Published week bundles for BTB Gridiron. Public on purpose: the app reads them
over plain HTTPS with no credential, which is what lets a data refresh reach a
running instance without a redeploy.

`manifest.json` names the current week and the hash of its bundle. The app polls
it and hot-swaps; readers are never disconnected by a refresh.

Each `week_<season>_<week>.rds` is a single R object holding that week's
projection, schedule, team context and accuracy table. Nothing here is a
secret and nothing here is an outcome claim.
