# Cyberrunner

A cybersecurity-themed endless runner built with [Phaser](https://phaser.io/) and Vite. Dodge malware, phishing, and ransomware. Grab keys and MFA tokens to stay alive.

Originally built as a side project on my [portfolio site](https://github.com/SammyCode002), extracted here as a standalone repo.

## Run locally

```bash
npm install
npm run dev
```

Then open the URL Vite prints (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
npm run preview
```

The static bundle lands in `dist/` and can be deployed to any static host (Vercel, Netlify, GitHub Pages, etc.).

## Controls

- **Space / Up / Tap** - jump
- **Down** - slide / fast-fall
- **Enter** - start / restart

## Project layout

```
src/
  main.js              Phaser game config + entry
  scenes/
    BootScene.js       generates pixel-art textures at runtime
    GameScene.js       gameplay, spawn loop, scoring
    GameOverScene.js   leaderboard + name entry
  util/
    audio.js           tiny WebAudio sound helpers
    leaderboard.js     localStorage-backed top-10 scores
index.html             host page + global styles
vite.config.js
```

No images or audio files ship with the repo. Every sprite is drawn with `Phaser.Graphics` in `BootScene.js`, and all sound effects are generated on the fly with WebAudio in `util/audio.js`.

## License

MIT
