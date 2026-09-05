# SkinPlasty Clinic — website

Static single-page site for **SkinPlasty Clinic, Noida** (Dr. Ankur Lal, MBBS, MD Dermatology — Gold Medalist, AIIMS New Delhi).

No build step, no dependencies. One `index.html` with inline CSS and JS.

## Deploy on Vercel

1. Push this folder to a GitHub repo.
2. In Vercel → **Add New → Project** → import the repo.
3. Framework preset: **Other**. Build command: leave empty. Output directory: leave empty (root).
4. Deploy.

Or from the terminal:

```bash
npm i -g vercel
vercel --prod
```

## What's in here

| File | Purpose |
|---|---|
| `index.html` | The whole site |
| `vercel.json` | Clean URLs + basic security headers |
| `robots.txt` / `sitemap.xml` | SEO basics |

## How the booking form works

There is no backend. On submit, the form validates the name and phone, then opens
WhatsApp (`wa.me/919971696703`) with the enquiry pre-filled. Nothing is lost and
nothing needs hosting.

To switch to email/CRM delivery later, replace the submit handler at the bottom of
`index.html` with a POST to Formspree, Web3Forms, or a Vercel serverless function.

## Things to swap before going live

- **Photos.** Images currently point at assets on the existing `skinplasty.in` server
  and hide themselves if they fail to load. Replace with real photos of Dr. Lal, the
  clinic interior, and before/after cases in `/images` and update the `src` attributes.
- **Consultation fee.** Not stated anywhere on the current site, so the FAQ says to call.
  Add the number once confirmed.
- **Reviews.** Excerpts are from the clinic's live Google Business listings. Confirm
  wording with the clinic, or swap in a live Google reviews widget.
- **Rating figures.** 4.9 / 175 reviews (Sector 122) and 218 reviews across all three
  listings, as of September 2026. Refresh before launch.
- **Before/after gallery.** Worth adding — this is the highest-converting section for a
  hair transplant practice, and the current site has no real gallery.

## Contact details used

- Sector 122, Noida (main) — +91 99716 96703
- SJM Hospital, Sector 63, Noida — +91 95321 36942
- Swastham Medicare, Greater Noida West — +91 97603 36942
- skinplasty@gmail.com
