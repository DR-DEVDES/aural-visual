# AUIL VISUAL

**AURAL ILLUSION — 3D Audio Visualizer**

A browser-based, real-time 3D audio visualizer built with HTML, CSS, JavaScript and Three.js.

## Features

- Eight visual modes: Tunnel, Terrain, Galaxy, Orb, Laser, City, Warp and Knot
- Real-time audio frequency analysis using the Web Audio API
- Animated 3D graphics with bloom and RGB-shift post-processing
- Randomized visual styles and color palettes
- Track title overlays and live clock
- Playback controls, seeking and fullscreen mode
- Mouse-controlled camera movement
- Responsive, single-page interface

## Quick start

1. Download or clone this repository.
2. Add your music file to the `audio/` folder.
3. Rename it to `audio.mp3`, or change `AUDIO_SRC` in `index.html`.
4. Open the project through a local web server.

> **Important:** Browsers may restrict audio playback and Web Audio features when opening
> files directly with `file://`. Use a local server instead.

### Run locally

If Python is installed, open a terminal in the project folder and run:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Configure the visualizer

Open `index.html` and find the settings block near the beginning of the script:

```js
const AUDIO_SRC = "audio.mp3";
const TITLE = "";
const LOOP = true;
const TEXTS = [
  ["AURAL ILLUSION", "MIX"],
  ["DARK", "ELECTRONIC"],
  ["MINIMAL", "MICRO HOUSE"],
  ["UNDERGROUND", "MUSIC NETWORK"],
  ["AURAL", "ILLUSION"]
];
const TEXT_TRACK = true;
```

- `AUDIO_SRC`: path or URL of the audio file.
- `TITLE`: optional fixed track title. Leave empty to use the filename.
- `LOOP`: enable or disable looping.
- `TEXTS`: rotating visualizer title cards.
- `TEXT_TRACK`: add the audio filename to the title rotation.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `Space` | Play / pause |
| `←` / `→` | Seek backward / forward by 5 seconds |
| `R` | Randomize visual style |
| `1`–`8` | Select a visual mode |
| `T` | Show / hide title text |
| `X` | Change title text |
| `C` | Show / hide clock |
| `F` | Toggle fullscreen |

## Visual modes

1. Tunnel
2. Terrain
3. Galaxy
4. Orb
5. Laser
6. City
7. Warp
8. Knot

## Deployment with GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder.
5. Save. GitHub Pages will publish the project.

Add your own `audio.mp3` to the `audio/` folder and update `AUDIO_SRC`
to `audio/audio.mp3` if you keep the file there.

### Audio hosting note

GitHub Pages is suitable for hosting the visualizer website, but large audio files
may make the repository unnecessarily heavy. Consider hosting your audio separately
and setting `AUDIO_SRC` to a publicly accessible direct audio URL. Check the hosting
provider's bandwidth, hotlinking and licensing terms.

## Dependencies

The page loads these libraries from public CDNs:

- [Three.js r128](https://threejs.org/)
- [Google Fonts](https://fonts.google.com/)
- [cdnjs](https://cdnjs.com/)
- [jsDelivr](https://www.jsdelivr.com/)

An internet connection is required for these external resources unless you vendor
the dependencies locally.

## Project structure

```text
auil-visual/
├── index.html
├── README.md
├── LICENSE
├── .gitignore
├── .nojekyll
├── audio/
│   └── README.md
├── assets/
│   └── README.md
└── .github/
    └── FUNDING.yml
```

## License

Released under the MIT License. See [LICENSE](LICENSE).

The visualizer source is provided as-is. You are responsible for ensuring that
any audio, fonts, images or other media you add are properly licensed.
