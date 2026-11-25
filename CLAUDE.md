# rexplained-media

Public staging area for studio videos on their way to Metricool. Not a source repo: the studio code lives in
`dcknowles04/Appeal-Agent`, folder `studio/` (see `studio/CLAUDE.md`, "Publishing an episode").

- Video and images are stored with **Git LFS** (`.gitattributes`), so 4K masters go up uncompressed by size limits.
- Metricool needs a public URL. Use the LFS media URL, not raw.githubusercontent.com (that serves the small LFS
  pointer text, not the video):
  `https://media.githubusercontent.com/media/dcknowles04/rexplained-media/main/<path>`
- Layout: `<channel>/epNN/` (e.g. `rexplained/ep03/`): episode master, Shorts, thumbnail.
- Metricool copies each file when the post is created. After every post for an episode is created and shows a
  static.metricool.com media URL, the episode's files can be removed from `main` with a normal commit.
  **That does not free LFS storage**: LFS objects stay billed until the repository is deleted. When the LFS storage
  quota runs low, delete and recreate this repository (empty), re-add the files of any not-yet-created posts, then
  carry on. Check usage under GitHub Settings -> Billing -> Git LFS.
- Never put anything private here: the repository is public.
