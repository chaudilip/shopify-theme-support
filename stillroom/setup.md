# Setting up Stillroom

A step-by-step guide for getting your store looking right after installing
the Stillroom theme. No coding involved — everything here happens in **Online
Store → Themes → Customize** (the theme editor) or elsewhere in Shopify
admin.

If you want nutrition facts, ingredients, dietary badges, allergen notices,
storage info, origin, or delivery estimates to appear on your product pages,
read the companion guide **Custom data: nutrition, ingredients, dietary
badges, and more** as well — those panels are intentionally invisible until
you connect data to them, and that guide walks through it.

## Contents

1. [First run](#1-first-run)
2. [Navigation menus](#2-navigation-menus)
   - [Breadcrumbs](#breadcrumbs)
   - [Back to top button](#back-to-top-button)
3. [Announcement bar](#3-announcement-bar)
4. [Logo, brand name, favicon and social sharing image](#4-logo-brand-name-favicon-and-social-sharing-image)
5. [Choosing colors](#5-choosing-colors)
6. [Choosing fonts](#6-choosing-fonts)
7. [Layout, shapes and motion](#7-layout-shapes-and-motion)
8. [Building the homepage](#8-building-the-homepage)
9. [Your story page](#9-your-story-page)
10. [Cart: drawer or page](#10-cart-drawer-or-page)
    - [Gift wrapping](#gift-wrapping)
11. [Product page blocks](#11-product-page-blocks)
    - [Image zoom](#image-zoom)
    - [Pre-order](#pre-order)
12. [Newsletter, social links, payment icons, country/language selector](#12-newsletter-social-links-payment-icons-countrylanguage-selector)
    - [Newsletter popup](#newsletter-popup)
13. [Troubleshooting](#13-troubleshooting)

---

## 1. First run

After installing the theme (but before publishing it), open **Online Store →
Themes**, find Stillroom in your theme library, and click **Customize**. This
opens the theme editor, where every change previews live and nothing goes
public until you click **Publish**.

Work through this guide roughly in order: logo and navigation first, then
colors and fonts (which affect everything else), then the homepage content,
then the product page. Publish only once you're happy with the preview.

## 2. Navigation menus

The header supports menus up to **three levels deep** — a top-level link,
its dropdown items, and a further sub-dropdown under any of those.

1. Go to **Online Store → Navigation** in Shopify admin (this is outside the
   theme editor).
2. Edit your **Main menu** — this is the menu the header shows by default.
   Add, remove, and nest menu items here; drag an item onto another to nest
   it one level deeper.
3. Edit or create a **Footer menu** if you want quick links in the footer.
4. Back in the theme editor, open the **Header** section (inside the
   **Header** group at the top of the section list) to confirm which menu it
   points to, and choose a **Layout**: "Logo left, menu centre" or "Logo
   centre, menu below." The same section also has toggles for **Stick to
   top on scroll**, **Show search**, **Show country and language selector**
   and **Show account link**. All four are on by default.
5. Open the **Footer** section to point its menu blocks at the footer menu
   you built.

Keep top-level labels short — long labels wrap awkwardly at narrow widths.

Three things about the header settings:

- **Show account link** only shows anything when customer accounts are
  turned on for your store in Shopify admin. The link opens Shopify's own
  account panel. **Account menu handle** names the menu shown inside that
  panel. Leave it as `customer-account-main-menu` unless you have created
  your own customer account menu.
- **Show country and language selector** only shows a selector when your
  store sells in more than one country or language. In the header it shows on
  desktop screens. The footer has its own selector (see section 12).
- **Menu images need no setup.** A menu item that links to a collection, a
  product or a blog post shows that item's image in the mobile menu and in
  the mega menu. A menu item that links to a page or an outside address shows
  no image.

### Mega menu (optional)

Any top-level menu item that has sub-items can open as a full-width panel with
images instead of a plain dropdown.

1. In the theme editor, open the **Header** section and click **Add block →
   Mega menu**.
2. In **Menu item**, type the top-level menu item exactly as it appears in your
   navigation — "Shop", say. Spelling and capitalization have to match, and that
   item needs to already have sub-items under it in **Online Store →
   Navigation**.
3. Add up to three **Feature** images, each with an optional **Heading** and
   **Link**. These are the cards that appear on the right of the panel. Leave
   them empty and the panel still works — you just get the link columns.

You can add up to five mega menus, one per top-level item. Any item without a
matching block keeps the normal dropdown.

Two things worth knowing:

- **Nothing loads until you add a block.** The mega menu's JavaScript is only
  requested when at least one Mega menu block exists. A store that doesn't use
  the feature doesn't download it.
- **It works without JavaScript.** The panel opens on click and by keyboard on
  its own; hovering is an extra for mouse users. The staggered entrance is CSS,
  and it is skipped entirely for visitors whose device is set to reduce motion.

### Search

Under **Theme settings → Search**, **Search opens** chooses between **In a
drawer** (the default — it suggests products as the shopper types) and **On
the search page**. With JavaScript off it falls back to the search page
either way.

**Browse menu** picks the menu shown inside the drawer before anything is
typed; it defaults to your Main menu.

The search icon itself is turned on and off by **Show search** in the
**Header** section.

### Breadcrumbs

A breadcrumb trail is the short row of links at the top of a page that shows
where the page sits in your store, for example "Home › Oils › Chilli oil".

Turn it on or off under **Theme settings → Navigation → Show breadcrumbs**.
It is on by default.

The trail appears on product pages, collection pages, the all-collections
page, blogs, blog posts, pages, search results, the cart page and the "page
not found" page. It does not appear on the home page or on customer account
pages.

What the trail shows:

- Every trail starts with **Home**.
- The last item is the page being viewed. It is plain text, not a link.
- **Product pages** show the collection only when the shopper reached the
  product through that collection. A shopper who arrived from search, or from
  a direct link, sees "Home › Product name". The theme does not guess a
  collection.
- **Collection pages** filtered by a tag show the collection, then the tag.
- **Blog posts** show the blog, then the post.

The theme also writes the same trail into the page as structured data, which
search engines can read. There is nothing to set up for this, and it turns off
together with the visible trail.

### Back to top button

A round button with an upward arrow that takes the visitor back to the top of
the page.

Turn it on or off under **Theme settings → Navigation → Show back-to-top
button**. It is on by default.

- It sits in the bottom right corner of the screen.
- It stays hidden until the visitor has scrolled about one and a half screens
  down, so it does not show on short pages.
- The ring around the arrow fills as the visitor moves down the page.
- For visitors whose device is set to reduce motion, the page jumps to the top
  instead of scrolling smoothly.
- With JavaScript off the button is always visible and still works.

## 3. Announcement bar

The announcement bar lives in the **Header** group in the theme editor, above
the Header section. It is the one section that can only be added there — it
isn't available on the homepage or any other template.

Add up to **eight Message blocks**. Each has **Text**, an optional **Link**,
and an **Icon** (delivery van, clock, leaf, seed, tick, star, or no icon).

- **Scroll messages** (on by default) runs the messages as a continuous
  scrolling strip. **Scroll duration** sets how long one full pass takes,
  from 15 to 90 seconds — a longer duration is a slower scroll.
- **With scrolling turned off, only the first message shows.** The bar
  becomes a single centred line. If you have several things to say and don't
  want the marquee, put them in one message or rotate them by hand.

### The pause button

When scrolling is on, a small pause button sits at the right-hand end of the
bar. Moving text that a shopper can't stop is an accessibility failure, so
this is deliberate and it can't be turned off. It is hidden in the two cases
where there is nothing to pause:

- for visitors whose device is set to reduce motion, where the messages are
  laid out static instead of scrolling; and
- when JavaScript is unavailable, where the strip never starts moving.

The strip also pauses on hover and on keyboard focus.

## 4. Logo, brand name, favicon and social sharing image

All of these live under **Theme settings** (the gear icon at the bottom of the
left-hand section list in the theme editor) → **Branding**:

- **Brand name** — the name shown in page titles, the footer, the header
  wordmark when you have no logo, the gift card, and the `og:site_name` tag
  used by link previews. Leave it blank and the theme uses your Shopify store
  name from **Settings → Store details**. Set it when the name you trade
  under differs from the store name in Shopify — for example when one Shopify
  store serves more than one storefront.

  **Checkout and order emails always use the Shopify store name, not this
  one.** Those pages belong to Shopify, not to the theme, so a brand name set
  here cannot reach them. If you need the name consistent everywhere, change
  it in **Settings → Store details** instead.
- **Logo** — upload your logo image and set its display width with the
  **Logo width** slider. A wide, short logo (roughly 3:1 or wider) reads
  best against the header's layout.
- **Favicon** — the small icon shown in browser tabs. Shopify scales it down
  to 32×32px automatically, so start with a simple, high-contrast square
  image.
- **Home screen icon (iOS)** — used when someone saves your store to an
  iPhone or iPad home screen. Upload a **square image of at least 180×180**
  with a **solid background**.

  This is a separate setting from the favicon on purpose, and reusing the
  favicon here will look wrong. Two reasons. Shopify's image CDN does not
  upscale, so asking a 32×32 favicon to fill a 180×180 slot returns the
  32×32 file and iOS blows it up. And iOS composites transparency onto
  **black** and applies its own rounded mask, so the transparent cut-out
  that is right for a browser tab becomes a small mark stranded on a black
  square.

  Left empty, no icon is declared at all and iOS uses a screenshot of the
  page instead — plain, but not broken. That is the intended fallback, which
  is why the theme does not quietly substitute the favicon.
- **Social sharing image** — shown when a link to your homepage is shared on
  social media or messaging apps that generate a link preview. Use a
  landscape image (1200×630px is the safe default) with your logo and
  branding.

## 5. Choosing colors

Stillroom ships four **color schemes** under **Theme settings → Colors**.
Each section on your store uses one of the four via its own **Colors**
setting, so you don't need to touch the schemes themselves to reassign
where each palette shows up — but if you do want to rebrand, edit the
scheme and every section using it updates together.

| Scheme | Feel | Used by default on |
|---|---|---|
| Scheme 1 | Warm oat background, dark ink text and buttons, persimmon reserved for marks | Most sections — header, hero, product grid, product page, most homepage content |
| Scheme 2 | Slightly deeper oat/tan background, dark button | Brand story, testimonials, newsletter, press and stockists, visit us |
| Scheme 3 | Full persimmon (bright orange) background | Announcement bar, delivery promise strip |
| Scheme 4 | Dark ink background, oat text, persimmon accent | Footer. Also available for any section you want to feature in a dark, high-contrast block |

These are the schemes a section starts on when you add it. The home page that
ships with the theme changes a few of them so that neighbouring sections
alternate, so what you see on a fresh install can differ from this table.

Each scheme controls: Background, Background gradient (optional), Text,
Secondary text, Accent, Accent text, Text on accent, Button background,
Button label, Secondary button label, Card and panel background, and Borders
and dividers.

**The rule that matters most: anything sitting on a bright color needs a dark
label, never a light one.** Dark ink on the bright orange reads comfortably;
white or pale text on that same orange is genuinely hard to read and fails
Shopify's accessibility contrast requirements outright — it's not a matter of
taste, it's a measurable pass/fail.

Three settings carry the accent, and they are deliberately separate:

- **Accent** is the color itself — the fill behind a sale badge, the ring
  round a highlighted word.
- **Accent text** is a darker version of the accent used for links and sale
  prices, so small colored text on the page background stays readable. It is
  checked against the **Background**.
- **Text on accent** is checked against **Accent**. It colors the things
  painted straight onto the accent color rather than onto a button: sale
  badges, low-stock chips, the selected size or variant, the current page
  number, the video play button. Keep it dark enough against your accent to
  clear 4.5:1.

And separately:

- **Button label** is checked against **Button background**. If you give a
  scheme a dark button, its label should be light — that pairing is fine.

If you change the accent or the button color, check both pairs before saving.
Passing one does not mean the other passes — they are different pairs of
colors, and that is exactly why there are separate settings.

## 6. Choosing fonts

Under **Theme settings → Typography** there are three separate font
pickers:

- **Display font** — used for headings, product names, and prices. Defaults
  to Playfair Display, a serif.
- **Body font** — used for paragraph and body text. Defaults to Lora.
  This is deliberately *not* the same face as the display font: Playfair is a
  high-contrast display serif whose thin strokes get fragile at paragraph
  sizes, so running text uses Lora, its sturdier text companion. You can set
  both to the same family if you prefer, but check a long paragraph on a phone
  before you do.
- **Utility font** — used for navigation, badges, sizes, prices and the
  announcement bar. Defaults to Jost.

The utility font is deliberately a **geometric sans**, and deliberately not
the body font. It carries the small text that *names* things rather than text
you read in sentences: nav items, size chips, dietary badges, the announcement
bar, the figures in a cart summary. Those want even, open letterforms that hold
their shape in caps at 11px with letter spacing — which is what a geometric
sans does and a text serif does not.

Keeping it separate from the body font is the point. Set both to the same
family and those labels stop reading as labels.

Each font picker has its own **Size** slider, and the display and utility
fonts also have a **Letter spacing** slider, so you can fine-tune scale and
tracking without changing the typeface itself.

## 7. Layout, shapes and motion

Three more theme-setting groups affect the whole store at once. (A fourth,
**Navigation**, holds the breadcrumb and back-to-top settings covered in
section 2.)

**Theme settings → Layout** sets **Maximum page width** (1000–1800px,
default 1440), **Page margin** (the gutter at the screen edge), **Space
between sections**, and **Grid spacing** (the gap between cards in a grid).
Widening the page and tightening the gaps gives a denser store; the defaults
are set for a roomy, editorial feel.

**Theme settings → Shapes** sets the corner radius for panels, images and
inputs, and the **Button shape** (Pill, Rounded, or Square). Set the radii to
0 for a squared-off look. Two extras live here:

- **Offset button outline** adds a second, offset dashed outline behind
  buttons.
- **Show drawn ornaments** controls the small drawn motifs — an olive sprig,
  an ear of wheat, a jar seal, a swash under headings. Turn it off for a
  plainer store; nothing else changes.

**Theme settings → Motion** has two checkboxes:

- **Reveal sections on scroll** (on by default) fades and lifts sections,
  cards and the hero as they come into view. This also drives the hero's
  staggered entrance and the mega-menu panel's.
- **Scale images on hover** (on by default) grows product and section images
  slightly under the cursor.

All motion in the theme is CSS, and all of it is switched off automatically
for visitors whose device is set to reduce motion — you do not have to choose
between the animation and accessibility.

## 8. Building the homepage

Your homepage is built from sections, top to bottom, in the theme editor.
Click **Add section** at the point in the list where you want a new one, or
drag existing sections to reorder them.

Stillroom ships **26 sections** you can add. Twenty-four of them can go on the
homepage; the remaining two are restricted by design — the **Announcement
bar** is only available in the Header group (see section 3), and **Product
recommendations** only on product pages. Everything else below can be added
to the homepage, a page, the collection template, or anywhere else that takes
sections.

### Banner and story

- **Hero** — the top banner. Set an eyebrow line, heading, body text, an
  optional badge, an image with an **Image shape** (Arch, Blob, or Square),
  a **Layout** (image first or image last), and up to two **Button** blocks.
  **Highlighted word** rings one word of the heading in a dashed ellipse —
  type the word exactly as it appears in the heading, including its
  capitalization, or nothing is ringed.
- **Slideshow** — up to 6 **Slide** blocks, each with an image, eyebrow,
  heading, text, and button. Autoplay and its speed are configurable, and it
  always pauses for visitors who prefer reduced motion.
- **Image with text** — a classic split layout: an image on one side, a
  heading, body copy, and up to two **Button** blocks on the other. **Image
  shape** sets the proportions (Portrait, Square or Landscape) and **Image
  outline** sets the outline (Arch, Blob or Square). **Layout** sets which side the image sits on.
- **Brand story** — a larger image-plus-text block meant for your founding
  story, with up to four **Stat** blocks (a value and a label) for things
  like "years in business" or "growers partnered."
- **Rich text** — a flexible, centered or left-aligned content block built
  from four kinds of block: **Eyebrow**, **Heading**, **Text** and
  **Button** — use it for one-off editorial copy that doesn't fit another
  section.

### Products

- **Collection list** — a grid of collection tiles ("shop by category").
  Add one **Collection** block per tile (up to 12); each block can override
  the title and image, and choose an **Image shape** (Arch, Blob, Square).
  2, 3 or 4 columns on desktop.
- **Featured collection** — pulls products live from one collection you
  pick, with a heading and an optional "View all" link. **Products to show**
  runs from 2 to 12; 3 or 4 columns on desktop.
- **Featured product** — spotlights a single product you choose, using the
  same blocks as the full product page (title, price, variant picker,
  description, and the food data blocks) so you can add a deep-dive for a
  hero product without sending shoppers away from the homepage. **Image
  position** puts the gallery left or right, **Make gallery sticky on
  scroll** keeps it in view while the details scroll, and **Enable image
  zoom** works as it does on the product page (see
  [Image zoom](#image-zoom)).
- **Product recommendations** — *product pages only.* Shows **Related
  products** or **Complementary products** for the product being viewed,
  chosen by Shopify. Complementary products are the ones you pick yourself in
  Shopify's Search & Discovery app; related products need no setup.
  **Products to show** runs from 2 to 10. When there is nothing to
  recommend, the section removes itself from the page.
- **Collections list** — the section that powers the "all collections" page.
  Leave its collection blocks empty and it lists every collection in your
  store, ordered by the **Sort** setting; add **Collection** blocks to
  choose and order them by hand instead.
- **Collection banner** — the heading area of a collection page: toggles for
  the collection image, its description, and the product count. It belongs on
  the collection template, though the editor will let you add it elsewhere.

### Reassurance and detail

- **Multicolumn** — a row of short feature callouts, each a **Column** block
  with an icon (Leaf, Truck, Clock, Checkmark, Star, Info, or None), a
  heading, text, and an optional link. Good for "why buy from us" points. 3
  or 4 columns on desktop.
- **Delivery promise** — a strip of short delivery/shipping reassurances
  ("Free delivery over $75," etc.), up to 6 **Promise** blocks with an icon
  (Truck, Clock, Leaf, Checkmark, Star) and text. Display as a **Row** or a
  **Scrolling marquee**.
- **How it's made** — an ordered sequence of up to 8 **Step** blocks, each
  with an optional image, a **Label** for a time or a season ("Late
  October", "Eight weeks"), a heading and text. The steps are numbered for
  you. Lay them out **Steps across** or **Steps down the page**. Add an
  image to one step and every step keeps a matching frame, so a part-
  illustrated sequence still lines up.
- **FAQ** — an accordion of up to 24 **Question** blocks, each a question and
  a rich-text answer. **Layout** puts the heading beside the questions or
  above them. **Open the first answer** starts the first one expanded, and
  **Allow several answers open at once** decides whether opening one closes
  the last (older browsers always allow several). There is also an optional
  link below the questions — for "still stuck? write to us". The accordion is
  built on the browser's own disclosure element, so it opens, closes and is
  searchable with JavaScript off.
- **Press and stockists** — a row of up to 12 **Logo** blocks, each with a
  logo image, a **Name** and an optional link. **A logo block with no image
  falls back to showing the name set in the display serif** — useful for a
  publication or a stockist that has no usable mark, and it means the row
  never shows a gap. Fill in **Name** either way: it is the image's
  alternative text. **Logo height** (20–80px) sets every logo to the same
  height so marks of different proportions sit on one line, and **Mute the
  logos** fades each one back until it is hovered.
- **Visit us** — your address, opening hours and a directions link, beside an
  optional photograph of the shop front or stall. Hours and any other details
  are **Detail row** blocks, up to 10, each a label and a value ("Thu to
  Sat" / "9am until 4pm"). **This is deliberately not a map embed.** Paste a
  link to your location from whatever map service you prefer into
  **Directions link** and the section sends people there — no third-party
  map script loads on your storefront, and nothing breaks when a maps API key
  expires.
- **Countdown** — a sale timer. Set **Ends at** in your store's time zone
  using `YYYY-MM-DD HH:MM` (for example `2026-10-03 23:59`); leave it empty
  and nothing shows on the storefront. **Display style** is a band in the
  page, a bar pinned to the bottom, or a card in the bottom corner — the bar
  and the card float above the page and the visitor can close them. **When it
  ends** either removes the section or shows a "this sale has ended" message.

### Editorial

- **Recipe feature** — a single recipe card. Add a **Recipe feature** block, connect
  it to a blog article, and fill in (or connect via dynamic source) **Prep
  time**, **Cook time**, **Servings**, **Level**, **Dietary note**,
  **Ingredients**, and **Method**. See the **Custom data** guide for the
  dynamic-source part.
- **Video** — a heading, subheading, and either a Shopify-hosted video or a
  YouTube/Vimeo URL, with a cover image shown before play.
- **Testimonials** — a heading and up to 12 **Testimonials** blocks, each
  with a quote, name, role or location, and star rating. Choose a **Grid** or **Scrolling
  marquee** layout.
- **Blog posts** — a preview grid pulled from one blog you choose, with
  toggles for date, excerpt, and author.
- **Newsletter** — an email signup with an eyebrow line, a heading and body
  text.
- **Promotional popup** — an email signup or offer shown in a popup. It ships
  switched off, in the **Footer** group. See
  [Newsletter popup](#newsletter-popup) in section 12.
- **Custom Liquid** — for advanced customization: paste raw Liquid/HTML
  (from a developer, or an app's install instructions) directly into a
  section. Available on every template.

Every content section above also accepts a **Custom Liquid** block inside
it, for the same purpose at a smaller scale.

## 9. Your story page

Every shop needs an about page, and a page with nothing but a heading and three
paragraphs is the one most likely to be skipped. Stillroom ships a ready-made
layout for it.

1. In Shopify admin go to **Online Store → Pages → Add page**.
2. Title it whatever you like — "Our story", "About us", "The kitchen".
3. Write your opening paragraph in the page's own content box. That is the only
   part you edit here; everything below it is edited in the theme editor.
4. On the right, under **Online Store**, open the **Theme template** dropdown
   and choose **about** instead of *Default page*.
5. Save, then open **Online Store → Themes → Customize** and pick your new page
   from the page selector at the top to edit the rest.

You get a composed page rather than a blank one: your opening, an
image-and-text spread for how it started, the brand story block with three
figures, a three-column section, and three customer quotes. Every section can
be reordered, edited or removed like any other, and you can add more — the
new **How it's made**, **Press and stockists**, **FAQ** and **Visit us**
sections all suit this page.

**Replace the placeholder copy.** It is written about a fictional preserves
maker, and it is there to show the shape of the page, not to describe your
business. The same goes for the figures in the brand story block and the
quotes — those are examples, and quotes in particular should only ever be real
ones from real customers.

Two images to add while you are there: one in the image-and-text section and
one in the brand story section. Both show a placeholder until you do.

### Making more pages like it

The **about** template is not limited to one page. Any page can use it —
stockists, sourcing, a press page — and each gets its own content while sharing
the layout. If you want two genuinely different layouts, duplicate the theme
and edit the second one, or build the page up from a Default page by adding
sections yourself.

## 10. Cart: drawer or page

Under **Theme settings → Cart**, the **Cart type** setting controls what
happens when a shopper adds something to their cart:

- **Drawer** (default) — a panel slides in from the side without leaving
  the current page.
- **Page** — adding an item takes the shopper to the dedicated cart page.

There's also an **Enable cart note** toggle, which adds a free-text field
where shoppers can leave a note with their order (delivery instructions and
so on). It is off by default.

### Gift wrapping

Gift wrapping adds a tick box to the cart labelled "Add gift wrapping". It
shows in both the cart drawer and the cart page. It is off by default.

There are three settings under **Theme settings → Cart**, below the **Gift
wrapping** heading:

- **Offer gift wrapping** — turns the feature on.
- **Gift wrap product** — optional. Leave it empty for free wrapping. Choose a
  product to charge for wrapping.
- **Let shoppers add a gift message** — on by default. When the shopper ticks
  the box, a **Gift message (optional)** field opens. A message can be up to
  200 characters.

**Free gift wrapping**

Use this when you do not charge for wrapping.

1. Go to **Theme settings → Cart → Offer gift wrapping** and tick it.
2. Leave **Gift wrap product** empty.
3. Save.

The cart shows "Add gift wrapping" with the word "Free" beside it. Nothing is
added to the cart. The request is saved on the order as two cart attributes:

- **Gift wrap:** Yes
- **Gift message:** the text the shopper typed

You see both on the order in Shopify admin. Check each order for them before
you pack it.

**Paid gift wrapping**

Use this when you charge for wrapping. The theme adds a product to the cart,
so the charge goes through checkout like anything else you sell.

First, create the product:

1. In Shopify admin go to **Products → Add product**.
2. Give it a title shoppers will understand in their cart, such as "Gift
   wrapping". Add an image if you want one shown in the cart.
3. Set the **Price** you charge for wrapping.
4. Keep it to a single variant. If the product has several, the theme uses
   the first one that is available.
5. Make sure it cannot sell out. Either turn inventory tracking off for it,
   or tick **Continue selling when out of stock**.
6. Set the status to **Active** and make sure it is available to the
   **Online Store** sales channel.
7. Save.

Then connect it:

1. Go to **Theme settings → Cart → Offer gift wrapping** and tick it.
2. In **Gift wrap product**, choose the product you created.
3. Save.

The cart now shows "Add gift wrapping" with the price beside it. When the
shopper ticks the box, the product is added to the cart as its own line. When
they untick it, the line is removed.

Things to know about paid wrapping:

- The wrap line has no quantity selector. It is one wrap per order.
- **Gift wrap: Yes** and **Gift message** are saved on the order in paid mode
  too, so you read the request in the same place either way.
- If the shopper removes everything else from the cart, the theme removes the
  wrap as well.
- **If the gift wrap product is sold out or unavailable, the gift wrapping
  option is hidden from the cart** until the product can be bought again.
  This is why step 5 above matters.
- A gift wrap product priced at 0 also shows as "Free".
- The gift wrap product is a normal product. It can appear in search results
  and in any collection it belongs to.
- With JavaScript off, the shopper's request and message are still saved on
  the order from the cart page, but the paid product cannot be added to the
  cart.

## 11. Product page blocks

Open the theme editor, navigate to a product page (use the page picker at
the top), and select the **Main product** section. The block list on the
left shows every block on the page, top to bottom, in the order they
render.

**To add a block:** click **Add block** and choose from the list — the
standard commerce blocks (Title, Price, Vendor, Inventory status, Pickup
availability, Variant picker, Quantity selector, Buy buttons, Description,
Share) and the
Stillroom-specific data blocks (Nutrition panel, Ingredients, Dietary badges,
Allergen notice, Storage info, Origin, Delivery estimate), plus Custom
Liquid and any app blocks you've installed.

**To reorder blocks:** drag a block up or down in the list, or select it and
use the reorder handles. The product page ships in this order: Vendor,
Title, Price, Dietary badges, Description, Variant picker, Quantity
selector, Inventory status, Buy buttons, Pickup availability, Delivery
estimate, Allergen notice, Ingredients, Nutrition panel, Storage info,
Origin, Share.

**To remove a block:** select it and click the trash icon.

The **Featured product** homepage section (see above) uses the exact same
block set, so anything you learn here applies there too.

Some of the standard blocks have settings of their own:

- **Inventory status** — **Low stock threshold** (1 to 50, default 5) sets
  the quantity at which the block starts to warn that stock is low. **Show
  pre-order availability** is covered under [Pre-order](#pre-order).
- **Variant picker** — **Show colour and image swatches** (on by default)
  shows the colour or image you set on an option value in Shopify admin.
  Option values without one stay as text buttons.
- **Buy buttons** — the two pre-order settings, covered under
  [Pre-order](#pre-order).
- **Pickup availability** — no settings. It shows only on products that are
  stocked at a location with local pickup turned on. On a store without local
  pickup it shows nothing.

The seven data blocks — Nutrition panel, Ingredients, Dietary badges,
Allergen notice, Storage info, Origin, Delivery estimate — render **nothing
at all** until you connect data to them. This is intentional: a food-first
theme still needs to work cleanly for a merchant who hasn't set up that data
yet. See the **Custom data** guide to connect them.

Two of them do more than one thing:

- **Storage info** holds three independent parts: the storage instructions,
  a **Shelf life** line, and the **Care symbols** checkboxes. The symbols
  need no metafield at all — they are plain checkboxes in the theme editor,
  and the block appears as soon as you tick one even with no text connected.
  The **Custom data** guide lists what each symbol means.
- **Dietary badges** takes a comma-separated list, so you can type
  `Vegan, Gluten-free` straight into it without setting up any data.

### Image zoom

Shoppers can open a product image full screen and zoom in to see detail.

Turn it on or off in the theme editor: open a product page, select the **Main
product** section, and find **Enable image zoom**. It is on by default. The
**Featured product** section has the same setting, set separately.

How it works for the shopper:

- Each product image gets a zoom button. Selecting it opens the image in a
  full-screen viewer.
- In the viewer, the plus and minus buttons zoom in and out. On a touch
  screen the shopper can pinch or double tap.
- When a product has more than one image, previous and next buttons move
  between them.
- The keyboard works too: left and right arrows change image, plus and minus
  zoom, and Escape closes the viewer.

Things to know:

- Zoom applies to images only. Videos and 3D models are not affected.
- How far an image zooms depends on the size of the image you uploaded.
  Upload large images if you want shoppers to see fine detail.
- The large version of an image is only downloaded when a shopper opens the
  viewer.
- With JavaScript off the zoom button does not show, and the gallery works as
  normal.

### Pre-order

A pre-order lets shoppers buy a product that is out of stock now and will
ship later. Stillroom reads Shopify's own inventory settings to decide what is a
pre-order. There is no app to install and no tag to add.

**When a variant is a pre-order**

A variant is sold as a pre-order when all three of these are true:

1. Shopify tracks inventory for the variant.
2. The quantity available is zero or less.
3. **Continue selling when out of stock** is turned on for the variant.

**Setting it up in Shopify admin**

1. Go to **Products** and open the product.
2. If the product has variants, open the variant you want to sell as a
   pre-order.
3. In the **Inventory** area, make sure inventory tracking is turned on.
4. Tick **Continue selling when out of stock**.
5. Set the available quantity to 0.
6. Save.

When new stock arrives, enter the new quantity. The variant goes back to
normal selling on its own.

**What shoppers see**

- The buy button reads **Pre-order** instead of "Add to cart".
- The faster checkout buttons (such as Shop Pay) are hidden for that variant.
- A shipping note shows under the button.
- The **Inventory status** block reads "Available to pre-order".
- Product cards in collections, search results and recommendations show a
  **Pre-order** badge. On a product with a single variant, the quick add
  button also reads "Pre-order".

On a product with several variants, all of this follows the variant the
shopper has selected. A variant that is in stock shows the normal button.

**The theme settings**

In the theme editor, open a product page and select the block:

- **Buy buttons → Sell out-of-stock variants as pre-orders** — on by
  default. Turn it off and these variants show the normal "Add to cart"
  button, with no note and no "Pre-order" mark on the order.
- **Buy buttons → Shipping note** — the text shown under the button. The
  default is "Ships with the next batch". Leave it blank to show no note.
- **Inventory status → Show pre-order availability** — on by default. Keep
  it the same as the Buy buttons setting, so the two blocks do not disagree.

These settings belong to the blocks on the product page. The **Pre-order**
badge and button on product cards do not have a setting. They show whenever
the first available variant of a product meets the three conditions above.

**Showing a ship date (optional)**

You can give each product its own ship date. When a product has one, the note
reads "Ships" followed by the date, and that replaces the **Shipping note**
text for that product.

1. In Shopify admin go to **Settings → Custom data → Products** and click
   **Add definition**.
2. Name it "Pre-order ship date".
3. Check the **Namespace and key** reads `custom.preorder_ship_date`. Click
   **Edit** if it does not.
4. Choose the type **Date**.
5. Save.
6. Open the product, scroll to **Metafields**, and enter the date.

You do not connect this metafield to a block. The theme reads it directly.

A date that has already passed is ignored, and the note goes back to the
**Shipping note** text. Update or clear the date when the stock arrives.

**What you see on the order**

Each pre-order line on the order carries a property named **Pre-order**. Its
value is the note the shopper saw:

- the ship date, when the product has one;
- otherwise the **Shipping note** text;
- or "Yes" when the note is blank.

A pre-order added from a product card carries the ship date when the product
has one, and "Yes" otherwise. The card cannot read the **Shipping note** typed
into the Buy buttons block.

The shopper sees the same property on the line in their cart.

The theme only labels the order. It does not change when payment is taken,
and it does not hold the order for you.

## 12. Newsletter, social links, payment icons, country/language selector

- **Newsletter**: add the **Newsletter** section anywhere (homepage or
  elsewhere), or use the **Newsletter** block in the footer. Both submit to
  Shopify's built-in customer signup. For a signup that appears in a popup,
  see [Newsletter popup](#newsletter-popup) below.
- **Social links**: under **Theme settings → Social media**, paste the full
  URL for each network you use (Instagram, Facebook, TikTok, YouTube,
  Pinterest, X). Leave any you don't use blank — the theme only shows icons
  for networks you've filled in. These icons appear in the footer when
  **Show social icons** is turned on there.
- **Follow on Shop**: in the footer, **Show Follow on Shop button** (on by
  default) shows a button next to the social icons. Shopify draws the button
  and hides it where it does not apply.
- **Footer logo**: the footer's **Brand** block has an optional **Footer
  logo**. The footer ships on a dark color scheme, where a dark logo is hard
  to see, so upload a light version here. Left empty, the footer shows your
  store name as text.
- **Payment icons**: in the footer, toggle **Show payment icons** on. The
  icons shown are pulled automatically from the payment methods you've
  actually enabled in **Settings → Payments** — there's nothing to
  configure in the theme itself.
- **Country/language selector**: in the footer, toggle **Show country and
  language selector** on. This only shows a selector if you've set up
  multiple markets or languages under **Settings → Markets** / **Languages**
  — with just one market and language, the toggle has nothing to display.
  The **Header** section has the same toggle (see section 2).

### Newsletter popup

The **Promotional popup** section shows an email signup, or an offer with a
button, in a popup over the page. It ships with the theme in the **Footer**
group, so it covers the whole store, and it ships **switched off**.

**Turning it on**

1. In the theme editor, open the **Footer** group at the bottom of the
   section list and select **Promotional popup**.
2. Untick **Disable this popup**.
3. Save.

To turn it off again, tick **Disable this popup**. While you are in the theme
editor the popup opens when you select the section, whether it is disabled or
not, so you can edit it.

**Where it appears**

The popup does not appear on the cart page or on customer account pages. It
also waits while a shopper is typing in a field or has the cart or search
drawer open.

**Content**

- **Eyebrow**, **Heading** and **Text** — the wording.
- **Collect email addresses** — on by default. Shows an email field.
  Subscribers are tagged "newsletter" in your customer list. Untick it to
  show a button instead, using **Button label** and **Button link**.
- **Footnote** — a small line under the form.

**Picture**

**Picture** chooses what shows beside the wording:

- **Moving product grid** (the default) — three columns of your product
  photographs, moving slowly. There is nothing to upload. It uses the first
  photograph of each product, up to 18 products.
- **One image** — a single image you upload in the **Image** setting.
- **No picture** — wording only.

**Collection for the grid** chooses which products the moving grid uses.
Leave it empty to use your whole catalogue. An empty collection also falls
back to the whole catalogue.

**Image** is used only when **Picture** is set to **One image**. If no image
is uploaded, the popup shows no picture.

If your store has no products yet, the moving grid shows no picture. The grid
stays still for visitors whose device is set to reduce motion.

**When it appears**

- **Trigger** — **After a delay** (the default), **After scrolling**, or
  **On exit intent**. Exit intent means the mouse pointer leaving through the
  top of the window. Touch screens have no pointer, so on those the popup
  uses the delay instead.
- **Delay** — 2 to 30 seconds, default 8. Used with **After a delay**.
- **Scroll depth** — 10% to 90% of the page, default 40%. Used with **After
  scrolling**.
- **Show again after** — 1 to 90 days, default 30. How long before a visitor
  who has seen the popup sees it again. This is remembered in the visitor's
  browser.

The shopper can close the popup with its close button, with the Escape key,
or by selecting the area outside it.

## 13. Troubleshooting

**My nutrition panel isn't showing.**
The Nutrition panel block renders nothing until a metafield is connected to
its "Nutrition facts" field via the dynamic source picker (or you've typed
content into it directly). Open the block's settings, check whether that
field is empty, and see the **Custom data** guide to connect real data — the
block's own help text in the editor names the exact metafield to create. This
is expected behavior on a product with no nutrition data, not a bug.

**My dietary badges aren't showing.**
There are two separate dietary badge features, and each reads its own
metafield:

- The badges on the **product page** (the Dietary badges block) need either
  typed text or a connected metafield in that block's "Dietary tags" field.
  The theme suggests `custom.dietary_badges`, a **Single line text**
  metafield holding a comma-separated list.
- The badges on **product cards** (collection grids, search results,
  related products) are read from whichever metafield namespace/key you've
  entered under **Theme settings → Product cards → Dietary metafield
  namespace / Dietary metafield key**, which default to `custom` and
  `dietary_tags` and expect a **List of single line text** metafield. If the
  metafield you created doesn't match what's typed into those two settings,
  the badges silently don't show. Only the first three show on a card.

Also check **Theme settings → Product cards → Show dietary badges** is
switched on — it's on by default, but if it's off, cards never show badges
regardless of your data. The **Custom data** guide has the full setup.

**My announcement bar only shows one message.**
Turn **Scroll messages** on in the Announcement bar section. With it off the
bar is a single static line and shows only the first Message block.

**My countdown isn't showing.**
Check **Ends at** is filled in and in `YYYY-MM-DD HH:MM` form, in your
store's time zone. An empty or unparseable date shows nothing at all rather
than a broken timer. If the date has passed, **When it ends** decides whether
the section disappears or shows the "sale has ended" message.

**My popup isn't showing.**
Check, in order: (1) **Disable this popup** is unticked in the **Promotional
popup** section, in the **Footer** group; (2) you are not on the cart page or
an account page, where it never shows; (3) you have not already seen it. The
popup shows once per browser, then waits for the number of days in **Show
again after**. Open your store in a private window to see it again.

**The gift wrapping option is missing from the cart.**
Check that **Offer gift wrapping** is ticked. If you chose a gift wrap
product, the option is hidden while that product cannot be bought: the product is sold out or not available on your online store. Open the
product in Shopify admin, set it to **Active**, and either turn inventory
tracking off or tick **Continue selling when out of stock**. See
[Gift wrapping](#gift-wrapping).

**My product doesn't show as a pre-order.**
All three conditions have to be true for the variant: Shopify tracks its
inventory, the quantity is zero or less, and **Continue selling when out of
stock** is ticked. A variant that does not track inventory is never a
pre-order. Also check **Sell out-of-stock variants as pre-orders** is on in
the **Buy buttons** block. See [Pre-order](#pre-order).

**My pre-order ship date isn't showing.**
Check the metafield is `custom.preorder_ship_date`, its type is **Date**, and
the date is today or later. A date in the past is ignored.

**The breadcrumb on a product page doesn't show a collection.**
The collection shows only when the shopper reached the product through a
collection page. From search, the home page or a direct link, the trail is
"Home" and the product name.

**The product grid looks empty.**
Check, in order: (1) the collection actually has products assigned to it —
open the collection in **Products → Collections**; (2) the products in it
are set to **Active**, not Draft — draft products never appear on the
storefront; (3) if you've applied filters (availability, price, type,
vendor, size, etc.) on the collection page itself, click **Clear all** — an
overly narrow filter combination can legitimately return zero results, and
the theme shows a "No products match these filters" message with a clear
button in that case, which is different from an actually-empty collection.

**My images look stretched.**
This usually means an image is being forced into a ratio it wasn't shot for.
Check the relevant setting — **Theme settings → Product cards → Image
shape**, or a section's own **Image shape** setting (Hero,
Image with text, Visit us, How it's made, Collection list tiles) — and
either pick **Adapt to image** where that option exists (shows the image at
its natural ratio, no cropping) or re-crop/replace the source image so its
proportions roughly match the ratio you've chosen (square, portrait, arch,
landscape). Very small source images stretched up to fill a large section
will also look soft — use images at least as large as the space they'll fill.

**The home screen icon on my iPhone is a screenshot of my store.**
That is what iOS does when no home screen icon is set. Upload one under
**Theme settings → Branding → Home screen icon (iOS)** — square, at least
180×180, solid background. See section 4.
