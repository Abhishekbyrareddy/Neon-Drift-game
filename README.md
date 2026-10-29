# Neon Drift

A tiny browser arcade game for a quick break: steer your ship, dodge pink meteors, collect golden stars, and chase your best score.

The entire game is one self-contained `index.html` file (about 9.5 KB), well under 2 MB. There are no dependencies, external assets, downloads during play, or build steps.

## Get the game

With Git installed, run:

```sh
git clone https://github.com/Abhishekbyrareddy/Neon-Drift-game.git
cd Neon-Drift-game
```

Alternatively, choose **Code → Download ZIP** on GitHub, then extract the ZIP.

## Play locally without a server

1. Open the downloaded or cloned folder.
2. Double-click **index.html** to open it in a modern browser such as Chrome, Edge, Firefox, or Safari.
3. Click **Start drifting** and play.

This works offline. No installation, account, or internet connection is needed after downloading the game.

## Host locally with Python

Use this method if you prefer playing through a local web address or serving the game during development.

1. Install Python 3 if it is not already available.
2. Open a terminal in the folder containing `index.html`.
3. Start the server:

   **Windows:**

   ```powershell
   py -m http.server 8000 --bind 127.0.0.1
   ```

   If `py` is unavailable but `python` is installed, use:

   ```powershell
   python -m http.server 8000 --bind 127.0.0.1
   ```

   **macOS / Linux:**

   ```sh
   python3 -m http.server 8000 --bind 127.0.0.1
   ```

4. Leave the terminal running and open **http://127.0.0.1:8000** in your browser.
5. Click **Start drifting**.
6. Press **Ctrl+C** in the terminal to stop hosting.

The server is bound to your own computer. If port 8000 is busy, replace `8000` with `8080` in both the command and browser address. If you see a directory listing instead of the game, stop the server and run it from the folder that contains `index.html`.

## How to play

| Action | Control |
| --- | --- |
| Steer left / right | Left / Right arrow keys or A / D |
| Steer with touch or mouse | Press and drag inside the play area |
| Pause / resume | P, Escape, or the Pause / Resume button |
| Start / restart | Start drifting / Play again button |
| Start, pause, or resume using the keyboard | Space |

- Avoid the **pink meteors**. Each hit costs one of your three lives, followed by a short period of invulnerability.
- Collect **golden stars** for **50 points** each.
- Earn **10 points per second** while playing.
- Meteors become faster and more frequent as you survive.
- The game ends when all three lives are lost. Choose **Play again** to restart.
- Switching away from the game automatically pauses it.

Your best score is saved in your browser's local storage at the end of a run when storage is available. Scores are specific to that browser and address, so opening the file directly and playing through localhost may show different records. Private browsing or blocked storage can prevent scores from persisting; the game still works.

## Host on a static web server

Serve `index.html` from your web server's document root. No backend, package installation, environment variables, or compilation is required. The same file works on static hosting services.

## Project files

```text
Neon-Drift-game/
├── index.html   # Complete game: HTML, styles, and JavaScript
└── README.md    # Setup, hosting, and gameplay instructions
```

Built with HTML, CSS, JavaScript, and the Canvas 2D API.
