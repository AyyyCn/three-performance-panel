# Three.js Renderer Inspector

A lightweight performance overlay panel for Three.js. It displays key runtime stats including FPS, frame time, geometry usage, draw calls, and triangle count — helping developers debug and optimize their scenes.

This is a clean, modern rewrite of the classic `THREEx.RendererStats`, refactored as an ES module with updated styling, more relevant metrics, and precise frame timing.

## Features

- Real-time **FPS** display with color-coded feedback
- Accurate **frame time** measurement (ms)
- Counts **geometries**, **textures**, **draw calls**, and **triangles**
- Clean, responsive visual layout
- No dependencies — drop-in module
- Compatible with ES modules and modern Three.js workflows

## Installation

Copy `RendererStats.js` into your project or import it as a module.

```js
import { RendererStats } from './RendererStats.js';

const stats = new RendererStats();
document.body.appendChild(stats.domElement);
```

## Usage

In your animation loop:

```js
function animate() {
  stats.begin();

  // update and render your scene
  scene.update();
  renderer.render(scene, camera);

  stats.end(renderer);
  requestAnimationFrame(animate);
}
```

## Attribution

This project was originally inspired by [`THREEx.RendererStats`](https://github.com/jeromeetienne/threex.rendererstats) by @jeromeetienne and @mrdoob.
