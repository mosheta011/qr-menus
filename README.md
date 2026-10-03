# QR Menus

Six ready-to-use digital QR menu designs for restaurants, plus a showcase page for clients.

**Live showcase:** https://mosheta011.github.io/qr-menus/

| Style | Venue type | Live page |
|---|---|---|
| Mavi Fincan | Café · specialty coffee · brunch | [/mavi/](https://mosheta011.github.io/qr-menus/mavi/) |
| Bademli | Bakery · patisserie | [/bademli/](https://mosheta011.github.io/qr-menus/bademli/) |
| KOR | Burger · fast food | [/kor/](https://mosheta011.github.io/qr-menus/kor/) |
| Usta Dönerci | Döner · kebab | [/usta/](https://mosheta011.github.io/qr-menus/usta/) |
| Hanedan | Fine dining restaurant | [/hanedan/](https://mosheta011.github.io/qr-menus/hanedan/) |
| Balkaymak | Breakfast house · kahvaltı | [/balkaymak/](https://mosheta011.github.io/qr-menus/balkaymak/) |

Every menu includes Turkish / English / Arabic (right-to-left), categories, search and diet filters,
item options and add-ons, allergens and calories, open/closed status, Wi-Fi and info, a cart,
WhatsApp ordering and a call-waiter button.

## Making a menu for a client

1. Copy one style folder, e.g. `kor/` → `client-name/`.
2. Open `client-name/index.html` and search for `window.MENU`. Edit:
   - `whatsapp:"905000000000"` – the client's WhatsApp number (country code, no `+` or spaces)
   - `restaurant` – name, tagline, address, phone, Wi-Fi, Instagram, `hours` (7 entries, Sunday first; `null` = closed)
   - `banner` – optional cover at the top (delete it to hide)
   - `categories` / `items` – names and descriptions in `tr` / `en` / `ar`, `price`, `tags`, `allergens`, `options`, `soldOut:true`, `img:"photo.jpg"`
3. Change the brand name in `<h1 class="brand-name">` and the colours in the `:root` block at the top of `<style>`.
4. Commit and push. The menu is live at `https://mosheta011.github.io/qr-menus/client-name/`.
   Make the QR code from that address; it never needs reprinting when prices change.

Business names, addresses and phone numbers in the samples are fictional.
