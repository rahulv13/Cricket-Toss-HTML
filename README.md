# Cricket Toss (Standalone Single-File Edition)

A completely self-contained, single-file release of the **Cricket Toss** 3D arcade browser game.

Everything needed to run the entire game—HTML markup, CSS styling, Three.js 3D graphics, Cannon-es physics simulation, procedural turf & pitch textures, procedural Web Audio sound synthesis, gameplay logic, scoring, wind mechanics, and moving obstacles—is bundled into **one single file**: `index.html`.

---

## 📦 What This Version Contains

- **`index.html` (644 KB)**: The complete, standalone game.
- **Zero Local Asset Dependencies**: Requires no image files, audio files, 3D model files, or separate `.js`/`.css` stylesheets.
- **Zero External CDN Dependencies**: Three.js and Cannon-es are bundled directly inside the file; it does not load anything from external servers.
- **Zero `node_modules` Required**: Runs immediately without installing npm packages or running build steps.

---

## 🚀 How to Run the Game

### Method 1: Using Any Local HTTP Server (Recommended)

Because modern web browsers have strict WebGL and security policies for local files, running through a local lightweight web server gives the best performance and compatibility across all browsers:

#### Option A: Python (Built into macOS / Linux / Windows)
```bash
# Navigate to the folder containing index.html
cd Cricket-Toss-HTML

# Start a local web server on port 8000
python3 -m http.server 8000
```
Then open your browser and visit: **`http://localhost:8000`**

#### Option B: Node.js (npx serve or http-server)
```bash
cd Cricket-Toss-HTML
npx serve .
```
Or:
```bash
npx http-server .
```

#### Option C: VS Code Live Server Extension
Right-click on `index.html` in VS Code and select **"Open with Live Server"**.

---

### Method 2: Direct File Opening (`file://`)

In modern browsers that permit WebGL on local file origins (such as Chrome with default flags, Safari, Edge, and Firefox), you can also double-click `index.html` or open it directly via:
```
file:///path/to/Cricket-Toss-HTML/index.html
```

---

### Method 3: Deploy to Free Web Hosting (Vercel, Netlify, GitHub Pages)

Because this repository consists of a single `index.html`, you can deploy it instantly:
- **GitHub Pages**: Go to your repository settings > Pages > select branch `main` > Save.
- **Vercel / Netlify**: Drag-and-drop the `Cricket-Toss-HTML` folder onto your dashboard or connect this repository.

---

## 🎮 Game Controls & Gameplay

| Control | Desktop | Mobile / Touch |
| :--- | :--- | :--- |
| **Aim Direction** | Move cursor horizontally / vertically across the pitch | Drag finger horizontally / vertically across the pitch |
| **Charge Power** | Click and drag down to charge throw power (55% to 145%) | Touch and drag down to charge throw power |
| **Throw Ball** | Release left mouse button | Lift finger from screen |
| **Reset Attempt** | Press `R` on keyboard | Handled automatically after ball settles |

### Features Included:
- **3D Cricket Stadium**: Outdoor pitch, realistic creases, 3D seating bowl, boundary rope, advertising ribbon, and concourse jumbotron scoreboard.
- **Realistic Cannon-es Physics**: Individual rigid bodies for 3 stumps and 2 bails with realistic wood collision audio synthesis and impact spark particles.
- **Scoring System**: 10 pts for 1 stump, 25 pts for 2 stumps, 50 pts for all 3 stumps, plus 20 bonus points for completing a round. Persistent high scores saved to `localStorage`.
- **Wind Mechanics**: Directional horizontal breeze (Calm, Light, Moderate, Strong) that deflects the airborne ball and dynamically curves the trajectory preview.
- **Moving Obstacles (Round 3+)**: Patrolling wooden hazard barrier across the pitch with real-time predictive collision detection and deflection physics.
- **Mobile Responsive Design**: Dynamic camera framing adapted for both widescreen desktops and tall mobile smartphone screens (iPhone & Android).

---

## 🛠️ Original Development Repository

The modular source code (with separate ES modules, Vite configuration, and development tools) is preserved in the main repository:
- **Original Project**: [https://github.com/rahulv13/Cricket-Toss](https://github.com/rahulv13/Cricket-Toss)
