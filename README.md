# FunctionSpace3D
OmniGraph3D is an interactive web-based mathematical visualization tool that allows users to input equations and instantly render them in a 3D coordinate space. It supports explicit, parametric, and implicit functions including curves, surfaces, and geometric shapes such as spheres and ellipses.

## 🚀 Features
- Surface plotting: `z = f(x, y)`
- Curve plotting: `y = f(x)` and `x = f(y)`
- Implicit surface (e.g., `x^2 + y^2 + z^2 = 4`)
- Special shapes (helix, torus-approx)
- Animate time-dependent formulas (`t` variable)
- Wireframe / solid toggle
- Interactive orbit with drag/scroll and touch
- Range controls for x/y/z limits

## 📁 Repository structure
- `index.html`: single-page app (React + Three.js + mathjs via CDN)
- `vercel.json`: static hosting config for Vercel

## ▶️ Run locally
1. Open `index.html` directly in a browser (works with modern browsers).
2. Or run a local server (recommended):
   - `python3 -m http.server 8000`
   - Visit `http://localhost:8000`

## ☁️ Deploy on Vercel
1. Add `vercel.json` (already included):
   - builds `index.html` via `@vercel/static`
   - routes all URLs to `index.html`
2. In Vercel project settings:
   - Framework Preset: `Other` / `Static`
   - Build Command: empty
   - Output Directory: (empty)
3. Deploy and verify `curl -L https://<your-app>.vercel.app | head -n 10` starts with `<!doctype html>`.

## 🧪 Using the app
1. Type equation in the input box.
2. Click `Plot`.
3. Adjust `x/y/z` ranges for zoom/detailed region.
4. Toggle `Wireframe` and `Animate`.
5. Use preset buttons to jump to common examples.
6. Drag in canvas to orbit view (mouse/touch); scroll to zoom.

## 🛠️ Notes
- If source appears as raw text, ensure Vercel serves `index.html` as static HTML, not a direct JS dump.
- Confirm `vercel.json` and clear Vercel cache on redeploy.

