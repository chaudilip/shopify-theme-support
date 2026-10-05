# Setting up Scullery

A step-by-step guide to getting your store looking right after installing
Scullery **2.0.0**. No coding involved: everything here happens in **Online
Store → Themes → Customize** (the theme editor) or elsewhere in Shopify admin.

Scullery treats a shop as a *pantry index*. Every product, recipe and basket
line is an **entry** on a ruled sheet, and the sheet is bound to a **spine**,
a fixed cobalt rail that replaces the usual header. The words the theme uses
for things: **Index** (menu), **Look up** (search), **Basket** (cart),
**Particulars** (product details), **Companions** (related products) and
**Colophon** (footer).

Product details such as tasting notes, origin, ingredients, nutrition and
allergens come from Shopify **metafields**. They stay invisible until you add
data, and the companion guide **Custom data: tasting notes, particulars,
nutrition and recipes** explains how.

## Contents

1. [Getting started](#1-getting-started)
2. [The spine, the folio and the drawers](#2-the-spine-the-folio-and-the-drawers)
   - [Menus](#menus)
   - [Look up (search)](#look-up-search)
   - [The trail](#the-trail)
   - [Back to top button](#back-to-top-button)
3. [Notice bar](#3-notice-bar)
4. [Logo, brand name, favicon and social sharing image](#4-logo-brand-name-favicon-and-social-sharing-image)
5. [Color schemes](#5-color-schemes)
6. [Typography](#6-typography)
7. [Layout, product entries and motion](#7-layout-product-entries-and-motion)
8. [Home page sections](#8-home-page-sections)
9. [Story, contact and other pages](#9-story-contact-and-other-pages)
10. [Collections and Look up results](#10-collections-and-look-up-results)
11. [Product page](#11-product-page)
    - [Image zoom](#image-zoom)
    - [Pre-order](#pre-order)
12. [Recipes and field notes](#12-recipes-and-field-notes)
13. [Basket: drawer or page](#13-basket-drawer-or-page)
    - [Gift wrapping](#gift-wrapping)
14. [Colophon, newsletter and promo pop-up](#14-colophon-newsletter-and-promo-pop-up)
    - [Newsletter popup](#newsletter-popup)
15. [Performance and accessibility](#15-performance-and-accessibility)
16. [FAQ and troubleshooting](#16-faq-and-troubleshooting)

---

## 1. Getting started

1. In Shopify admin, open **Online Store → Themes**, find Scullery in your
   theme library and click **Customize**. Every change previews live and
   nothing goes public until you click **Save** and then publish the theme.
2. A fresh install is a clean starting point, not a copy of the demo shop.
   The home page arrives with its sections in place and sample wording, but
   no products, collections, photographs or films are chosen. Each empty
   picker shows a placeholder drawing until you fill it.
3. Work roughly in this order: logo and menus, color schemes and type
   (they affect every page), the home page, then the product page.
4. Point **Theme settings → Product entries → Recipes blog** at the blog
   that holds your recipes, if you have one. Several sections read it.

The demo store you may have seen belongs to **Larder**, a fictional kitchen
used to show the theme. Its products, wording and photographs are demo
content and do not install with the theme.

## 2. The spine, the folio and the drawers

Scullery has no header bar. The **Spine and folio** section (inside the
header group) draws three things:

- **The spine**: a fixed rail along the left edge on screens 990px and wider,
  lettered with your brand like the spine of a book. On phones and tablets it
  lies along the bottom edge as a bar. It carries three tabs: **Index**,
  **Look up** and **Basket** (with the item count).
- **The drawers**: each tab pulls a panel out from behind the spine: from the
  left on desktop, from the bottom on a phone. Escape or the close button
  shuts it, and focus returns to the tab that opened it.
- **The folio**: a slim running line at the top of the page with the trail
  (where you are), your top-level menu links and the account link. It
  scrolls away on the way down and comes back on the way up; the spine stays.

Settings in **Spine and folio**:

| Setting | What it does |
|---|---|
| Spine color scheme | Defaults to the cobalt scheme. |
| Spine logo | Optional light version of your logo for the cobalt rail. Empty: the main logo is used, or your shop name in the display typeface. |
| Logo on the spine | Turned to run up the spine, or upright. |
| Menu | The folio shows its top-level links; the whole menu, sub-items included, is the Index drawer. Default `main-menu`. |
| Show the menu's links in the folio | Wide screens only. Phones always use the Index drawer. |
| Home page line | A line shown in the folio on the home page and at the foot of the Index drawer. |
| Show account link / Account menu handle | The account link, and the menu Shopify shows inside the account sheet. |
| Index color scheme | Colors of the Index drawer. |
| Default photograph | Shown beside the index on wide screens. Collections, products and articles in the menu show their own photograph when pointed at. |
| Show country and language selector / Show social links | Inside the Index drawer. The selector appears only when you sell in more than one country or language. |

With JavaScript off, the tabs fall back to plain links (the search and cart
pages) and the Index opens with every row already open.

### Menus

1. Go to **Online Store → Navigation** and edit your **Main menu**. Nest
   items by dragging one onto another; the Index drawer shows sub-items as
   rows that open in place.
2. Create a **Footer** menu for the Colophon's link columns.
3. Optionally create a short "browse" menu for the Look up drawer and the
   404 page (see below).

### Look up (search)

**Theme settings → Look up**:

- **Look up opens as**: a drawer from the spine (suggests products as the
  shopper types) or the search page. Without JavaScript it always uses the
  search page.
- **Browse menu**: shown in the drawer before anything is typed.
- **Products in the drawer** / **Number of products**: a small shelf of
  products shown before anything is typed. Empty uses all products.
- **Show quick look-ups**: suggested searches.

Recipes from your recipes blog appear in results alongside products.

### The trail

The folio's first item is the trail: the path to the current page
(for example *Pantry / Oil / Olive oil*). It replaces the breadcrumbs of 1.x
and needs no setting.

### Back to top button

A small square button appears in the bottom-right corner once a visitor is
about two screens down. It rises above chat widgets, the spam-protection
badge and the product page's add bar when they share the corner, sits above
the bottom bar on phones, and moves keyboard focus to the top of the page.
It has no setting and never appears without JavaScript.

## 3. Notice bar

The **Notice** section sits in the header group above the folio. Add one
**Notice** block per message. Each has an icon, a short accent **Tag**
("New", "50% off"), the text, and an optional link and link label.

| Setting | What it does |
|---|---|
| Style | One notice at a time, or a ticker (a moving line). |
| Ticker loop length | Longer is slower. |
| Turn over notices automatically / Time on each notice | For the one-at-a-time style. |
| Label | Set before the notice number, e.g. "Batch note 01". |

### The pause button

Whenever notices move on their own (ticker, or automatic turning) a pause
button is shown, and they stand still for visitors whose device asks for
reduced motion.

## 4. Logo, brand name, favicon and social sharing image

**Theme settings → Branding**:

- **Brand name**: used in page titles, the footer and the spine. Blank uses
  the store name from **Settings → Store details**.
- **Logo** and **Logo width**: the logo appears in the folio on phones and on
  the spine (unless a separate spine logo is chosen in **Spine and folio**).
  A rotated spine logo is held to 44px thick.
- **Favicon** (scaled to 32 × 32) and **Home screen icon (iOS)**: a square
  image of at least 180 × 180 with a solid background.
- **Social sharing image**: used when a page has no image of its own.

## 5. Color schemes

**Theme settings → Colors.** Every section has a **Color scheme** setting
and picks one of the schemes; edit a scheme to restyle every section that
uses it. Each scheme has six roles:

| Role | Used for |
|---|---|
| Paper | The ground |
| Second paper | Behind photographs, panels and open drawers |
| Ink | Text and strong rules |
| Soft ink | Captions, labels and secondary text |
| Accent | Catalog numbers, active states, the spine, tabs |
| Text on accent | Text and icons on the accent |

Hairlines are ink at low strength and are derived for you.

Scullery ships four schemes:

| Scheme | Paper | Ink | Accent |
|---|---|---|---|
| `scheme-1` Paper | chalk `#F5F3EC` | `#15181D` | cobalt `#1F3BCB` |
| `scheme-2` Bone | `#EBE7DB` | `#15181D` | cobalt `#1F3BCB` |
| `scheme-3` Ink | `#15181D` (dark) | `#F5F3EC` | `#9DB0FF` |
| `scheme-4` Cobalt | cobalt `#1F3BCB` | `#F5F3EC` | `#F5F3EC` |

The accent is the one signal color. Keep it the same across schemes that
share a page, and use a whole scheme (for example Cobalt) when a section
should stand on a colored ground. Two contrast rules, which the editor
repeats: the **Accent** must reach 4.5:1 against **Paper**, and **Text on
accent** must reach 4.5:1 against the **Accent**. Check both with a
contrast tool when you change them.

## 6. Typography

**Theme settings → Typography.** Two families, five roles:

| Setting | Default | Sets |
|---|---|---|
| Display: Font | Besley | Page and section titles, product names, catalogue numbers (italic) and marginal notes |
| Display: Size | 100% | Scales every display size |
| Text and labels: Font | Schibsted Grotesk | Body copy, labels, prices, navigation, ledgers |
| Text and labels: Size | 100% | Scales text sizes |
| Article and page body | Text family | Which family sets long reading text |

Choose a display family **with an italic** (numbers and notes are set in it)
and a text family **with clear numerals** (prices and ledgers). Any font
from Shopify's library works; the theme loads the bold and italic it needs.
Nothing is set smaller than 12px.

## 7. Layout, product entries and motion

**Theme settings → Layout**

- **Fill wide screens**: the sheet runs from the spine to the right edge.
  Turn off to hold it to **Sheet width when not filling the screen**; the
  spare room falls to the right, since the sheet is bound to the spine.
- **Spacing**: Compact, Regular or Airy.
- **Number the sections of each page**: each section heading carries its
  position on the page, like a chapter number.

Corners are square everywhere and there are no shadows or gradients; these
are part of the design, not settings.

**Theme settings → Product entries** controls how a product is drawn
wherever it appears (shelves, ledgers, search, basket):

| Setting | Default |
|---|---|
| Photograph shape: Portrait 4:5, Square, Tall 3:4 | 4:5 |
| Show the catalog number | On |
| Show the family (the product type, e.g. Oil) | On |
| Show tasting notes (from the `flavour` metafield) | On |
| Show the size (`size` metafield, else the variant title) | On |
| Reveal origin and process on hover (pointer devices only) | On |
| Change the crop to the second photograph on hover | On |
| Add to basket from the entry | On |
| Quick view: opens the entry in a dialog with pictures, options and add button | On |
| Metafield namespace | `custom` |
| Recipes blog | (none) |

Under **Wording** on the same page you can name the catalog in your own
words. Each field left empty uses the theme's wording, translated for the
shopper's language:

- **Name of the whole catalog**: the title of the page of every product
  (`/collections/all`) in browser tabs and search results. Empty: "The
  catalogue". The page's heading uses it too, unless the Catalog section's
  **Title of the all-products page** is filled in (see *Collections* below).
- **Title of the collections list**: Empty: "The catalogue, by family".
- **Product notes label**: what the `flavour` words are called, for example
  *Tasting notes* or *Finish*. Empty: "Notes".

Products with one variant get an **Add** button on the entry; products with
several link to their page with **Choose**.

**Theme settings → Motion**

- **Motion**: None, Restrained (default) or Expressive. Drawers slide, rows
  open and photographs are uncovered by a moving crop. Visitors whose device
  asks for reduced motion always get none.
- **Smooth scrolling**: eases mouse-wheel and trackpad scrolling. Touch,
  keyboard and reduced-motion visitors always scroll natively.

## 8. Home page sections

Every section below can be added from **Add section** on any page template
(except where noted), and each has a **Color scheme** setting. A fresh
install's home page runs: Hero film, Pantry index, Plate, Shelf reel,
Countdown, Families, Kitchen steps, Statement, Journal collage, Sign-off.

### Opening the page

- **Hero film**: a silent looping film beside or behind the headline.
  Settings: Video, Poster image (shown at once and when the film does not
  play; use the first frame), Description of the video (for screen readers),
  Caption, Line above the headline, Headline (italic words turn accent),
  Supporting line, Button label and link; **Layout** (Full screen with the
  headline over the film, or Beside with the film right or left), headline
  position, Height, Mobile order and Mobile crop focus. The film only starts
  after the page has loaded, never for reduced-motion or data-saver visitors,
  and always has a pause button.
- **Cover**: a magazine cover. Build the cover lines from **Words**,
  **Picture** (a small picture set inside the line, optionally linked to a
  product) and **Line break** blocks. Settings: Issue line, size of the cover
  lines, Staggered or Left lines, Introduction, button, up to three
  **Products** shown as small tickets with an add button, and a scroll cue.
- **Pantry index**: the table of contents. One sentence (the page's main
  heading on the home page), a side note and two links, then **Product row**
  and **Collection row** blocks. Pointing at or tapping a row opens it like
  a drawer to show a wide photograph and particulars. **Add to basket from an
  open row** adds single-variant products directly.

### Products

- **Shelf reel**: "On the shelf this week". Choose a **Collection** (empty
  shows the whole catalogue) and **Entries to show**. On desktop the section
  pins while its entries travel sideways; on phones and with reduced motion
  it is a row you swipe.
- **Shelf**: a collection as a **Run** (scrolls sideways) or **Cells** (a ruled
  table, four across), with title, entry count and link.
- **Featured product**: one product with its own blocks (title, statement,
  tasting notes, price, variant picker, quantity, buy buttons, particulars,
  description and more). Photograph position and shape, and a link to the
  full entry.
- **Families**: your collections as giant stacked words; pointing at one
  floats its picture. Add a **Family** block per collection, with optional
  photograph and a one-line note.
- **Recently viewed**: the products this visitor opened before, kept in
  their own browser.

### Story and pause

- **Plate**: one large photograph or film. Shapes: Landscape 3:2, Wide 16:9,
  Slit 16:5, Portrait 4:5; width on the sheet or bleeding to the right edge.
  **Effect: Open to full bleed** starts the picture inset and opens it to the
  screen's edges as it reaches the middle. A Shopify-hosted video can **Play
  silently on a loop** (starts when it comes on screen, with a pause button)
  or a YouTube/Vimeo address can be used, loaded only when pressed.
- **Statement**: one or two sentences that darken word by word as the page
  scrolls, with up to six **Fact** blocks beneath (term and value) and a
  link. Size: Section, Title or Display.
- **Chapter**: a numbered chapter of text with a photograph right, left or
  full width under the text, a caption and a marginal note. **Title is**
  lets one chapter be the page title (h1) on a page without another.
- **Annotated image**: a photograph with numbered **Note** markers you place
  by position across and down; the notes are listed beside it.
- **Timeline**: **Moment** blocks (year, title, text, optional photograph).
- **Register**: a ruled table of up to three columns with optional row
  photographs. Two presets: *Register: makers* and *Register: delivery*.
- **Letters**: customers' letters (text, writer, place, optional product).
- **Questions**: questions that open in place. Open the first answer, and
  close the others when one opens.

### Kitchen and journal

- **Kitchen steps**: one recipe told as steps beside a sticky picture. Pick
  a **Recipe** (empty uses the newest recipe in your recipes blog). Add
  **Step** blocks (title, text, photograph or video, product with its add
  button), or add none: one step is made for each product the recipe is
  tagged with.
- **Recipe and its pantry**: a recipe beside the products it uses, each with
  an add button.
- **Journal collage**: a blog as a collage of pictures in three columns that
  move at different speeds. **Field notes** shows a blog as a plainer list.
  Both take a Blog, Heading and number of entries.

### Sign-ups and closing

- **Countdown**: counts to a real deadline, either **a weekly dispatch
  cut-off** (choose days and a time) or **one date and time**. Time zone,
  kicker, heading, text and button; when a one-off date passes it shows a
  message or removes itself. Use real deadlines only.
- **Dispatch**: a newsletter sign-up with title, text and small print.
- **Sign-off**: the back cover. Your shop's name set across the full width
  on cobalt, one line, up to three links and the newsletter sign-up. On a
  page that ends with it, the Colophon hides its own large name.
- **Custom Liquid**: for app snippets or your own code.

Sign-ups from any form are saved to **Customers** with the tag
`newsletter`.

## 9. Story, contact and other pages

- **Story page**: assign the `page.about` template to a page under **Online
  Store → Pages → Theme template**. It is built from Chapter, Annotated
  image, Timeline and Plate sections; change or add any section.
  Create more templates like it from the template picker in the editor.
- **Contact page**: assign `page.contact`. Add **Detail** blocks (term and
  value, e.g. Hours). Settings: introduction (shown when the page has no
  text) and **Ask for a phone number**.
- **Page**: a **Shelf mark** (small label above the title) and the
  published date.
- **Families index** (`/collections`): every collection or those in a menu,
  sort order, families per page and entry counts.
- **404 page**: shows the look-up and the browse menu.
- **Password page**: message, email sign-up and social links.

## 10. Collections and Look up results

The **Catalog** section sets a collection as a catalog rather than a
plain grid:

- **Title of the all-products page**: the heading Shopify would otherwise
  call "Products". Empty: the theme's **Name of the whole catalog**, or "The
  catalogue". Browser tabs always use the theme setting, so set the name
  there to keep tab and heading the same.
- **Show the collection description / image** (the image as a slit).
- **Families menu**: a strip of tabs, one per link, with entry counts.
- **Shelf layout**: *Catalog rhythm* (one feature entry, four standard
  entries, three ledger rows, repeating) or *Even shelves*.
- **Entries per page** and **Opening view**: Shelves or Ledger. Shoppers can
  switch, and their choice is remembered on their device.
- **Refine and sort**: **Show Refine** (filters, chosen in the **Search &
  Discovery** app) and **Show sorting**. Both sit on one line above the
  entries, beside the Shelves | Ledger switch, and work with JavaScript off.
- **Promo tile** blocks (up to four): a tile set into the grid after a
  chosen product, one or two cells wide, with optional image. Shown on the
  first page only and not while a filter is on.

**Look up results** has the same layout, view, Refine and sorting settings.
Under **Before a look-up, and when nothing is found**: **Show entries from
the shelf** (a **Collection**, all products if none, and **Entries shown**)
and **Suggest the browse menu**.

## 11. Product page

The product page is a **dossier**: the plates (photographs) on one side, a
label that stays in view beside them, then the details and margin notes.

**Main product** settings: **Photograph shape**, **Enable image zoom**,
**Show the plate index** (a numbered column of thumbnails on desktop),
**Keep the label in view while scrolling** and **Show the add bar on phones**
(a slim bar with name and add button while the main button is off screen).

Blocks in the label (add, remove and reorder freely):

| Block | Notes |
|---|---|
| Title, Vendor, Price | Price shows sale and unit prices where they apply. |
| SKU | The selected variant's SKU; hidden when the variant has none, and updated when the variant changes. |
| Statement | One sentence from the `statement` metafield. |
| Tasting notes | From the `flavour` metafield. |
| Contents | For a box or a set: the products in its `contents` metafield (a list of products), as numbered rows with photograph, family and size, each linking to its own page. Prints nothing for a product without one. |
| Variant picker | Color and image swatches from **Settings → Products → Variants**, optional. |
| Quantity pricing | Quantity rules and price breaks from a B2B catalog or price list. |
| Quantity selector, Buy buttons | Buy buttons show dynamic checkout, Shop Pay instalments where eligible, gift card recipient fields, and handle pre-order. |
| Back-in-stock alert | Shown only while the selected variant is sold out. Requests arrive as contact form emails; the customer is tagged `back-in-stock`. |
| Trust badges | Up to four **Point** blocks (icon and text). |
| Inventory status | Pre-order availability, and an optional low-stock count (off by default). |
| Pickup availability | From your pickup locations. |
| Particulars | Origin, maker, process, season, use, size and batch from metafields. |
| Share, Custom Liquid, apps | |

Two fixed groups sit under the label:

- **Margin**: Margin note, Dietary badges, Delivery estimate, Origin, Share,
  Custom Liquid and apps.
- **Details**: rows that open like drawers. Description, Ingredients,
  Nutrition panel, Allergen notice, Storage info (with optional care
  symbols), Text row, Delivery estimate, Origin, Dietary badges, Custom
  Liquid and apps. Rows with no data are left out.

Below the dossier, the product template adds **Companions** (the `pairings`
metafield, or Shopify's recommendations), **In the kitchen** (recipes tagged
with this product) and **Recently viewed**.

### Image zoom

With **Enable image zoom** on, shoppers can open a photograph full screen
and zoom in. Videos and 3D models are not affected.

### Pre-order

On the **Buy buttons** block, **Sell out-of-stock variants as pre-orders**
applies to variants that track inventory, have none left and are set to
*Continue selling when out of stock*. The button reads **Pre-order**,
dynamic checkout buttons are hidden, and the **Shipping note** is shown and
saved on the order. A product with an upcoming date in the
`preorder_ship_date` metafield shows that date instead. Keep **Show
pre-order availability** on the Inventory status block in step with it.

## 12. Recipes and field notes

Recipes link to products with **no app and no metafield**: tag a recipe
article with the **handle** of each product it uses. The handle is the last
part of the product's address: `/products/preserved-lemons` has the handle
`preserved-lemons`.

1. Choose the blog under **Theme settings → Product entries → Recipes blog**.
2. On each recipe, add a tag per product, written exactly as the handle
   (lower case, hyphens). Other tags ("Supper", "Winter") stay ordinary
   tags. Up to 20 tags per recipe are checked.

Then:

- the recipe shows **From the pantry**: those products with add buttons (up
  to eight), plus optional `serves` and `time` facts from article metafields;
- the product page's **In the kitchen** section lists up to three recipes
  tagged with its handle (it looks through the newest 50 articles);
- Kitchen steps and Recipe and its pantry use the same tags.

Any other blog is treated as **field notes**; a note tagged with product
handles lists them as "Mentioned in this note". The **Blog post** section has
settings for featured image, author, date, reading time, tags, share,
next/previous links and comments. The **Blog posts** section can show a
separate introduction on the recipes blog and the tags as an index strip.

## 13. Basket: drawer or page

**Theme settings → Basket → Basket opens as**: a drawer from the spine
(default) or its own page. Both show line and order discounts, the tax line
and dynamic checkout buttons, and close with a double rule under the total.
**Enable cart note** adds a note field.

The basket page is a **ledger**: column heads (No., Entry, Qty, Figure) over
one ruled line per product, the tally across the full width, then the note
and gift wrap on the left and the way to checkout on the right. On a phone
the checkout button, which carries the total, stays at the foot of the
screen until the end of the list reaches it.

An **empty basket** shows three entries "on the shelf": from the collection
chosen in the **Basket** section's **Products shown in an empty basket**
(all products if none); the empty drawer takes three from all products.
Under **Theme
settings → Basket → Empty basket**, **Heading over the suggested products**
and **Link to every product** rename them; empty fields use "On the shelf
now" and "See the whole catalogue".

### Gift wrapping

**Offer gift wrapping** adds a gift wrap option to the basket. With no
**Gift wrap product** chosen it is free and recorded as a note on the order;
with a product chosen, that product is added when the shopper checks the box
(and the option hides while it is unavailable). **Let shoppers add a gift
message** adds a message field.

## 14. Colophon, newsletter and promo pop-up

The **Colophon** (footer) takes **Links** (a menu), **Text**, **Facts** (up
to six term/value pairs) and one **Newsletter** block. Settings: policy
links, social links, country and language selector, payment icons, Follow on
Shop, **Show the shop's name** set large across the foot (with its own color
scheme), and **Name the typefaces** ("Set in …" in the imprint line).

Social links are entered once under **Theme settings → Social media**
(Instagram, Facebook, TikTok, YouTube, Pinterest, X).

### Newsletter popup

The **Promo pop-up** section lives in the overlay group and is installed
there; hide or remove it to switch it off. It is a ruled sign-up **slip**
that slides out from behind the spine (it rises above the bottom bar on a
phone) with a numbered tab, "The dispatch, No. 01". It covers a corner of the
page, never the whole of it, so the shop stays in reach while it is out.

Settings: image, **Label** and **Issue number** (the tab), heading, text, an
optional **Discount code** shown with a copy button after sign-up (create it
under **Discounts** first), **Show after** (seconds), **Show again after
closing**, and **Also show on exit intent** (desktop). It is never shown
again to someone who signs up or to a signed-in customer who already
accepts marketing, never over an open drawer, and never while a shopper is
typing in a form. Escape or **Close** puts it away and returns focus. In the
theme editor it shows only while the section is selected.

## 15. Performance and accessibility

Built in; nothing to switch on:

- Only the first image on a page loads eagerly at high priority; everything
  else loads lazily with set dimensions so the page does not jump.
- Photographs inside the Index and Look up drawers load only when a drawer
  is first opened.
- The hero film waits until the page has loaded and gone quiet, and never
  downloads for reduced-motion or data-saver visitors. A Plate film set to
  play silently on a loop does not download until it comes on screen.
- Scripts are small, vanilla and deferred. The look-up script loads only
  when Look up opens as a drawer, the basket script only when the basket
  drawer or entry add buttons are on, and smooth scrolling (a bundled copy
  of Lenis) only when that setting is on.
- Navigation, product form, filters, sorting, pagination, basket and search
  all work with JavaScript off.
- One `h1` per page, skip link, landmarks, visible focus, 44px touch targets,
  labelled inputs, focus-trapped drawers and dialogs that close with Escape.
- Moving content (ticker, notices, films) always has a pause control, and
  reduced-motion visitors get a still page.

Keep your own content accessible too: write alt text for images (Shopify
admin, on each image), a description for each video, and check contrast if
you change a color scheme.

## 16. FAQ and troubleshooting

**The tasting notes, particulars, nutrition or allergen rows don't show.**
They read metafields and print nothing until a product has data. See the
**Custom data** guide.

**My recipe doesn't list its products.** Check the blog is chosen as the
**Recipes blog**, and that each tag is the product handle exactly (lower
case, hyphens, no spaces). Only the newest 50 recipes are searched from the
product page.

**Where is the header / hamburger menu?** It is the spine. The **Index** tab
is the menu; edit it under **Online Store → Navigation** and choose it in
**Spine and folio → Menu**.

**My logo doesn't show on the spine.** The spine is cobalt; a dark logo may
disappear. Upload a light version as **Spine logo**.

**The home page looks empty after install.** That is expected: choose
products, collections, photographs and films in each section. The sample
wording is there to replace.

**The countdown disappeared.** A one-date countdown removes itself after the
date if **When it ends** is set to *Remove the section*.

**Filters don't appear on a collection.** Turn on **Show Refine** and set up
filters in the **Search & Discovery** app.

**Can I bring back rounded buttons or a classic header?** No. Square
corners, the spine and the ruled sheet are the design of Scullery 2.0, not
settings.

**Where do I change the "Add" button text or other wording?** **Online Store
→ Themes → ⋯ → Edit default theme content.** Storefront text ships in
English, German, Spanish, French and Italian.

**Which version am I running?** **Online Store → Themes → ⋯ → Edit code**,
then open `config/settings_schema.json` and look for `theme_version`. This
guide covers **2.0.0**.

Still stuck? See the **Scullery support** page.
