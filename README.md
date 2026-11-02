# Canary Kebab & Snack Bar website

The website for **Canary Kebab & Snack Bar**: kebabs, pizza and Indian food in Costa Teguise, Lanzarote. Hosted on GitHub Pages.

It's a plain static site: six self-contained HTML pages (all CSS and JS inline), bilingual English/Spanish, with no build step.

| Page | Content |
|---|---|
| `index.html` | Video hero, favourites, gallery, reviews, WhatsApp ordering, blog, both shops with maps |
| `menu.html` | Full menu (71 dishes, 112 drinks) with filters and "Add to order" |
| `about.html` · `blog.html` · `contact.html` · `reels.html` | Story, 5 articles, contact details, promo videos |

Preview locally: `python3 -m http.server 8000`, then open http://localhost:8000

## Editing notes
- The nav, footer, styles and order script are copied into **every page**, so change all six files.
- Text comes in pairs: `<span data-lang="en">…</span><span data-lang="es">…</span>`.
- **WhatsApp order number:** currently +34 695 07 17 65 (temporary, shared with Hippie Chippy). To change it everywhere:
  `sed -i 's/34695071765/34NEWNUMBER/g; s/+34 695 07 17 65/+34 NEW NUMBER/g' *.html`
- Menu prices appear on `menu.html`, in the `MENU_ITEMS` order list on every page, in the favourites on `index.html` and in some blog articles.
