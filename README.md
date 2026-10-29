# Inferno Wave Solver

A dependency-free, single-file browser tool for planning OSRS Inferno waves
1–68. It includes wave rosters, the playable arena, pillars, and the nine
documented spawn locations. Choose the current wave and overhead prayer, then
select each monster and tap its top-left map tile to match the live encounter.
The map highlights tiles no unprotected monster can currently attack from its
position. Your setup is saved in local storage.

The board solver is a static estimate, not a client plugin or tick simulator.
It does not model pathing, attack timing, the blob's changing attack cycle,
Jad attack cues/healers, pillar damage, or Zuk wave 69; Jad spawn locations are
starting estimates. Line of sight uses a tile-based Bresenham approximation;
compare its output with the game before relying on it.
Monster sizes, wave composition, spawn locations, and arena coordinates are
based on the OSRS Wiki and the [Inferno reference data and its source list](https://github.com/davidsaad-git/triple-jad-sim/blob/main/docs/INFERNO_DATA.md).

## Host it on GitHub Pages from your phone

1. Merge the solver change into `main`.
2. In your phone's browser (not the GitHub app), open
   <https://github.com/danbudworthmead/Inferno-daily/settings/pages>. Sign in
   if asked; request the desktop site from the browser menu if the page needs it.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Choose the `main` branch and `/(root)`, then tap **Save**.
5. Return to the Pages settings page after a minute or two and open the
   published site URL shown there.

To update the game from your phone later, edit `index.html` from the repository's
**Code** tab and commit the change to `main`; Pages will publish it automatically.