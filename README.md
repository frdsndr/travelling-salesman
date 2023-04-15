# Travelling Salesman

A Svelte, SvelteKit and Threlte (Three.js) demo project.

URL: https://travelling-salesman.punctuation.pictures/

## Todos

- [ ] Optimize performance for older iPhones (6/7) and Androids.
    - Instancing of geometry? Lightbaking?
- [X] ~~Fix directional lighting shadows [Issue](https://github.com/threlte/threlte/issues/201)~~
    - ~~issue related to frustrum size / shadow-camera / scene-size~~

## Setup project

```bash
# run dev server
make dev

# build production version
make build
```

> Make sure the correct [adapter](https://kit.svelte.dev/docs/adapters) is set up! (Netlify/Vercel/etc)
