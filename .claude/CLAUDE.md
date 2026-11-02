# CCA Photos

Static photo index for Costa Catholic Academy, live at cca.polillo.com.
Hand-written HTML with the MDBootstrap UI kit and no build step. Photos are
hosted on SmugMug in password-protected galleries; this site only links to them.
Pushing to `main` publishes the site.

## Pages
- `index.html`: Home, most recent galleries for the current school year
- `index_cca_bb.html`: Basketball
- `index_cca_tf.html`: Track & Field
- `index_cca_vb.html`: Volleyball (has no current-season header, only Prior Seasons)
- `index_cca.html`: Events
- `about.html`: About

## Formatting
- Entries go between `<!-- Post Begin -->` and `<!-- Post End -->` comments,
  newest first.
- Date format is `Mon, 02 Nov 2026`, on its own line: `Title<br />Date`.
- Dated entries have no link on the icon. Archive and "All Photos" entries do,
  with `aria-hidden="true" tabindex="-1"` on that link.
- All icons use `alt=""`.
- Buttons read `View&nbsp;Photos`, or a label such as `7th Grade`.
- Menu and page layout are repeated on all six pages, so site-wide changes must
  be made on each. The current page's link has `active fw-bold` and
  `aria-current="page"`.

## Adding a gallery
Add the entry to its sport or Events page and to Home.

## New school year
1. Get the archive links for the year that just ended, plus the link for the
   new year's All Photos gallery.
2. On Basketball, Track & Field and Events, change the current header to the
   new year and remove that year's individual entries.
3. Add a `YYYY-YYYY Season Archive` entry (`Event Archive` on Events) at the top
   of Prior Seasons or Prior Years.
4. Add "Coming Soon" under the new header where there are no galleries yet.
5. On Home, change the header, remove the old entries, and update
   "All YYYY-YYYY Photos".
6. Check every SmugMug link, because moving galleries to the archive breaks the
   old URLs. Password-protected galleries still load a page if the link is good.

Only add a sport to Prior Seasons if photos were taken that year.
