
# 🏰 Collatz Castle 3D – Teleport Adventure

> An immersive 3D exploration of the Collatz Conjecture, built from a classic text adventure and enhanced with modern graphics and AI assistance.

## 🎮 About the Game

This project started as a text‑based game written in p5.js, where you navigated the Collatz conjecture by typing door numbers. Now, it has been transformed into a full 3D experience using Three.js. Explore rooms connected by mathematical rules, click on glowing doors to teleport between numbers, and follow the fastest route to Room 1. A radial 3D tree map shows the branching structure of the conjecture, and a celebration awaits when you reach the final room.

## ✨ Features

- **3D Exploration** – Freely rotate, pan, and zoom around a central octagonal pedestal.
- **Collatz Mechanics** – Each number has 2 or 3 doors (neighbors) based on the classic rules:
  - Always: `n × 2`
  - If even: `n ÷ 2`
  - If odd: `3n + 1`
  - Even numbers sometimes have an extra door: `(n − 1) ÷ 3` if divisible.
- **Path Visualization** – Toggle “Show Collatz Path” to highlight the golden doors that follow the shortest route to 1.
- **3D Tree Map** – Enable the tree to see a radial diagram of all forward connections from your current room, with spheres for numbers and thick glowing cylinders for links.
- **Bilingual Instructions** – Help overlay available in both English and Chinese.
- **Celebration** – Reaching Room 1 triggers a confetti‑free celebration modal.

## 🖥️ Running the Game

### Offline

1. **Download Three.js**  
   Place the following files in a `lib/` folder next to your `index.html`:
   - `three.module.js` from `https://unpkg.com/three@0.128.0/build/three.module.js`
   - The entire `jsm/` folder from `https://unpkg.com/three@0.128.0/examples/jsm/`

2. **Update the import map** in the HTML to point to these local files:
   ```html
   <script type="importmap">
       {
           "imports": {
               "three": "./lib/three.module.js",
               "three/addons/": "./lib/jsm/"
           }
       }
   </script>
   ```

3. **Start a local web server** (do **not** just double‑click the HTML file – browser security blocks ES modules).  
   - **Option A:** If you have Python, run `python -m http.server 8000` in the folder, then open `http://localhost:8000`.  
   - **Option B:** Use VS Code’s **Live Server** extension (right‑click the HTML → “Open with Live Server”).  
   - **Option C:** Use Node.js: `npx serve .`  
   - **Option D:** Use a portable static server like Mongoose.

### Online (CDN)

If you have internet, you can simply open the original HTML (which uses unpkg CDN) in any modern browser – no local server needed.

## 🛠️ How to Play

1. **Goal:** Reach **Room 1**.
2. **Controls:** Drag the mouse to rotate the camera, right‑click to pan, and **click on any colored door cube** to teleport to that room.
3. **Strategy:**  
   - If the current number is **even**, choose the door to `n ÷ 2`.  
   - If the current number is **odd**, choose the door to `3n + 1`.  
   This is the classic Collatz path and always reaches 1 in the fewest steps.
4. **Hints:**  
   - Enable “Show Collatz Path” to see golden doors that follow this strategy.  
   - Enable “Show 3D Tree Map” to see all possible connections from your current room.  
   - The HUD shows your current room and the number of steps left to 1.

## 📜 Credits

- **Original Text Adventure** – Written in p5.js before the era of AI coding.
- **3D Upgrade & Enhancements** – Brought to life with **Three.js** and **CSS2DRenderer**.
- **AI Assistance** – Code generation, debugging, and feature integration with the help of **coding LLMs** (Claude, ChatGPT, etc.) to transform the original concept into a modern interactive experience.

## 📁 File Structure

```
collatz-castle-3d/
├── index.html          # Main game file (the full code)
├── lib/
│   ├── three.module.js
│   └── jsm/            # Three.js add‑ons (controls, renderers, etc.)
└── README.md           # This file
```

## 📄 License

Feel free to use, modify, and share this project for educational and non‑commercial purposes. Attribution to the original concept and AI assistance is appreciated.

---

Happy exploring, and may you always reach 1! 🎉
```
