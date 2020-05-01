# StraitsIT product documentation

Static files generated by `next export` (via `npm run deploy` command)

## Build locally and develop

This is essentially nextjs's standard development workflow.

```bash
npm run dev
open localhost:3000
```

## Build local static files and serve

This executes a `next build` and `next export`, and copies the generated static files to the root directory and to the `straitsit.github.io` directory.

We then use `serve` to serve our static files locally, so we can manually verify that our static files are correctly generated and can expect it to work fine when we actually deploy it

```bash
npm run deploy
npm start # we have modified `start` to use `serve`, a static file server
open localhost:5000
```

## Deploying to github pages

```bash
npm run deploy

# git commit and push to master branch
git add .
git commit -m "Update documentation"
git push
open straitsit.github.io 
```