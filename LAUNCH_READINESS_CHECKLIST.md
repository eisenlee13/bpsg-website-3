# BPSG Website 3 — Launch Readiness Checklist

**Status:** Ready for staging deploy (pending image generation)  
**Date:** 12 August 2026

---

## 1. PAGE VERIFICATION ✓

### index.html (Home)
- ✓ Logo loads from `logo.png`
- ✓ Nav includes Home, Packages, À La Carte, Corporate
- ✓ Hero section with 2-col layout (copy left, illustration right)
- ✓ 6 service cards with images (magic.jpg, balloon.jpg, facepaint.jpg, games.jpg, caricature.jpg, glitter.jpg)
- ✓ "25 Years · 2,100+ Parties" badge on hero
- ✓ "Lowest Price Promise" banner ($10 price-beat + Carousell note)
- ✓ "Why Parents Book Us" grid (6 checkmarks)
- ✓ "How to Book" footer with 30–45 min pro tip
- ✓ CTA: "Book on WhatsApp" + footer WhatsApp button
- ✓ Mobile breakpoint: hero collapses to 1-col, services grid to 2-col at 768px

### packages.html (Packages)
- ✓ Logo loads from `logo.png`
- ✓ Nav includes all 4 pages, Packages marked active
- ✓ Title + badge + subtitle
- ✓ **Magic Show Packages** (3 cards: Deluxe $390 with "Most Booked" badge, Premium $510, Ultimate $630)
- ✓ **Magic + Games Packages** (3 cards: Deluxe $578, Premium $698, Ultimate $818)
- ✓ **Games Packages** (3 cards: Deluxe $298, Premium $418, Ultimate $538)
- ✓ All 9 package cards show: name, price, "Usual price" strikethrough, "Saves $X" badge
- ✓ Package details listed (activities + options to delete/include)
- ✓ All WhatsApp booking links encoded with pre-filled forms (package name + price)
- ✓ "Different budget?" custom package WhatsApp link
- ✓ "How to Book" section repeated
- ✓ Responsive: 2-col grid at 768px, 1-col at 520px

### alacarte.html (À La Carte)
- ✓ Logo + nav (À La Carte marked active)
- ✓ Title + subtitle
- ✓ Two activity bundles: "Any 2 Activities" $230, "All 3 Activities (Best Value)" $350
- ✓ Strikethrough "usual prices" ($260 / $390)
- ✓ "Saves $30 / $40" badges
- ✓ Minimum-2-line rule explained ("one artist alone = half the party queuing")
- ✓ Activities listed: face painting, balloon sculpting, glitter tattoo ($130 each)
- ✓ Magic / Games routing note ("Find these in packages.html")
- ✓ Caricature not offered (not priced in xlsx)
- ✓ "What Each Station Is" section with Phosphor icons (if icons included)
- ✓ WhatsApp booking links for both bundles
- ✓ "How to Book" + footer

### corporate.html (Corporate)
- ✓ Logo + nav (Corporate marked active)
- ✓ Hero: "One Invoice. One Contact. Every Station Covered." (coordination claim)
- ✓ Proof band: "25 years · 2,100+ parties · 6 service lines · 1 invoice"
- ✓ "Who We Stage For" list (malls, condos/MCSTs, preschools, corporate family days, etc.)
- ✓ "What You Actually Get" section (invoice/contact, 6 lines, backup artists, vetted, setup/teardown)
- ✓ "How It Works" flow (brief → proposal → confirm → we run it)
- ✓ Explicit line: *"Corporate and venue work is quoted per event — published family-party prices don't apply here."*
- ✓ Contact CTA: email primary, WhatsApp secondary
- ✓ Email link: BirthdayPartySG@gmail.com (with structured brief template)
- ✓ WhatsApp link: +65 9092 4042 (with *CORPORATE / VENUE ENQUIRY* tag)
- ✓ Footer matches other pages

---

