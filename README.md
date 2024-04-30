## Issue

https://github.com/cloudflare/workers-sdk/issues/5729

## Steps to reproduce

- Clone https://github.com/Cherry/wrangler-custom-builds-hang-repro
- npm ci
- npm run dev
- Observe requests to `http://127.0.0.1:8787` working fine
- Make multiple changes to `src/index.ts`. Add a console.log, etc. but ensure the file is written to at least twice
- Observe requests are now just hanging

---

-  `npx wrangler@3.53.0 dev` - hangs with above steps
-  `npx wrangler@3.19.0 dev` - hangs with above steps
-  `npx wrangler@3.18.0 dev` - works without issue

