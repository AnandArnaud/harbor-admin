# harbor-admin

Harbor Admin is a tiny internal admin panel — sign in, manage products, sign out.

**Stack:** Plain HTML / CSS / JS (no build step)

It is realistic but intentionally small, and 
## Key user actions

sign in · create product · delete product · sign out

## Running it

```bash
# static site — no build
python3 -m http.server 8000   # then open http://localhost:8000
```

## Session replay

FullStory is loaded in `index.html` (session replay, rage clicks, funnels). `app.js` identifies the admin by email on sign-in, sends `signed_in`, `product_created`, `product_deleted`, `signed_out`, and anonymises on sign-out; the email field is excluded (`fs-exclude`) and the products table masked (`fs-mask`). The org id is set at the top of `app.js`.
