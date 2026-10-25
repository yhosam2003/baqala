# Baqala Orders

A one-page order menu for neighbourhood baqalas. The customer opens the shop's link, picks products, adds their building and flat, and taps **Place order on WhatsApp**. WhatsApp opens with the order written out for the shop, and the customer taps Send.

## Links

- A shop's menu: `https://yhosam2003.github.io/baqala/#al-noor` (each shop has its own link name)
- Shop manager: `https://yhosam2003.github.io/baqala/#admin`

## Set up once

You need two repositories on your GitHub account:

- `baqala` (**Public**): this website. Turn on Settings → Pages → Deploy from a branch → `main`.
- `baqala-private` (**Private**, tick "Add a README file"): the list of shop owners, their phone numbers, fees and notes. The shop manager refuses to save owners to a public repository.

On each phone you use, open the shop manager and connect GitHub:

1. Create a fine-grained token at https://github.com/settings/personal-access-tokens/new
2. Repository access: **Only select repositories**, then pick both repositories.
3. Permissions: **Contents → Read and write**.
4. Paste the token in the shop manager and tap **Connect**.

## Sign up a shop on the spot

1. Open the shop manager and tap **Sign up a shop**.
2. Fill in:
   - **Shop:** name, WhatsApp number for orders, buildings it delivers to, minimum order.
   - **Owner:** name, phone, area.
   - **Deal:** free trial, paying or stopped; setup fee paid; monthly fee; notes.
3. Tap **Save shop**. Then:
   - **Send the owner their link** opens WhatsApp to the owner with a welcome message, the link, and how to save it as a quick reply.
   - **QR code for the counter** makes an image the owner can print.
   - **Open menu** shows the shop's menu. It works on your phone straight away and for everyone else about a minute later.

The shop list shows every shop with its owner, phone, status and fees. You can search it, call or WhatsApp an owner, and download it as a CSV for Excel or Google Sheets. Setting a shop to **Stopped** hides its menu from customers until you change it back.

Under **Products and prices** you can untick what a shop doesn't sell and change any price for that shop only.

## Files

- `index.html`: the whole page (design, products, ordering, shop manager). The product list is `CATALOG` near the top of the second script.
- `shops.json`: what each shop's menu needs. The shop manager edits it for you. It holds no owner details.
- `img/`: one product photo per product, named after the product's id in `CATALOG` (for example `img/milk-alain-1l.webp`). A product without a photo shows a card with its brand name instead.
- `registry.json`, in the private repository: owners, phones, status, fees and notes.

Product photos and default prices come from Talabat listings, plus a few Carrefour UAE prices, in October 2026. Each shop confirms the final price on WhatsApp. QR codes use QR Code Generator by Kazuhiko Arase (MIT license).
