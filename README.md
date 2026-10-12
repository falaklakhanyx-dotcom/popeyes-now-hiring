# Popeyes Now Hiring

Hiring portal for CSM's Popeyes restaurants. Applicants scan the QR flyer, enter a ZIP code, city, or county, and see the nearest restaurants with Apply buttons that open the job application pre-filled with the store number and position.

**Live site:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/
**Printable flyer:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/flyer.html

## Files

| File | What it is |
| --- | --- |
| `index.html` | The portal page (the QR code's destination) |
| `flyer.html` | Letter-size "Now Hiring" flyer with the QR code. Open it and use **Print flyer**. |
| `geo.json` | ZIP / city / county coordinates used for the "closest to you" search |

## Updating stores or roles

Everything is in the `<script>` block of `index.html`:

- `STORES`: one row per restaurant: `[market, store #, street, city, state, zip, phone, email, lat, lng]`
- `DEFAULT_JOBS`: roles shown at every store (`minAge: 18` adds the age check)
- `FORM_URL`: the job application form the Apply buttons open

Edit the file on GitHub (pencil icon) and commit; the live site updates within a minute or two.
