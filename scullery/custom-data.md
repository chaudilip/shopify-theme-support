# Custom data: tasting notes, particulars, nutrition and recipes

Scullery 2.0 draws every product as a catalogue **entry**: a number, a
family, a name, tasting notes, particulars and a price. Most of that comes
straight from Shopify. The food-specific parts (tasting notes, origin,
maker, ingredients, nutrition, allergens, storage, companions, pre-order
dates) come from **metafields** you add in Shopify admin. Recipes link to
products through **tags**, with no metafield at all.

**Nothing here is required.** A fresh install shows none of these details,
and that is correct. Every block and every line on an entry checks for data
first and prints nothing when there is none: no empty panel, no placeholder
text. Add data for one product today and the rest later.

The companion guide **Setting up Scullery** covers sections, settings and
the product page block list.

## Contents

1. [What is a metafield?](#1-what-is-a-metafield)
2. [Two kinds of metafield in Scullery](#2-two-kinds-of-metafield-in-scullery)
3. [Pantry data: read automatically](#3-pantry-data-read-automatically)
4. [Product page panels: connected in the editor](#4-product-page-panels-connected-in-the-editor)
5. [Creating a metafield definition](#5-creating-a-metafield-definition)
6. [Connecting a metafield to a block](#6-connecting-a-metafield-to-a-block)
7. [Care symbols (no custom data needed)](#7-care-symbols-no-custom-data-needed)
8. [Recipes and products](#8-recipes-and-products)
9. [Worked example](#9-worked-example)
10. [Notes for developers](#10-notes-for-developers)

---

## 1. What is a metafield?

A metafield is an extra field on a Shopify object, such as a product. You
create a **definition** once (name, namespace, key, type) under **Settings →
Custom data → Products**, and from then on every product's admin page shows
that field in its **Metafields** card, ready to fill in.

Themes cannot create definitions themselves; you create them once, and the
theme reads them.

## 2. Two kinds of metafield in Scullery

| Kind | How the theme finds it | Namespace |
|---|---|---|
| **Pantry data** (section 3) | Read automatically, by key, wherever the product appears | Set under **Theme settings → Product entries → Metafield namespace**, default `custom` |
| **Panels** (section 4) | You connect the metafield to a block in the theme editor | Any; the help text suggests `custom` |

## 3. Pantry data: read automatically

Create these product metafields in the namespace set under **Theme settings
→ Product entries** (default `custom`) and the theme uses them without any
further setup. All are optional.

| Key | Type | Where it shows | Example |
|---|---|---|---|
| `statement` | Single line text | Statement block, Pantry index rows, Shelf reel, Kitchen steps, quick view | `Picual olives from one grove, pressed within hours.` |
| `flavour` | List of single line text (or one line) | Tasting notes on entries and the Tasting notes block | `Grassy`, `Peppery`, `Bitter almond` |
| `size` | Single line text | Entries (falls back to the variant title) and Particulars | `500 ml` |
| `origin` | Single line text | Particulars; entry hover; the feature entry | `Jaén, Andalusia` |
| `maker` | Single line text | Particulars; the feature entry | `The Ortega family` |
| `process` | Single line text | Particulars; entry hover | `Cold pressed` |
| `season` | Single line text | Particulars | `Harvest 2026` |
| `batch` | Single line text | Particulars | `No. 14` |
| `use` | Single line text | Particulars | `Finishing, dressings` |
| `pairings` | List of product references | **Companions** section on the product page | Two or three products |
| `preorder_ship_date` | Date | Pre-order note on the Buy buttons block | 3 March 2027 |

Notes:

- **Particulars** prints the terms in this order: origin, maker, process,
  season, use, size, batch. A term with no value is left out; a product with
  none prints nothing.
- **Reveal origin and process on hover** (Theme settings → Product entries)
  shows those two on shelf entries for pointer devices.
- **Companions** without `pairings` falls back to Shopify's complementary,
  then related, product recommendations.
- **`preorder_ship_date`** is used only on variants sold as a pre-order (see
  *Pre-order* in the setup guide). A date that has passed is ignored and the
  block's own shipping note is shown instead.
- If you change the namespace setting, every key above must live in that
  namespace.

## 4. Product page panels: connected in the editor

These blocks sit in the product page's **Details** and **Margin** groups.
Each has a field you either type into or connect to a metafield with the
**Connect dynamic source** button. The editor's help text on each block
names the suggested definition:

| Block | Field | Suggested key (namespace `custom`) | Type |
|---|---|---|---|
| Ingredients | Ingredients | `ingredients` | Rich text |
| Nutrition panel | Nutrition facts | `nutrition_facts` | Rich text |
| Allergen notice | Allergen notice | `allergen_notice` | Rich text |
| Storage info | Storage instructions | `storage_instructions` | Rich text |
| Storage info | Shelf life | `shelf_life` | Single line text |
| Origin | Origin | `origin` | Single line text |
| Delivery estimate | Delivery estimate | `delivery_estimate` | Single line text |
| Dietary badges | Dietary tags | `dietary_badges` | Single line text, comma separated |

The **Origin** block can use the same `origin` metafield as Particulars.
Dietary badges prints each comma-separated value as a stamp
(`Vegan, Gluten free`).

**Nutrition is a rich text metafield, not a metaobject.** Build the table
for each product in the rich text editor; the block prints what is
connected. **Show reference intake note** adds "Reference intakes are for an
average adult (8,400 kJ / 2,000 kcal)." beneath it.

Rich text panels (Ingredients, Nutrition, Allergen, Storage) open like
drawers; each has **Open when the page loads**.

> **Upgrading from 1.x?** The `dietary_tags` list metafield and the product
> card dietary badges it fed are not used in 2.0. Your data stays on the
> products; `dietary_badges` still feeds the Dietary badges block.

## 5. Creating a metafield definition

1. Shopify admin → **Settings → Custom data → Products → Add definition**.
2. **Name**: anything readable, e.g. "Tasting notes".
3. **Namespace and key**: type it as `custom.flavour` (namespace, a dot,
   key). It must match the tables above exactly, in lower case.
4. **Type**: as in the tables. For `flavour` choose *Single line text* and
   **List of values**; for `pairings` choose *Product* and **List of values**.
5. Save. Open any product: the field is in its **Metafields** card.

To fill many products at once, use a product CSV import or a bulk editor.

## 6. Connecting a metafield to a block

Only needed for the panels in section 4.

1. Open **Online Store → Themes → Customize** and switch to a product
   template.
2. In the left sidebar open **Main product → Details** (or **Margin**) and
   select the block, e.g. **Ingredients**.
3. Next to the field click **Connect dynamic source** and choose the
   metafield, e.g. *Ingredients*.
4. Save. Every product that uses this template and has the field filled
   shows the row; the others leave it out.

## 7. Care symbols (no custom data needed)

The **Storage info** block has six checkboxes: *Keep sealed*, *Cool, dark
place*, *Chill once opened*, *Don't refrigerate*, *Store upright* and *Shake
before use*. Each one prints a small symbol with its label. They apply to
every product on that template, so for products that need different
symbols, make a second product template.

## 8. Recipes and products

Recipes and products link both ways through article **tags**, with no app.

1. Under **Theme settings → Product entries → Recipes blog**, choose the
   blog that holds your recipes.
2. On each recipe, add one tag per product it uses, written exactly as that
   product's **handle**: the last part of its address.
   `/products/chilli-oil` → tag `chilli-oil`.

What happens:

- The recipe page shows **From the pantry**: the tagged products with add
  buttons (up to 8; the first 20 handle-shaped tags are checked).
- The product page's **In the kitchen** section shows up to three recipes
  tagged with its handle, from the newest 50 articles in the recipes blog.
- **Kitchen steps** and **Recipe and its pantry** sections list the same
  products; Kitchen steps builds one step per product if you add no steps.
- An article in any other blog is a **field note**; product-handle tags list
  the products as "Mentioned in this note".

Optional recipe facts: create **article** metafields `serves` and `time`
(single line text) in the same namespace. They print above the products, for
example *Serves 4* and *40 minutes* (write `4` in `serves`; the theme adds
"Serves").

Tags that are not product handles ("Supper", "Slow cooking") remain ordinary
tags and appear in the blog's tag index.

## 9. Worked example

Chilli oil, handle `chilli-oil`:

1. Definitions (once): `custom.statement`, `custom.flavour` (list),
   `custom.origin`, `custom.process`, `custom.size`, `custom.ingredients`
   (rich text), `custom.allergen_notice` (rich text).
2. On the product: statement *Dorset chillies, fried slowly in rapeseed
   oil.*; flavour *Smoky*, *Bright*, *Hot*; origin *Dorset*; process
   *Slow fried*; size *200 ml*; ingredients and allergen notice.
3. In the editor, connect **Ingredients** and **Allergen notice** in
   **Main product → Details**.
4. Tag a recipe in the recipes blog `chilli-oil`.

The entry now shows *Smoky / Bright / Hot* and *200 ml* on every shelf; the
product page shows the statement, a Particulars list (Origin, Process,
Size), two detail rows, and the recipe under **In the kitchen**.

## 10. Notes for developers

- Pantry data is read as `product.metafields[ns].<key>.value`, with `ns`
  from `settings.data_namespace` (default `custom`). See
  `snippets/specimen.liquid`, `snippets/particulars.liquid`,
  `blocks/statement.liquid`, `blocks/tasting-notes.liquid`,
  `sections/companions.liquid` and `blocks/buy-buttons.liquid`.
- Recipe → products: `snippets/pantry-products.liquid` resolves each
  handle-shaped tag with `all_products[tag]` (Shopify allows 20 such
  look-ups per page). Product → recipes: `sections/product-recipes.liquid`
  loops `settings.recipe_blog.articles` (limit 50) and keeps those whose
  tags contain `product.handle`.
- Panel blocks use ordinary settings that accept dynamic sources, so any
  namespace and key works if you connect it yourself.
