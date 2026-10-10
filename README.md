# QR Menus

Seven ready-to-use digital QR menu designs for restaurants and cafés, plus a showcase page for clients.

**Live showcase:** https://mosheta011.github.io/qr-menus/

| Style | Venue type | Live page |
|---|---|---|
| Mavi Fincan | Café · specialty coffee · brunch | [/mavi/](https://mosheta011.github.io/qr-menus/mavi/) |
| Bademli | Bakery · patisserie | [/bademli/](https://mosheta011.github.io/qr-menus/bademli/) |
| KOR | Burger · fast food | [/kor/](https://mosheta011.github.io/qr-menus/kor/) |
| Usta Dönerci | Döner · kebab | [/usta/](https://mosheta011.github.io/qr-menus/usta/) |
| Hanedan | Fine dining restaurant | [/hanedan/](https://mosheta011.github.io/qr-menus/hanedan/) |
| Balkaymak | Breakfast house · kahvaltı | [/balkaymak/](https://mosheta011.github.io/qr-menus/balkaymak/) |
| **Maison Noor** (premium) | Luxury café · patisserie · afternoon-tea salon | [/noor/](https://mosheta011.github.io/qr-menus/noor/) |

Every menu includes Turkish / English / Arabic (right-to-left), categories, search and diet filters,
item options and add-ons, allergens and calories, open/closed status, Wi-Fi and info, a cart,
WhatsApp ordering and a call-waiter button. Orders are always written in the house language (Turkish by
default, set `orderLang` in `window.MENU` to change it) so staff can read them whatever language the guest used.

**Maison Noor** adds night and day themes, a menu that follows service hours (brunch, high tea), a currency
converter, favourites, allergen-exclusion filters, table booking (WhatsApp + calendar file), tip choice,
a daily pick, and works offline / installs to the home screen. In `noor/index.html`, update `rates:{…}`
(sample exchange rates) before using it for a real client.

**Table QR codes:** add `?table=12` to a menu address (e.g. `…/kor/?table=12`) and the table number is
pre-filled in the order and waiter call. Hours use the venue's time zone (`restaurant.tz`, default `Europe/Istanbul`),
not the guest's phone clock. For demos, Noor also accepts `?time=14:30` to preview a service window.

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
