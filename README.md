# RN Life Science — website

A complete single-page website for Raj Nandani Life Science Private Limited.
No build step, no frameworks, no npm. Open `index.html` and it runs.

```
index.html          the whole website
assets/             logo files (extracted from your FESUBEST artwork)
images/             product photos — the only folder you normally touch
```

---

## 1. Before you go live — set your email address

Enquiries are delivered by FormSubmit.co. Open `index.html`, and near the start
of the `<script>` block you will find:

```js
const CONFIG = {
  formsubmitEmail: "info@rnlifesciences.in",
  whatsapp: "918240028656"
};
```

Change `formsubmitEmail` to the inbox that should receive enquiries. That single
line also updates the email shown in the contact panel and the footer, so there
is nothing else to edit.

**Activation:** the very first time someone submits the form, FormSubmit sends a
one-time confirmation email to that address. Click the link inside it once and
the form works permanently from then on. Until you do, submissions will not
arrive — so send one test enquiry yourself and confirm it.

---

## 2. Replacing the product photos

Every photo on the site is an ordinary file in the `images` folder. **To change a
photo, save your own image over the file of the same name.** Nothing in the code
needs to change.

| File | Where it appears |
| --- | --- |
| `hero.png` | Large image on the opening screen |
| `fesubest.png` | FESUBEST — card and product page |
| `fesubest-pack.png` | FESUBEST — second gallery view |
| `fesubest-detail.png` | FESUBEST — third gallery view |
| `naturerise-d3.png` | NatureRise-D3 — card and product page |
| `naturerise-d3-pack.png` | NatureRise-D3 — second gallery view |
| `naturerise-d3-detail.png` | NatureRise-D3 — third gallery view |
| `vita-co-gold.png` | VITA CO-GOLD — card and product page |
| `vita-co-gold-pack.png` | VITA CO-GOLD — second gallery view |
| `vita-co-gold-detail.png` | VITA CO-GOLD — third gallery view |
| `rn-calci-forte.png` | RN-CALCI FORTE — card and product page |
| `rn-calci-forte-pack.png` | RN-CALCI FORTE — second gallery view |
| `rn-calci-forte-detail.png` | RN-CALCI FORTE — third gallery view |
| `rn-omega-1000.png` | RN-OMEGA 1000 — card and product page |
| `rn-omega-1000-pack.png` | RN-OMEGA 1000 — second gallery view |
| `rn-omega-1000-detail.png` | RN-OMEGA 1000 — third gallery view |
| `about-lab.png` | Spare slot for a facility photo |
| `review-1.png` | Reviewer photo |

Three rules, and that is all:

1. **Keep the file name and the `.png` ending exactly as they are.** A photo saved
   as `Fesubest.PNG` or `fesubest.jpg` will not be picked up.
2. **Use a square image**, around 1200 × 1200 pixels. Anything roughly square works.
3. **Keep each file under about 500 KB** so pages load quickly.

Every file currently holds a labelled placeholder that names itself on screen, so
you can always see which slot is which. If a file is ever missing or misspelt, the
page draws its own placeholder rather than showing a broken image — the site will
never look broken to a visitor.

---

## 3. Changing the logo

`assets/rn-logo.png` is your logo, extracted from the FESUBEST artwork at
1773 × 1436 with a transparent background. Overwrite it with the same file name to
change it. A compressed copy is also embedded inside `index.html` as a safety net,
so the opening screen shows the mark even if the assets folder is ever lost.

---

## 4. Putting it online

Upload the whole folder — `index.html`, `assets` and `images` together — to your
web host's public directory (often called `public_html` or `www`). It will also
work as-is on Netlify, Vercel, Cloudflare Pages or GitHub Pages: drag the folder in.

The form needs a real web address to work, so test it after uploading rather than
by double-clicking the file on your computer.

---

## 5. Two things to confirm before launch

**The FESUBEST dose.** Your two source documents disagree. The leaflet says *4
puffs for adults, 2 for children*; the product information document says *3–5
years: 1 spray, 6–8 years: 2, 9–12 years: 4, 13+ years: 8*. The dose calculator
currently follows the product information document. Please confirm which is
correct — it is in the `PRODUCTS` list under `calc.options` for `fesubest`.

**The absorption figures.** The bar chart in your leaflet has no printed numbers,
so the values used (93% spray down to 18% pills) were read off the graphic. They
are described on the site as the manufacturer's comparative positioning rather
than clinical data. If you hold the real figures, they are in the `ROUTES` list.

---

## 6. Editing the text

All product content lives in one place: the `PRODUCTS` list inside the `<script>`
block. Each product has its name, description, composition table, benefits, usage
notes and safety notes together in one block. Editing the text there updates the
product card, the product page, the enquiry dropdown and the brand carousel at
once — you never have to change the same wording twice.
