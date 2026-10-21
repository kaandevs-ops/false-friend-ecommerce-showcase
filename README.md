# False Friend — Cinematic E-Commerce Showcase

**A complete streetwear storefront concept, from scroll-driven storytelling to server-verified checkout.**

Designed and developed by **Kaan Tekin**. This repository presents the main False Friend project through real desktop/mobile screenshots, accelerated walkthroughs and implementation documentation.

[**Türkçe anlatım**](README.tr.md) · [**Desktop walkthrough · 2×**](assets/videos/desktop-walkthrough-2x.mp4) · [**Mobile walkthrough · 2×**](assets/videos/mobile-walkthrough-2x.mp4) · [**Discuss a project**](mailto:kaantekin06@icloud.com)

![False Friend cinematic storefront](assets/screenshots/01-acilis-masaustu.png)

> **Showcase repository:** application source code, database dumps, credentials and deployment packages are kept outside this repository. Payments and refunds in the demonstrated application use a simulation adapter. This is a portfolio concept rather than a live merchandise shop.

## The project

False Friend explores how an editorial fashion experience can connect to practical commerce. The visual direction uses restrained typography, a dark product stage, oversized headlines, material studies and a consistent collection language. The backend provides the product, account, cart, order and operations behavior behind that interface.

The intended use is to demonstrate my work to prospective clients. The experience can be adapted to a client's brand and catalog, or used as a starting point for a separately scoped custom website. The main version shown here preserves its cinematic opening and AI-created concept product imagery. Template Edition is a separate presentation and is not included in this repository.

## Visual experience

- Scroll-driven opening video with staged Identity, Material, Form and Object reveals.
- Chapter controls, scroll progress and a direct link to the featured product.
- Dynamic hero product name, price and availability sourced from the catalog.
- Editorial collection blocks, material/construction studies and campaign layouts.
- Full-screen navigation with category previews, search, saved items and currency controls.
- Lookbook, manifesto, service, privacy and terms surfaces with a shared visual system.
- Loading transitions, image fallbacks and support for reduced motion.
- Hero poster fallback if the video cannot load; video seeking pauses when off-screen.

The opening motion was created with Gemini. Product visuals are AI-created concept assets; the screenshots and walkthroughs show the actual running website.

![Scroll-driven material scene](assets/screenshots/02-kaydirma-sahnesi.png)

## Products and catalog

The demo catalog contains **eight products across four categories**: tops, outerwear, bottoms and accessories.

| Capability | Behavior |
| --- | --- |
| Collection browser | Category filters, catalog search, price/name sorting and editorial/compact density controls |
| Product details | Product description, composition, fit notes, price and availability |
| Variant selection | Size/color combinations, variant-specific prices and stock limits |
| Product media | Gallery navigation, thumbnails, pointer inspection and keyboard-accessible full-screen viewing |
| Quick interactions | Quick view/add controls and saved products |
| Product guidance | Size architecture, available sizes, category guidance and service access |
| Live catalog changes | Added products can load from the backend after a frontend build |
| Product documents | Initial titles, social images, canonical URLs and structured product metadata use live backend data |
| Missing items | Genuine missing-product status and recovery links; API outages are handled separately |

Physical garment measurements are not provided in the concept catalog. Product materials, availability and delivery copy are demo content to be replaced for a real merchant.

![Product and variant selection](assets/screenshots/03-urun-detayi.png)
![Collection browser](assets/screenshots/10-koleksiyon.png)

## Cart, wishlist and pricing

Guests can keep a local bag and wishlist. Signing in synchronizes the selection with the account. The interface supports quantity changes, removal, saved items, coupon application and shipping-threshold feedback.

The server calculates authenticated cart prices and validates current product variants and stock. Restored guest selections are checked against the live catalog; stored client prices are not trusted as checkout prices. Late responses from an old login session cannot replace the active user's state. A failed partial account synchronization can be retried explicitly.

Currency display supports EUR, USD and GBP. USD/GBP use fixed illustrative conversion rates; **checkout settlement remains in EUR**.

![Real server cart with quantity and coupon](assets/screenshots/06-sepet-ve-kupon.png)

