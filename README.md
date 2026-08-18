# A Deep Dive Into Vector Field Pathfinding

An interactive blog post explaining **Vector Field Pathfinding**, an alternative to A* / Dijkstra for moving many agents toward a goal. The post mixes written explanations, LaTeX math, and live p5.js visualizations you can play with directly in the browser (Dijkstra heatmaps, Eikonal spreading, vector field construction, agent motion, and more).

Live site: https://nnnawi.github.io/A-Deep-Dive-Into-Vectorfield-Pathfinding/

## Stack

- [Astro](https://astro.build) — static site framework
- MDX (`@astrojs/mdx`) — Markdown + JSX for t√he blog content
- [p5.js](https://p5js.org) — canvas-based interactive visualizations
- `remark-math` / `rehype-mathjax` — LaTeX equation rendering
- `mathjs` — math utilities used in some of the sketches
- Prettier — code formatting

## Project Structure

```
src/
├── common/          # Shared math/graphics helpers (solver, vector field, p5 utils...)
├── components/       # One .astro component per interactive visualization
│   └── BlogContent.mdx   # The actual blog post content
├── layouts/
│   └── Layout.astro  # Base page layout, fonts, global styles
└── pages/
    └── index.astro    # Entry point, renders BlogContent
```

## Development

```bash
npm install       # install dependencies
npm run dev       # start dev server at http://localhost:4321
npm run build     # build static site to dist/
npm run preview   # preview the production build
```

For details on how the visualizations are built and how to add new ones, see [README-astro.md](README-astro.md).
