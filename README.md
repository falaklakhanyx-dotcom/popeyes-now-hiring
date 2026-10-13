# CSM Careers – Popeyes Now Hiring

Hiring portal for CSM's Popeyes restaurants, branded **CSM Careers**. Applicants scan the QR flyer, enter a ZIP code, city, or county (or tap **Use my location**), and see the nearest restaurants. Each Apply button asks English or Español, then opens the job application pre-filled with the store number and position.

The whole page also has an **English | Español** switch at the top. Phones set to Spanish open in Spanish automatically, and a link ending in `?lang=es` always opens in Spanish (handy for a Spanish flyer). In Spanish, Apply goes straight to the Spanish form.

**Live site:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/
**Printable flyer:** https://falaklakhanyx-dotcom.github.io/popeyes-now-hiring/flyer.html

## What's on the page

- **Search:** ZIP, city, or county, or **Use my location**. Results sort by distance; the closest store is tagged.
- **Why work with us:** Weekly Pay · Flexible Schedules · Free Meal For Employees · Paid Training · Promotion Opportunities · Monthly Management Bonuses · Employee Discounts
- **Open roles at every store:**

  | Role | Type | Age |
  | --- | --- | --- |
  | Team Member | Full & part-time | 16+ |
  | Cook | Full & part-time | 18+ |
  | Shift Leader / AM | Full-time | 18+ |
  | General Manager | Full-time | 18+ |

  18+ roles ask "Are you 18 or older?" before opening the form, and anyone who answers no is pointed to Team Member.
- **The CSM Circle:** "Ask a Team Member About The CSM Circle! Eligible team members can earn $50,000."
- **Grow your career:** Team Member → Shift Leader / AM → GM → DM → MM
- No store count is shown anywhere (header, market buttons, or results).

## Files

| File | What it is |
| --- | --- |
| `index.html` | The portal page (the QR code's destination) |
| `flyer.html` | Letter-size "Now Hiring" flyer: benefits, The CSM Circle, career path, and the QR code to the live site. Open it and use **Print flyer**. |
| `geo.json` | ZIP / city / county coordinates used for the "closest to you" search |
| `urgent.txt` | Stores that need help sooner. Each store listed gets an "Urgently hiring" badge and shows first. Edit it on GitHub with the pencil icon, even from a phone. |

## Updating stores or roles

These are in the `<script>` block of `index.html`:

- `STORES`: one row per restaurant: `[market, store #, street, city, state, zip, phone, email, lat, lng]`
- `DEFAULT_JOBS`: roles shown at every store. `title` is the Position name sent to the form and must match the form's choice exactly; `label` is an optional shorter name shown on the page; `minAge: 18` adds the age check.
- `JOB_ES` / `TYPE_ES`: Spanish names for each role and job type
- `FORM_URL`: the job application form the Apply buttons open
- `FORM_URL_ES` / `FORM_LANG_ES`: where the Español button goes. By default it's the same form with its Spanish translation (Forms → Settings → Multilingual → Español (México))

## Updating page text (benefits, The CSM Circle, career path)

Every label on the page lives in `STR` in `index.html`, once in English (`en`) and once in Spanish (`es`). Change both so the two languages match:

- Benefits: `perkPay`, `perkSchedule`, `perkMeal`, `perkTraining`, `perkPromo`, `perkBonus`, `perkDiscount`
- The CSM Circle: `circleAsk`, `circleName`, `circleEarn` (the $50,000 amount is in the page markup, in the `circle-amt` line)
- Career path: `path1` to `path5`
- Header and headline: `careers`, `tagline`, `h1`

The flyer is plain text in `flyer.html`; edit it there and print a test page.

Edit files on GitHub (pencil icon) and commit; the live site updates within a minute or two.