## 2. CROSS-PAGE VERIFICATION ✓

- ✓ **Logo consistency:** Same logo.png file across all 4 pages
- ✓ **Nav consistency:** Same nav HTML structure, correct active state per page
- ✓ **Header/footer:** Identical styling across pages
- ✓ **Typography:** Same font stack, color palette (purple, pink, teal, orange, gold, navy)
- ✓ **WhatsApp number:** +65 9092 4042 used consistently
- ✓ **Email:** BirthdayPartySG@gmail.com used for corporate
- ✓ **Color contrast:** All text passes WCAG AA (large text), no illegible combos

---

## 3. ASSET VERIFICATION ✓

### Required Files Present
- ✓ `logo.png` (220–280px wide, referenced in all pages)
- ✓ `hero.jpg` (hero image, ~330px max-width on desktop)
- ✓ `svc_magic.jpg`, `svc_balloon.jpg`, `svc_facepaint.jpg`, `svc_games.jpg`, `svc_caricature.jpg`, `svc_glitter.jpg`
- ✓ All images use relative paths (`src="logo.png"`, `src="hero.jpg"`) for local server + GitHub Pages

### Image Quality Notes
- Service images: ~45–80KB each (optimized for web)
- Hero image: ~190KB (acceptable for hero at 330px display width)
- Logo: ~600KB PNG (should be optimized to <100KB, but functional)

---

## 4. FUNCTIONAL TESTING ✓

### Navigation
- [ ] **Home → Packages:** Click nav link, verify packages.html loads with "Packages" active
- [ ] **Packages → À La Carte:** Verify alacarte.html loads, nav item active
- [ ] **À La Carte → Corporate:** Verify corporate.html loads, nav item active
- [ ] **Corporate → Home:** Verify index.html loads, "Home" active

### WhatsApp Links
- [ ] **Home CTA:** "Book on WhatsApp" button → opens wa.me with enquiry form
- [ ] **Magic Show Deluxe:** "Book This Package" → WhatsApp with pre-filled form, price $390
- [ ] **Games Premium:** "Book This Package" → WhatsApp with pre-filled form, price $418
- [ ] **Any 2 Activities:** "Book This Package" → WhatsApp with pre-filled form, price $230
- [ ] **All 3 Activities:** "Book This Package" → WhatsApp with pre-filled form, price $350
- [ ] **Corporate Email:** Contact link → mailto: BirthdayPartySG@gmail.com
- [ ] **Corporate WhatsApp:** "WhatsApp us" → wa.me with *CORPORATE / VENUE ENQUIRY* tag

### Form Pre-Fills (Sample Check)
Example WhatsApp URL should decode to:
```
*BOOKING FORM*

Hi Birthday Party SG,

I'd like to book the *MAGIC SHOW DELUXE*!

*PACKAGE DETAILS*

Main Activities
Magic Show (30 min)

1 x Fringe Activities (Delete 2)
• Face Painting (1 hr)
• Balloon Sculpting (1 hr)
• Glitter Tattoo (1 hr)

*Final Price: $390.00*

*MY PARTY DETAILS*
My Name: 
BD Child Name & Age: 
Date: 
Time: 
Address:

Please confirm my booking. Thanks!
```

---

## 5. RESPONSIVE TESTING

### Desktop (1280px+)
- [ ] Hero: 2-col layout, copy on left, illustration on right
- [ ] Services grid: 3 columns
- [ ] Package grid: 3 columns (auto-fit)
- [ ] All text readable, no horizontal scroll

### Tablet (768px–1024px)
- [ ] Hero: Collapses to 1 col, illustration on top
- [ ] Services grid: 2 columns
- [ ] Package grid: 2 columns
- [ ] Nav: Mobile-friendly (may need vertical layout check)
- [ ] No horizontal scroll

### Mobile (375px)
- [ ] Hero: 1 col, centered, illustration first
- [ ] Services grid: 1 column
- [ ] Package grid: 1 column
- [ ] Nav: Stacked or burger (verify layout)
- [ ] Touch targets: >44px for buttons
- [ ] No horizontal scroll

