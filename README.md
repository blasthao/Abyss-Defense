# Abyss Defense: Total Deadlock

A lightweight, high-intensity, zero-dependency HTML5 Canvas arcade shooter. Command an escalating array of heavy twin-barrel defense turrets, repel relentless mutant swarms, trigger tactical strikes, and hold the defensive perimeter at all costs.

---

## Key Features

* **Zero Dependencies:** Built entirely with vanilla HTML5, Canvas 2D API, Web Audio API, and modern JavaScript in a single, portable file.
* **Twin-Barrel Defense Battery:** Scale your battery from a single core turret up to a devastating 10-unit frontline array with progressive bullet upgrades (Piercing, Frag Splinter, Plasma Fusion).
* **Dynamic Wave & Outbreak Engine:**
* Controlled early-game progression (Waves 1–19).
* Massive, dense swarm outbreaks starting at **Wave 20** (recurring every 5 waves).
* Adaptive Rubber-Band pressure system that dynamically paces spawn intervals to keep combat engaging without unfair spikes.


* **Tactical Enemy Mechanics:**
* **Runners:** Sprinting targets that initiate high-speed charges when breaking the perimeter.
* **Shield Brutes:** Heavy units that absorb frontal kinetic fire; break shields via flanking crossfire to inflict a 3-second 2× vulnerability window before armor regenerates.
* **Abyss Tyrants (Bosses):** Multi-phase titans firing mutagenic spores. Concentrated fire builds an **Overheat gauge**, triggering a 2.5-second stunned vulnerability window with 2× damage.


* **Tactical Command Skills:**
* ✈️ **Strategic Airstrike (300K):** Screen-clearing carpet bombing that eradicates all active threats immediately.
* ⚙️ **5-Barrel Gatling Emplacement (200K):** Deploys a stationary heavy fire support turret along center choke points.
* ❄️ **Cryo Stasis (100K):** Freezes all targets on screen for 8 seconds.
* 💣 **High-Explosive Mines (100K):** Heavy area denial that shatters incoming waves.
* 🕸️ **Tether Traps (50K):** Pins enemy clusters and increases damage taken by 25%.


* **Tactical Supply Airdrops:**
* Floating supply pods spawn on the outer flanks (`Common`, `Rare`, `Elite`).
* Forcing positional trade-offs: moving to the flank accelerates crate capture but leaves the center lane exposed.


* **Dynamic Bounties & Clutch Kills:**
* Timed mini-missions reward skill charges and score bonuses without penalizing failure.
* Last-second kills inside critical defensive range (`z < 0.15`) trigger score multipliers (**CLUTCH KILL**).


* **Local & Geolocation Leaderboard:**
* Persistent high-score rankings stored locally.
* Built-in IP-based geo-detection displays the operator's combat sector.



---

## Controls

| Action | Control (Desktop) | Control (Mobile / Touch) |
| --- | --- | --- |
| **Move Battery / Aim** | Mouse movement (horizontal) | Touch and drag horizontally |
| **Fire Primary Battery** | Automatic continuous fire | Automatic continuous fire |
| **Activate Skills** | Click dock buttons on left | Tap dock buttons on left |
| **Pause Game** | Click `⏸️ Pause` button on right | Tap `⏸️ Pause` button on right |
| **Toggle Audio** | Click `🔊 Sound` button on right | Tap `🔊 Sound` button on right |

---

## Quick Start & Deployment

No installation, build tools, or package managers required.

### 1. Run Locally

Clone the repository and open `index.html` directly in any modern web browser:

```bash
git clone https://github.com/your-username/abyss-defense.git
cd abyss-defense
# Open index.html directly, or serve with any static server:
npx serve .

```

### 2. Deploy to GitHub Pages

1. Push the code to your GitHub repository.
2. Go to **Settings** > **Pages**.
3. Under **Build and deployment** > **Branch**, select `main` (or your default branch) and `/ (root)`.
4. Click **Save**. Your game will be live at `https://<your-username>.github.io/<repo-name>/`.

### 3. Deploy to Cloudflare Pages / Vercel

* **Cloudflare Pages:** Connect your GitHub repo or drag-and-drop the directory directly under **Workers & Pages** > **Create Application** > **Pages**.
* **Vercel:** Import the project as a static site with no build command required.

---

## Architecture

```text
├── index.html       # Self-contained game client (HTML structure, CSS UI, Canvas engine, SFX)
└── README.md        # Documentation

```

* **Rendering:** Pure Canvas 2D projection simulating pseudo-3D depth perspective.
* **Audio:** Native Web Audio API procedural synthesis (synthesizes gunfire, explosions, sirens, and hits without external `.mp3`/`.wav` assets).
* **Persistence:** `localStorage` for cross-session high scores and callsign retention.

---

## License

Distributed under the [MIT License](https://www.google.com/search?q=LICENSE). Free for personal and commercial modification.
