In this project the `src/App.vue` is [registered as a dependency](https://github.com/bradlc/vite-vue-bug/blob/main/postcss.config.js#L16-L21) in a PostCSS plugin. The plugin reads the CSS from the multi-line comment in `src/App.vue` and appends it to the CSS root. Editing `src/App.vue` should trigger a rebuild and update the CSS but it does not.

### Reproduction Steps

1. `npm install`
2. `npm run dev`
3. Edit the CSS comment in `src/App.vue` and notice that the styles do not update