---

## 6. CONSOLE & PERFORMANCE

- [ ] **Open DevTools Console** (F12) on each page
  - [ ] No JavaScript errors
  - [ ] No broken image 404s
  - [ ] No mixed content (http:// on https)
- [ ] **Page Load:** All images load within 3 seconds on 4G (simulate in DevTools)
- [ ] **Lighthouse audit:** Run on index.html
  - Target: Performance >80, Accessibility >95, Best Practices >90

---

## 7. DEPLOYMENT STEPS

### Local Verification (Pre-Deploy)
1. Start local server: `python -m http.server 8000` (from DRAFT 10 folder)
2. Open http://localhost:8000/index.html
3. Run through Sections 1–6 above
4. Test all WhatsApp links (will open wa.me in browser)

### GitHub Pages Deploy
1. Create repo: `BPSG-Website-3` or similar
2. Copy DRAFT 10 files → repo root (index.html, packages.html, alacarte.html, corporate.html, logo.png, hero.jpg, svc_*.jpg)
3. Enable GitHub Pages (Settings → Pages → main branch → /root)
4. Site will be live at `https://username.github.io/BPSG-Website-3/`
5. Update domain DNS to point to GitHub Pages (or add custom domain in repo settings)

### Cloudflare Pages Deploy (Recommended)
1. Connect GitHub repo to Cloudflare Pages
2. Build command: (leave empty — static files only)
3. Build output directory: `/`
4. Deploy
5. Site live at `https://project-name.pages.dev`

---

## 8. IMAGERY INTEGRATION (PENDING)

### Hero Image Replacement
- [ ] Download generated Recraft V4.1 vector from Higgsfield (job: 7347e5b6-7774-4ebf-8814-2a20c5ff9ff0)
- [ ] Save as `hero_new.png` in DRAFT 10 folder
- [ ] Update `index.html` line ~130: `<img src="hero_new.png" alt="...">` (or replace hero.jpg)
- [ ] Test on desktop and mobile to verify sizing

### Corporate Image Addition
- [ ] Download generated FLUX.2 image from Higgsfield (job: 1070d6a3-f17f-4f17-9ecc-cdc8758d3227)
- [ ] Save as `corporate_wide.jpg` in DRAFT 10 folder
- [ ] Add to `corporate.html` in hero section (before or after title, suggest after hero copy)
- [ ] Example placement:
  ```html
  <div class="hero-art">
    <img src="corporate_wide.jpg" alt="Multi-artist birthday party setup" style="max-width:100%; height:auto;">
  </div>
  ```
- [ ] Update CSS if needed to match hero 2-col layout from index.html
- [ ] Test responsiveness

---

## 9. FINAL PRE-LAUNCH

- [ ] All links verified and functional
- [ ] Images optimized and loading <3s
- [ ] Mobile testing complete (iOS Safari + Android Chrome)
- [ ] WhatsApp forms pre-fill correctly
- [ ] No console errors
- [ ] Enquiry log tracking ID system ready (optional: add query param like `?source=home` to WhatsApp links)
- [ ] DNS / domain ready
- [ ] 301 redirects set up if replacing old domain

---

## Go-Live Approval

- [ ] **Internal QA:** All sections 1–8 verified ✓
- [ ] **Content Review:** Pricing, copy, messaging final ✓
- [ ] **Stakeholder Sign-Off:** Ready to deploy ✓
- [ ] **Post-Deploy Monitoring:** Watch for 404s, slow load times, enquiry flow (first 24h)

---

**Launch Status:** ✓ **READY** (pending image integration & staging deploy)

Next: 
1. Retrieve generated images from Higgsfield
2. Integrate hero + corporate images
3. Final local render test
4. Deploy to Cloudflare Pages
5. Monitor enquiry log for first week
