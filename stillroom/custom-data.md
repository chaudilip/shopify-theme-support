# Custom data: nutrition, ingredients, dietary badges, and more

Stillroom's food-specific features — the nutrition panel, ingredients list,
dietary badges, allergen notice, storage info, origin note, delivery
estimate, the pre-order ship date, and the recipe feature — are all powered
by **custom data** you add in Shopify admin. This guide explains what that is, why the theme needs you
to set it up, and exactly how to do it.

**Read this before you conclude anything is broken.** A brand-new install of
Stillroom shows none of these panels, and that is correct, expected behavior —
not a bug. Every single one of these blocks is written to render nothing at
all when it has no data connected, specifically so a store that doesn't sell
food, or hasn't entered this data yet, still gets a clean, normal-looking
product page instead of a page full of empty boxes. Nothing is broken. You
turn each one on by connecting data to it, at your own pace, one product (or
all of them, via a CSV/API import) at a time.

The companion guide **Setting up Stillroom** covers everything else: sections,
colors, fonts, menus and the product page block list.

## Contents

1. [What is a metafield?](#1-what-is-a-metafield)
2. [The theme works without any of this](#2-the-theme-works-without-any-of-this)
3. [The ten metafields Stillroom reads](#3-the-ten-metafields-stillroom-reads)
4. [Creating a metafield definition](#4-creating-a-metafield-definition)
5. [Binding a metafield to a block with dynamic source](#5-binding-a-metafield-to-a-block-with-dynamic-source)
6. [Dietary badges: two features, two metafields](#6-dietary-badges-two-features-two-metafields)
7. [Care symbols (no custom data needed)](#7-care-symbols-no-custom-data-needed)
8. [The recipe feature](#8-the-recipe-feature)
9. [Worked example: one product, start to finish](#9-worked-example-one-product-start-to-finish)
10. [Notes for developers](#10-notes-for-developers)

---

## 1. What is a metafield?

**A metafield** is one extra piece of data you attach to something Shopify
already has, like a product — a field Shopify's product form doesn't offer
by default. Shopify's built-in product fields are title, price, description,
and so on; a metafield is how you add "ingredients," "storage instructions,"
or "country of origin" as real, structured data on that same product,
instead of just typing it into the description as plain text.

Every metafield has three things you need to get right, and the theme names
all three for you in the editor:

- a **namespace** — a grouping name. All of Stillroom's are `custom`, which is
  what Shopify assigns by default.
- a **key** — the field's own name, like `ingredients`.
- a **type** — Rich text, Single line text, and so on.

You may also see **metaobjects** mentioned in Shopify's admin. A metaobject
is a custom record type you design yourself. **Stillroom's product blocks do not
read metaobjects** — every one of them reads a plain product metafield. There
is one optional exception for product-card badges, covered in
[section 6](#6-dietary-badges-two-features-two-metafields).

## 2. The theme works without any of this

Worth repeating on its own: install Stillroom, publish it, and your store works
completely normally with zero custom data set up. Every block this guide
covers checks whether it has data before rendering anything, and quietly
renders nothing if it doesn't. You can set this up for one flagship product
today and leave the rest for later — nothing else on the site depends on it.

## 3. The ten metafields Stillroom reads

These are the exact definitions the theme's own help text names, inside the
theme editor, on each block. **Create them with these namespaces, keys and
types and everything lines up on the first try.** All ten are on
**Products**, and all ten use the namespace `custom`.

| Key | Type | Feeds | Example |
|---|---|---|---|
| `ingredients` | Rich text | Ingredients block | A list, or a paragraph |
| `allergen_notice` | Rich text | Allergen notice block | "Contains tree nuts. Packed in a kitchen that handles wheat." |
| `nutrition_facts` | Rich text | Nutrition panel block | A nutrition table built in the rich text editor |
| `storage_instructions` | Rich text | Storage info block | "Keep in the fridge once opened." |
| `shelf_life` | Single line text | Storage info block | `Best within 6 months, unopened` |
| `origin` | Single line text | Origin block | `Sonoma County, California` |
| `delivery_estimate` | Single line text | Delivery estimate block | `Arrives in 3–5 business days` |
| `dietary_tags` | List of single line text | Badges on **product cards** | `Vegan`, `Gluten-free` |
| `dietary_badges` | Single line text | Dietary badges block on the **product page** | `Vegan, Gluten-free, Non-GMO` |
| `preorder_ship_date` | Date | Pre-order note on the Buy buttons block and on product cards | 3 March 2027 |

The two dietary rows are not a duplication — see
[section 6](#6-dietary-badges-two-features-two-metafields).

`preorder_ship_date` is optional, and it is the one metafield in this table
you do not connect to a block. The theme reads it directly. It is used only
on products sold as a pre-order, and a date that has passed is ignored. The
**Setting up Stillroom** guide covers pre-orders in full, under "Pre-order".

You do not have to create all ten, and you do not have to create any of them
in a particular order. Create the ones you'll use; each block stays invisible
until its own data arrives.

### Nutrition facts is a rich text metafield, not a metaobject

Nutrition is the one that most often gets set up the hard way, so it is worth
stating plainly. The **Nutrition panel** block has exactly one content field,
"Nutrition facts," and it is a **rich text** field. It prints whatever is
connected to it. So:

- Create `custom.nutrition_facts` as a **Rich text** product metafield.
- Build the nutrition table for each product in Shopify's rich text editor,
  the same way you'd write any other formatted content.
- Connect the block to it once (section 5) and every product that has the
  field filled in shows a panel.

A metaobject cannot be connected here. Shopify's dynamic-source picker binds
a rich text setting to a single rich text value, and it has no way to loop
over a structured record — so a "nutrition facts" metaobject with nutrient
rows inside it would have nothing on the page able to read it. If you need
nutrition stored as structured, machine-readable rows for some other reason,
see [section 10](#10-notes-for-developers).

The block also has a **Show daily value disclaimer** checkbox, on by default,
which adds "Percent Daily Values are based on a 2,000 calorie diet." below
the panel. Turn it off if that sentence doesn't apply where you sell.

## 4. Creating a metafield definition

**Themes cannot create these definitions themselves** — only a merchant
(via admin) or an app can. That's a Shopify platform limitation, not
something specific to Stillroom, and it's exactly why this guide exists: the
theme ships ready to *display* this data the moment you connect it, but it
can't create the fields for you first.

1. In Shopify admin, go to **Settings → Custom data → Products**.
2. Click **Add definition**.
3. Give it a **Name** — the label you and your staff see in the product
   editor. It can be anything readable, e.g. "Ingredients".
4. Check the **Namespace and key** underneath. Shopify generates one from the
   name; click **Edit** if it doesn't match the table in
   [section 3](#3-the-ten-metafields-stillroom-reads). Typing "Ingredients"
   normally lands on `custom.ingredients` on its own, but confirm it rather
   than assume.
5. Choose the **Content type** — Rich text, Single line text, Date, and so
   on, per the table. For `dietary_tags`, pick Single line text and then turn on the
   **list of values** option so it becomes "List of single line text".
6. Save.

Shopify may offer a **standard definition** — a pre-named field Shopify
itself maintains — for some of these, ingredients in particular. A standard
definition is portable: other sales channels like the Shop app and some apps
read the same field. If you use one, note the namespace and key it actually
creates, because it will not be `custom`, and you will need to know it when
you connect the block in section 5 (the dynamic source picker will list it
either way) and when you fill in the two theme settings in section 6.

## 5. Binding a metafield to a block with dynamic source

This is the step most merchants get stuck on the first time — it's a small,
specific click, not a dropdown.

1. Open the theme editor: **Online Store → Themes → Customize**.
2. Navigate to a product page (use the page picker at the top of the theme
   editor, or click through from a product in the preview).
3. In the section list on the left, find the block you want to connect —
   e.g. **Ingredients**. If it isn't already on the page, click **Add
   block** first and add it. The **Setting up Stillroom** guide has the general
   add/reorder steps.
4. Click the block to open its settings panel. Under the content field you'll
   see the theme's own note naming the exact metafield that field expects —
   the same values as the table in section 3.
5. Find the field (e.g. "Ingredients"). If a metafield of a compatible type
   exists anywhere on your store, you'll see a small icon at the right edge
   of that field — it looks like a database/link plug icon, separate from the
   text input itself. Click it.
6. A picker opens showing the available metafields, grouped by resource
   (Product, in this case). Choose the one you created.
7. The field's input area now shows the connection — often a small chip or
   label indicating it's bound, rather than an editable text box. The block
   will now render that metafield's value for **every product that has one
   filled in**, and continue to render nothing for any product that doesn't.
8. Click **Save**.

Because the binding is made on the **block**, not on one individual product,
you only do this once per block, store-wide — after that, filling in the
metafield's value on each product (in the product editor, under **Metafields**
at the bottom of the product page) is all that's needed to make that
product's panel appear.

Two of the blocks also accept typed text instead of a connection, for stores
that want the same line on every product: **Dietary badges** and **Delivery
estimate**. Type into them directly and no metafield is needed at all.

## 6. Dietary badges: two features, two metafields

Dietary badges appear in two places, and the two are wired differently. This
is the single most common source of "my badges show here but not there."

### On the product page — the Dietary badges block

Uses `custom.dietary_badges`, a **Single line text** metafield holding a
**comma-separated** list:

```
Vegan, Gluten-free, Non-GMO
```

The block splits on commas and trims the spaces. Connect it with the dynamic
source picker (section 5), or just type the list into the block and skip the
metafield entirely.

### On product cards — collection grids, search results, recommendations

Uses `custom.dietary_tags`, a **List of single line text** metafield — the
badge words as separate list entries, not one comma-separated string.

Cards are generated in a loop, so there is no settings panel to click into
for each one and no dynamic source picker involved. Instead you tell the
theme where to look, once, under **Theme settings → Product cards**:

- **Dietary metafield namespace** — defaults to `custom`
- **Dietary metafield key** — defaults to `dietary_tags`

The defaults match what Shopify assigns if you create a product metafield
named simply "Dietary tags" — so for most stores, creating that one metafield
and leaving the two settings alone is all that's needed. If your metafield
ended up somewhere else, update these two settings to match rather than
renaming the metafield.

Two more things about card badges:

- **Only the first three show.** A card is small and a row of six chips
  crowds out the product name. Put the three that matter first.
- **Show dietary badges** (also under Theme settings → Product cards, on by
  default) switches them off store-wide regardless of your data.

**If you only want to set up one of the two,** set up `dietary_tags` for the
cards — it is the one shoppers see while browsing — and type the list into
the product-page block by hand.

## 7. Care symbols (no custom data needed)

The **Storage info** block also carries **care symbols** — drawn marks for
how a product should be kept. These are the one part of this guide that needs
**no metafield and no setup**: they are plain checkboxes in the theme editor.

Clothing has had a care-symbol language since the 1960s, because handling rules
get glanced at rather than read. Food has never had one, so a jar ends up
explaining "shake before use, store upright, refrigerate once opened" in a
sentence most shoppers skim past.

Open the **Storage info** block on a product and tick the ones that apply:

| Symbol | Means |
|---|---|
| Keep sealed | Reseal after each use |
| Cool, dark place | Away from direct light and heat |
| Chill once opened | Refrigerate after opening |
| Don't refrigerate | Cold will spoil or cloud it — common for olive oil and honey |
| Store upright | Don't lay it on its side |
| Shake before use | It settles or separates — dressings, unfiltered oils |

Tick only what's true. Six symbols on every product teaches a shopper to ignore
all six; two teaches them to read them.

Each symbol always appears **with its wording underneath**, so nothing depends
on recognising the mark — it works the first time someone sees it, and on a
screen reader.

Because the symbols are settings rather than data, they are set per block,
not per product. Ticking "Chill once opened" on the product page's Storage
info block applies it to every product that page renders. If your range needs
genuinely different symbols product by product, put the difference in the
`storage_instructions` text instead, or use a separate product template for
the products that differ.

Ticking any symbol makes the Storage info panel appear even with no text
connected to it.

## 8. The recipe feature

The **Recipe feature** section shows one recipe card, and it is built around
a **blog article**, not a metaobject.

Add a **Recipe feature** block and pick an **Article**. Every other field
in the block — **Title override**, **Image override**, **Description**,
**Prep time**, **Cook time**, **Servings**, **Level**, **Dietary note**,
**Ingredients**, **Method** — is either typed directly or connected by
dynamic source **to a metafield on that article**. Any field left blank is
hidden.

- **Simplest, recommended:** write the recipe as a blog post and type the
  prep time, cook time, servings and the rest straight into the block's own
  fields. No metafields at all.
- **If you want the recipe data structured and reusable:** create those
  fields as metafields on **Articles** (Settings → Custom data → Articles)
  and connect them with the dynamic source picker, exactly as in section 5.
  Article metafields are what these fields read; a recipe metaobject has
  nothing here able to read it.

**Shopping from a recipe is not part of this theme.** The Recipe feature
section has no product list and does not cross-sell products from a recipe.
If you want shoppable links near a recipe, put a **Featured collection**
section next to it, or write a Custom Liquid block against your own
product-reference metafield.

## 9. Worked example: one product, start to finish

Setting up **nutrition, ingredients, and two dietary badges** on a single
product, "Chilli Honey."

1. **Create three metafield definitions** (Settings → Custom data → Products
   → Add definition, once each). Confirm the namespace and key on each one
   before saving:
   - "Nutrition facts" — **Rich text**, `custom.nutrition_facts`
   - "Ingredients" — **Rich text**, `custom.ingredients`
   - "Dietary tags" — **List of single line text**, `custom.dietary_tags`
2. **Fill in the product.** Open Chilli Honey in **Products**, scroll to
   **Metafields** at the bottom, and: build your nutrition table in the
   "Nutrition facts" rich text field; write the ingredients list into
   "Ingredients"; under "Dietary tags," add two list entries, `Vegan` and
   `Gluten-free`. Save the product.
3. **Connect the two blocks, once, store-wide.** In the theme editor, go to
   this (or any) product page, open the **Nutrition panel** block and connect
   its "Nutrition facts" field to the metafield you made, via the
   dynamic-source icon (section 5). Do the same for the **Ingredients**
   block.
4. **Check the card-badge theme settings.** Under **Theme settings → Product
   cards**, confirm **Dietary metafield namespace** is `custom` and
   **Dietary metafield key** is `dietary_tags`. Those are the shipped
   defaults, so if you left the metafield on its auto-generated namespace and
   key there is nothing to change. No dynamic-source connection is needed for
   this one — the card reads it directly once the namespace and key line up.
5. **Publish and check.** View Chilli Honey's product page: the Nutrition
   panel and Ingredients panel now show your content. View it in a collection
   grid: the "Vegan" and "Gluten-free" chips now show on its card, provided
   **Show dietary badges** is on.
6. Every other product without this data set up continues to show no
   nutrition panel, no ingredients panel, and no card badges — exactly as
   intended.

## 10. Notes for developers

Two things in this guide have a developer-only path behind them. Neither is
needed for a normal setup.

**Structured nutrition data.** If you need nutrition stored as rows a machine
can read — for an app, a POS integration, a future custom storefront —
build whatever metaobject shape suits you and render it with a **Custom
Liquid** block on the product page, reading
`product.metafields[namespace][key].value` and looping in Liquid. That is the
only route that can iterate a list; the dynamic-source picker resolves one
value at a time and cannot. The theme ships no built-in labels for "Serving
size," "Calories" or "% Daily Value", so write those into your Liquid or into
the entries themselves. This is instead of `custom.nutrition_facts`, not
alongside it.

**Metaobject-backed card badges.** The product card accepts either shape at
the namespace and key you configure: a plain list of single line text (what
this guide recommends), or a **list of metaobject references** whose entries
each carry a field with the key `label`. The second is worth it only if you
want each badge defined once and reused — with its own icon field, say —
across many products. The card reads `label` and nothing else.

**One Shopify platform rule sits behind both.** A Theme Store theme is not
allowed to offer a setting that picks a custom metaobject: the `metaobject`
and `metaobject_list` setting types are reserved for Shopify-defined standard
metaobjects. So a custom metaobject can never be the subject of a picker in
the theme editor, and reaching one always means Liquid you write yourself.
