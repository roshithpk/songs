# Ayyappa Devotional Music Player — GitHub Pages edition

This version runs entirely on GitHub Pages. It has no Python backend and needs no server setup. It includes the Spotify-inspired player, a full-resolution Ayyappa poster, five rotating devotional backgrounds, search, play/pause, previous/next, shuffle, repeat, seek and volume controls.

## Publish on GitHub Pages

1. Create a GitHub repository, for example `ayyappa-devotional-player`.
2. Upload the **contents of this folder** to the repository root: `index.html`, `playlist.json`, `backgrounds/`, and `songs/`.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then click **Save**.
6. Wait a few minutes. GitHub will show the published website URL in Settings → Pages.

## Add songs

GitHub Pages cannot scan a folder dynamically. To add a song:

1. Upload the audio file into `songs/`.
2. Edit `playlist.json` and add an entry for that file. Example:

```json
[
  {
    "title": "Harivarasanam",
    "artist": "Ayyappa devotional song",
    "file": "songs/Harivarasanam.mp3"
  },
  {
    "title": "Pallikettu",
    "artist": "Ayyappa devotional song",
    "file": "songs/Pallikettu.mp3"
  }
]
```

Keep valid JSON: use double quotes, separate entries with commas, and do not leave a comma after the final entry. The `file` path must match the uploaded filename, including capitalization. Commit both changes to GitHub; Pages will publish them automatically after a short delay.

## Important audio note

GitHub repositories are not designed as large-scale audio streaming storage. Keep the repository small and only upload recordings you have permission to distribute. For a large library, host audio files in a suitable storage/CDN service and use their direct audio URLs in `playlist.json`.
