# CF build command
`pnpm exec opennextjs-cloudflare build`  
output:
```
.open-next/worker.js
.open-next/assets
```

# CF deploy command
`pnpm exec wrangler deploy`  
use `wrangler.jsonc` as args which define:
```
"main": ".open-next/worker.js",

"assets": {
    "directory": ".open-next/assets",
    "binding": "ASSETS"
},
```

# Var for both build time and run time in CF
* NEXT_PUBLIC_DEFAULT_REGION         // nz, which has been set in medusa admin
* NEXT_PUBLIC_BASE_URL               // this store public url
* NEXT_PUBLIC_MEDUSA_BACKEND_URL     // medusa backend url without trailing slash
* NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY // get from medusa admin
