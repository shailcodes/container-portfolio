# Container Yard — Portfolio

An interactive 3D portfolio built as a container yard. Cargo containers drop in with
physics, and a crane picks one up, opens its doors, and reveals the content inside.



---

## What it is

A single self-contained `index.html` — no build step, no dependencies to install.
Everything (3D, physics, UI, content) lives in one file.

- **7 sections** as shipping containers: What I Do, Portfolio, Say Hello, The Work, About, Process, Toolkit
- **Real-ish physics** — containers fall, stack, collide (cannon-es)
- **Crane choreography** — trolley slides, claw grips, lifts, straightens, drops
- **Content opens inside the container** — doors swing open and HTML content scales to fit the face
- **Responsive** — layout recalculates camera and scale on resize; works on phones
- **Nav-linked** — header links fly the crane to the matching container

---

## Tech

| Layer | What |
|---|---|
| 3D | [three.js](https://threejs.org/) `0.160.0` (CDN, import map) |
| Physics | [cannon-es](https://github.com/pmndrs/cannon-es) `0.20.0` (CDN) |
| Fonts | Archivo, Instrument Serif, JetBrains Mono (Google Fonts) |
| Textures | Generated at runtime on `<canvas>` — no image assets |
| Build | None. Plain ES modules in the browser. |

---

## Edit your content

Open `index.html` and find the **`EDIT ME`** block near the top of the `<script type="module">`:

```js
const CONFIG = {
  name:  'Shailendra',
  role:  'Designer & creative developer',
  city:  'Mumbai, IN',
  email: 'hello@yourdomain.com',
  year:  '2026',
  services: [ ... ],
  projects: [ { n:'01', t:'Project One', d:'Brand + website · 2026' }, ... ],
  timeline: [ ... ],
  process:  [ ... ],
  tools:    [ ... ],
};

## Credits
- Design and code: [@shailcodes]
