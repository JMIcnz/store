# build command
`pnpm exec opennextjs-cloudflare build`  
output:
```
.open-next/worker.js
.open-next/assets
```

# deploy command
`pnpm exec wrangler deploy`  
use `wrangler.jsonc` as args which define:
```
"main": ".open-next/worker.js",

"assets": {
    "directory": ".open-next/assets",
    "binding": "ASSETS"
},
```
