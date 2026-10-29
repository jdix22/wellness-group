# The Wellness Group Aurora: website redesign

A one-page redesign for [The Wellness Group Aurora](https://www.thewellnessgroupaurora.com/), a multidisciplinary clinic at 15620 Bayview Avenue, Aurora (chiropractic, massage therapy, physiotherapy, pelvic floor physio, chiropody, acupuncture, TCM, naturopathic medicine and more). It's plain HTML, CSS and JavaScript with no build step, so it runs on GitHub Pages as-is.

Live preview: https://jdix22.github.io/wellness-group/

## Highlights
- **Before/after "tension map" slider** in the hero. Drag it (or use the arrow keys) and the pain hotspots on the "before" side turn into the treatment that addresses them on the "after" side. It plays a short sweep the first time it scrolls into view.
- **Services by category** (hands-on care, injury & rehab, foot care, integrative & natural, therapeutic technology). Every service opens a detail panel with the full description, conditions treated, **treatments & rates** and its practitioners.
- **Jane booking everywhere**: each service, treatment row and practitioner deep-links to the right page on `thewellnessgroupaurora.janeapp.com`.
- **"Not sure where to start?" finder**: pick a concern (back pain, headaches, foot pain, pelvic health…) and get the matching services.
- **Team of 20** with filters, photos and full bios (each with a "Book with…" button).
- Billing, direct billing, veterans coverage, Three Best Rated awards, hours with a live "open now" status, map, contact form, FAQ and clinic policies.
- Shareable deep links: `#service/massage`, `#team/17`.

## Updating content
All service and team content lives in the `<script>` near the bottom of `index.html`:
- `TEAM`: one entry per practitioner. `id` is their **Jane staff member id** (used for the photo `assets/img/team/<id>.jpg` and the booking link `#/staff_member/<id>`).
- `S`: one entry per service. `disc` is the Jane discipline id; each `rates` row is `[name, note, duration, price, "discipline/<id>/treatment/<id>"]`.
- Rates were copied from the clinic's public Jane booking page on 2026-10-29 and should be re-checked before launch.

Jane link formats: `…janeapp.com/#/discipline/1`, `#/staff_member/17`, `#/discipline/8/treatment/132`.

## Notes
- The contact form opens the visitor's email app addressed to reception@thewellnessgroupaurora.com. To send without an email app, point it at a form service such as Formspree.
- The blog cards link to the existing posts on thewellnessgroupaurora.com. Move or update those links if the old Wix site is retired.
- Team headshots come from the clinic's own Jane profiles. Service and slider photos are from [Unsplash](https://unsplash.com) (free to use) and are stored in `assets/img/`. The before/after image is illustrative.

Website designed by [jdix.ca](https://jdix.ca).
