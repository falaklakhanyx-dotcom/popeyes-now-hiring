# Popeyes Now Hiring

Hiring portal for CSM's Popeyes restaurants. Applicants scan the QR flyer, enter a ZIP code, city, or county (or tap **Use my location**), and see the nearest restaurants. Each Apply button asks English or Español, then opens the job application pre-filled with the store number and position.

**Live site:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/
**Printable flyer:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/flyer.html

## Files

| File | What it is |
| --- | --- |
| `index.html` | The portal page (the QR code's destination) |
| `flyer.html` | Letter-size "Now Hiring" flyer with the QR code. Open it and use **Print flyer**. |
| `geo.json` | ZIP / city / county coordinates used for the "closest to you" search |
| `urgent.txt` | Stores that need help sooner. Each store listed gets an "Urgently hiring" badge and shows first. Edit it on GitHub with the pencil icon, even from a phone. |

## Updating stores or roles

Everything is in the `<script>` block of `index.html`:

- `STORES`: one row per restaurant: `[market, store #, street, city, state, zip, phone, email, lat, lng]`
- `DEFAULT_JOBS`: roles shown at every store (`minAge: 18` adds the age check)
- `FORM_URL`: the job application form the Apply buttons open
- `FORM_URL_ES` / `FORM_LANG_ES`: where the Español button goes. By default it's the same form with its Spanish translation (Forms → Settings → Multilingual → Español (México))

Edit the file on GitHub (pencil icon) and commit; the live site updates within a minute or two.
