# StonePro SD — Conversion, Trust, SEO & Positioning Audit

**Scope:** All 13 pages of the static site (`index.html`, 5 service pages, 7 city pages).
**Stance:** Every missed lead = $10,000. Brutal honesty, ranked by revenue impact.
**Date:** June 2026

---

## 1. Executive Summary

This is one of the best-written contractor sites we've audited. The positioning voice is already where most competitors never get: "restore instead of replace," coastal-specific expertise, HOA liability framing, honest-assessment promise. The service-page headlines ("The cheapest decade of protection your concrete will ever get," "Before you tear it out, let us look at it") are genuinely strong sales copy.

**But the site cannot convert a single lead today.** The phone number is (000) 000-0000 on every page. The quote form posts to nothing — a visitor who fills it out sees "Request sent" and their lead evaporates. The before/after "photos" are CSS gradients. The license number is #0000000. There is no mobile navigation below 860px wide — which is where 60–75% of home-services traffic lives.

The brutal truth in one sentence: **this site has premium copy wrapped around an empty trust layer, and the trust layer is what closes $10,000 jobs.** Luxury homeowners and HOA boards don't buy words; they buy proof — real photos, real reviews, a real license number, a real human who answers.

A second strategic truth: the brief says "Southern California," but the site is built — correctly — around coastal North County San Diego. **Do not "fix" this.** A specialist who owns 7 wealthy coastal zip-code clusters will out-rank, out-close, and out-earn a generalist who claims all of SoCal. The architecture already supports expansion (city-page template + service schema); expand only after North County is dominated.

### The five moves that matter most (everything else is downstream)

1. **Make the site able to receive a lead** — real phone, real form endpoint, real license. (Currently: $10,000 lost per submission.)
2. **Replace simulated imagery with real project photography** — even 3 jobs, photographed properly, beats every gradient on the site. Until then, the site *says* "the proof is in the after" and then shows no proof. That contradiction actively damages trust.
3. **Add a mobile menu and a persistent mobile call/text bar.** The #1 conversion action for this audience on mobile is a thumb-tap call. It currently takes 4+ scrolls to find a (fake) phone number.
4. **Build the trust layer as jobs complete:** reviews pipeline → Google Business Profile → review schema → named warranty → "after" photo discipline (already promised in the process copy — keep that promise publicly).
5. **Quantify "fraction of replacement cost" everywhere.** The single most persuasive number this company owns is the gap between "$18,000 repour" and "$4,500 restoration." It appears nowhere as a number. Numbers convert; adjectives don't.

---

## 2. Launch Blockers (not improvements — these are "the cash register is unplugged")

| # | Blocker | Where | Revenue impact |
|---|---------|-------|----------------|
| 1 | Phone is (000) 000-0000 | Every page, every CTA | 100% of call leads lost |
| 2 | Quote form posts nowhere (`// TODO: POST form data`) but shows a success message | Every page | 100% of form leads lost — *and* the visitor believes they're in your queue. They wait, hear nothing, hire a competitor, and tell neighbors you ghosted them. This is worse than no form. |
| 3 | CA LIC #0000000 | Hero note + footer, every page | An obviously fake license number on a contractor site is a trust *negative*, not a neutral. Sophisticated SoCal homeowners check CSLB. |
| 4 | No mobile navigation below 860px (`.nav-links{display:none}`, no hamburger) | Every page | Mobile visitors can reach only the quote anchor. Service and city pages become orphans on the device most visitors use. |
| 5 | Before/after slider is a simulated gradient, captioned "(replace with your real before/after photo)" — visible to customers | Homepage hero | The signature visual proof element currently proves you have no projects. |
| 6 | No analytics, no conversion tracking of any kind | All pages | You cannot know what's working. Flying blind on ad spend. |

**Fix order: 1, 2, 4, 6 can ship this week with no photography. 3 and 5 ship the day the license/photos exist.**

---

## 3. Top 20 Highest-ROI Improvements (ranked)

1. **Wire the quote form to a real endpoint** (CRM webhook, or even Formspree/Basin day one) with email + SMS notification to the owner. Add a hidden `page_source` field so you know which page converts.
2. **Real phone number with call tracking** (CallRail or similar) — separate tracked numbers for site vs. GBP unlocks attribution.
3. **Mobile hamburger menu** + persistent bottom bar on mobile: `[ Call ] [ Text ] [ Get Quote ]`. Text matters: affluent homeowners and property managers strongly prefer text-first contact for contractors.
4. **Photograph the first 5 jobs like the business depends on it** (it does): tripod, same angle before/after, golden hour for the "after." Replace homepage slider, gallery tiles, and add 2–3 per service page.
5. **Real license number + clickable CSLB verification link** ("Verify our license → CSLB #XXXXXXX"). Nobody else links to their own license check. Instant differentiation, costs nothing.
6. **Quantified cost-comparison module** on homepage and restoration page: "Typical 800 sq ft repour: $15,000–$25,000+, 2–3 weeks, demolition. Typical restoration: a fraction of that, 2–4 days, zero demolition." Even ranges without exact pricing anchor the value.
7. **Google Business Profile** set up day one, review-request workflow built into job completion (text the link while you're still in the driveway and goodwill is peak).
8. **Named warranty/guarantee** — e.g., "The StonePro Standard: written scope, approved sample before full application, documented before/after, X-year workmanship warranty, scheduled resealing reminder." Put it on every page. A named promise is a positioning asset competitors can't copy without looking like copycats.
9. **Founder/team section with a real face and name.** "Hiring the wrong contractor" is the #1 stated fear; an anonymous company is the #1 trigger of it. One good portrait + 3 sentences of "who answers when you call" outperforms any amount of copy.
10. **Per-page tailored form headline + service preselect** (already done on service pages — extend the pattern: city pages should preselect city, which they do; now shorten the form on mobile to Name/Phone/City + photo upload).
11. **Photo upload field on the quote form.** The site already says "send a few photos." The form has no upload. Photo-attached leads close at far higher rates (you can quote accurately and respond specifically).
12. **`sitemap.xml` + `robots.txt` + Open Graph/Twitter tags + favicon.** Zero OG tags today — every shared link renders naked. HOA board members *forward links to each other*; that share preview is a trust surface.
13. **Homepage LocalBusiness schema** — the only page with no JSON-LD is the most important one. Include `areaServed`, `geo`, `sameAs` (GBP, Yelp, Instagram), hours, and license number in `hasCredential`.
14. **Fix canonical/filename mismatch.** Canonicals point to `/anti-slip-pool-deck-sealing` and `/rancho-santa-fe` but files are `.../anti-slip-pool-deck-sealing.html` and `concrete-rancho-santa-fe.html`. On GitHub Pages these canonicals 404. Either set up clean-URL hosting (Netlify/Vercel redirects) or make canonicals match reality. Wrong canonicals = pages may not index at all.
15. **Reviews section** (homepage + service pages) the moment 3 real reviews exist — with full names, neighborhoods, and project type. "Mark R., The Covenant — motor court restoration" is worth ten anonymous 5-star widgets.
16. **Pool deck restoration page** as its own URL. "Pool deck restoration/resurfacing" has distinct, high-value search intent currently split between two pages. Highest-margin keyword in the set.
17. **HOA/commercial dedicated page** with the board-ready report as a lead magnet ("Request the free Deck Liability Assessment"). HOA jobs are the recurring-revenue engine; they deserve more than a homepage section.
18. **FAQ on the homepage** (4–5 questions) with FAQPage schema — the only page without FAQs is the one most visitors land on.
19. **Before/after case study pages** (1 per service over time): location, problem, process, materials, timeline, cost-vs-replacement delta, photos. These become the highest-converting pages on the site and the backbone of SEO content.
20. **Exit lead magnet for researchers:** "The San Diego Homeowner's Guide to Concrete Restoration vs. Replacement (with real cost ranges)" — email-gated PDF. Captures the 97% not ready to request a quote today.

---

## 4. Top 10 Conversion Improvements

1. **Persistent mobile action bar** (call/text/quote) — single biggest conversion lever on the site.
2. **Form works + photo upload + mobile-shortened** (Name, Phone, City, Photos; everything else optional). Every removed field measurably lifts completion.
3. **Response-time promise at the form:** you already say "within one business day" *after* submission. Say it *before*: "We respond within one business day — usually same-day." Then beat it.
4. **Text-message option everywhere phone appears.** "Call or text photos to (XXX) XXX-XXXX" is the lowest-friction lead path that exists for this trade. Make texting photos a first-class CTA, not a footnote.
5. **Replace the second hero CTA "See our work" → keep, but make it deliver.** Currently it scrolls to placeholder tiles. Until real photos exist, swap to "Get a free honest assessment" (the strongest offer on the site, currently buried in the 6th service card).
6. **Sticky header CTA on mobile:** the Request a Quote button survives below 860px (good) — but verify tap target size and add `tel:` as a second icon button in the header on mobile.
7. **Quantify the offer at every CTA.** "Request a quote" is commodity language. "Get your free assessment + written quote" raises perceived value at zero cost. (Excellent versions already exist on the HOA panel and pool page — standardize them.)
8. **Success state should sell the next step:** after submit, show "Request received. ✓ Here's what happens next: 1) We review your photos today. 2) [Name] calls or texts you within one business day. 3) On-site assessment if it's a fit." Reduces post-submit anxiety and screens for quality.
9. **Add a "What it costs" section** (ranges + the replacement comparison). Price-curious visitors who find zero pricing signal bounce to competitors who give a range. Affluent ≠ price-insensitive; affluent = waste-averse.
10. **Spam protection on the form** (honeypot + server-side validation) — the moment it works, it will be hammered, and junk leads bury real $10k ones.

---

## 5. Top 10 Trust Improvements

1. Real before/after photography, watermark-free, location-labeled. (The entire brand promise — "Every project is photographed before and after" — depends on this.)
2. Real license + CSLB verify link + insurance carrier named ("Insured through [carrier], certificates available on request").
3. Founder face, name, and story ("Why we only do surface restoration").
4. Reviews with names + neighborhoods; aggregate rating schema once ≥5 reviews exist.
5. Named written warranty, stated in years, on every page.
6. The sample-first promise elevated to a guarantee: "You approve a cured sample on your own concrete before we commit to the full surface. If you don't love it, we stop. You owe nothing for the sample." That's a risk-reversal worth a section, currently a half-sentence in process step 03.
7. The honest-assessment promise elevated: "We'll tell you if your concrete needs nothing at all yet" is the single most differentiating sentence on the site. Put it in the hero area or trust strip, not card #6.
8. Project documentation as a visible artifact: show a (redacted) sample of the board-ready HOA report and the homeowner's written scope. Proof of process beats description of process.
9. Manufacturer/system credibility: name the sealer systems' performance class (UV-rated, breathable, pool-chemistry-rated) and any installer certifications.
10. "Recent projects" with dates/cities once real — recency signals an alive, busy company. (The pre-launch marquee currently signals the opposite: "COMING TO YOUR AREA SOON" tells a luxury buyer *nobody has hired them yet*. Remove it the day you have one completed job, even if "official launch" is later.)

---

## 6. Top 10 SEO Improvements

1. **Fix canonicals vs. real URLs** (see #14 above) and add a canonical to the homepage. Indexing-level severity.
2. **sitemap.xml + robots.txt**, submit to Search Console day one.
3. **Homepage LocalBusiness/HomeAndConstructionBusiness schema** with `sameAs`, `geo`, `hasCredential`, `aggregateRating` (when real).
4. **Google Business Profile** + weekly photo posts + review velocity. For "concrete staining near me" queries, the map pack *is* the battlefield; the website's job is to convert the click and feed the profile.
5. **Split "pool deck restoration"** into its own page; current architecture has "anti-slip pool deck sealing" (great, low-competition) but cedes the bigger head term.
6. **Add pages for unowned brief keywords:** concrete recoloring (distinct intent from staining — "my colored concrete faded" vs "I want new color"), grip additive / slip-resistant sealer (commercial-intent), pool deck sealing (vs anti-slip variant).
7. **Title tag tuning:** lead with the keyword + city, keep the brand last (already done — good). Add the year-free "cost" modifier pages later: "Concrete Staining Cost in San Diego — What Actually Drives Price" is a content page that ranks and pre-qualifies.
8. **BreadcrumbList schema** (the visual breadcrumb already exists in `.eyebrow` — mark it up).
9. **City-page depth is genuinely good** (neighborhood lists, local conditions — better than 95% of doorway pages). Strengthen: 1–2 real project photos per city over time, and link city pages to each other (currently only service→city links exist; add "nearby areas" footer on city pages).
10. **Content engine (one piece/month, photo-driven):** "Acid stain vs. integral color vs. dye," "Why glossy sealers make pool decks dangerous," "What salt air does to concrete in Del Mar," "HOA pool deck liability: what boards must document." Each targets a question your buyers actually type, and each is also sales collateral.

---

## 7. Top 10 Positioning Improvements

1. **Lead with restore-vs-replace economics, with numbers.** It's the brief's core promise and the site's strongest latent message — currently stated qualitatively ("a fraction of the cost") in card 3 and city FAQs only.
2. **Keep the narrow geography. Own it louder.** "Coastal North County, exclusively. We stay local on purpose." is elite positioning copy. Resist the temptation to claim Southern California until you can prove it; expand city-by-city behind real jobs.
3. **Name the category.** Competitors say "concrete contractor." The site should consistently say **surface restoration specialists** — it appears nowhere as a phrase. The company that names the category owns it.
4. **The rock/waterslide specialty is the moat — promote it harder.** "A specialty few crews in San Diego County handle" is true and verifiable in a Google search. It deserves homepage hero rotation or a dedicated showcase, because it's unGoogleable-elsewhere proof that you're not a commodity crew.
5. **Coastal-science authority:** the salt-air/marine-layer/UV framing is excellent. Deepen it once: a short "Why coastal concrete fails differently" explainer makes the expertise legible and is endlessly quotable/linkable.
6. **The honest-assessment promise as brand pillar** (see Trust #7) — "we'll tell you if it needs nothing" is contrarian, memorable, and self-qualifying. Luxury buyers are advice-buyers before they're service-buyers.
7. **Document-driven professionalism for commercial:** board-ready reports, insurance docs, written scopes — this is exactly what property managers can't get from typical crews. Make a sample artifact visible.
8. **Maintenance relationship, not transaction:** "Every surface goes on a resealing calendar" converts one-time jobs into recurring revenue and signals stewardship. Currently mentioned twice in passing; make it a named program ("StonePro Surface Care").
9. **Anti-commodity language audit:** the copy is already largely free of "quality workmanship / customer satisfaction" filler. Protect that. The one drift: "concrete done right" (Carlsbad H1) is the genre's most common cliché — rewrite.
10. **Premium restraint in claims:** no superlatives without evidence. The current copy mostly earns this; keep the rule "every claim is checkable" as a brand law.

---

## 8. Homepage Critique (section by section)

**Pre-launch banner** — Kill at launch as planned, but kill it *early* (see Trust #10). "Coming soon" and "premium established expert" cannot coexist. The mailto: CTA ("Reserve your spot") is friction-heavy; if a pre-launch list matters, use the form with a "pre-launch" flag.

**Header/nav** — Clean, premium, sticky: good. Issues: (a) no mobile menu — blocker; (b) "HOA & Pool Decks" nav label links to the pool service page from the homepage but to `#hoa` from other pages — inconsistent destination, pick one (recommend a real /hoa-commercial page); (c) consider phone number in the header on desktop — for a call-first trade, hiding the number until the footer/quote section costs calls.

**Hero** — "Same concrete. Different home." is a genuinely good line: clear benefit, premium cadence, no jargon. Keep it. The lede is strong. Weaknesses: (a) the proof element beside it is fake (blocker #5); (b) hero note shows the fake license; (c) no human/social proof near the CTA. When photos exist, A/B the abstract line against a concrete-value line: "Your concrete doesn't need to be replaced. It needs to be restored." — speaks directly to the $20k fear in the visitor's head. (d) "Request a quote" twice (header + hero) is fine; make the ghost CTA earn its place (see Conversion #5).

**Trust strip** — Right instinct, weak ammo. "Licensed & insured" + "Coastal-grade sealants" are claims, not credentials. Upgrade as assets arrive: `CSLB #XXXXXX (verify)` · `★ 5.0 Google (XX reviews)` · `X-year written warranty` · `Sample approved before full application — always`.

**Services grid** — Well-differentiated, benefit-led card copy; the dark 6th card ("Not sure what your concrete needs?") is the best conversion idea on the page — but it's the strongest offer hidden in the weakest position. Promote that offer to the hero area or directly under it.

**Gallery** — "The proof is in the after." with placeholder tiles is the site's most self-damaging moment. Until 3 real projects exist, replace the section with the process/sample-guarantee story; never ship a proof section without proof.

**Process** — Excellent. "Prep is 70% of a finish that lasts — it's where we refuse to cut corners" is exactly the connoisseurship luxury buyers reward. Add one artifact photo per step when available (assessment sheet, prepped surface, sample chips, sealing pass).

**Service areas** — "Coastal North County, exclusively. We stay local on purpose." — best section on the page. The premium-bordered La Jolla / Rancho Santa Fe chips are a subtle, smart touch. No changes beyond linking real projects per city later.

**HOA section** — Strong, correct buyer psychology (liability, documentation, resident-friendly). Deserves promotion to its own page with the report sample as a lead magnet.

**Quote section** — Good structure (reassurance aside + form). Fix: working endpoint, photo upload, response-time promise above the form, post-submit next-steps, real phone, and a "prefer to text? Send photos to XXX" line.

**Footer** — Functional. Add: real license, GBP/Yelp/Instagram links, and a one-line brand statement. The 7 city links + 5 service links are good internal linking.

## 9. Service-Page Critique (template, audited via anti-slip page)

What's right: breadcrumb, problem-led intro that demonstrates diagnostic expertise (two causes of slippery decks), signs-you-need-this sidebar, process, city links with context, FAQs with schema, related services, pre-selected form. This is a top-decile service-page template.

Weaknesses, in revenue order:
1. **No proof block** — no photos, no reviews, no projects. Slot a "Recent decks" strip between process and FAQs.
2. **No risk-reversal block** — the sample guarantee and warranty belong on every service page, near the CTA.
3. **No cost anchoring** — the restoration and pool-deck pages especially should carry the replacement-vs-restoration economics module.
4. **"See our work" CTA scrolls to the homepage's placeholder gallery** — until real, route to the assessment offer.
5. FAQs are excellent (specific, confident, board-psychology-aware) — add one cost-range FAQ per page ("What does it typically cost?") because that's the #1 unasked question and an FAQ snippet opportunity.

## 10. City-Page Critique (template, audited via Rancho Santa Fe)

These are far better than typical location doorway pages — real local detail (Covenant, Fairbanks Ranch, estate irrigation hard-water crusting, inland sun vs. coastal salt), differentiated H1s, locally-reframed service cards, local FAQs, LocalBusiness + FAQ schema. Keep this quality bar for any expansion city.

Improvements: (1) one real local project photo each, eventually; (2) neighborhood chips are dead `<span>`s — fine, but add a line of unique copy under them naming 1–2 neighborhood-specific surface conditions to deepen uniqueness; (3) cross-link adjacent city pages; (4) "The finish your builder never gave you" (Carmel Valley) is the best H1 on the site — that insight (newer-build community, builder-grade concrete) is a whole content angle.

## 11. Mobile UX Critique

1. **No nav below 860px** — blocker, covered.
2. **No persistent contact bar** — the highest-ROI mobile element for this trade; covered.
3. **Form on mobile:** 6 fields + textarea is long; collapse to essentials + photo upload (the phone camera is the mobile user's superpower — exploit it: "Snap 2–3 photos of your concrete right now").
4. **Hero slider:** `touch-action:none` on a full-width element can trap vertical scrolling on touch devices — test on a real phone; users who can't scroll past the hero bounce. Consider handle-only drag.
5. **Marquee banner** consumes top viewport on mobile with the tag hidden — at launch this disappears anyway.
6. Type scale and tap targets are otherwise well-handled; section padding (88px) could compress ~30% on mobile to bring proof and CTAs higher.

## 12. Luxury Brand Critique

The design system is genuinely distinctive: concrete-and-stain palette, Archivo + Plex Mono spec-sheet typography, restrained 4px radius, no stock-photo genericism, no gradients-for-gradients'-sake. It reads "engineering studio meets craftsman" — exactly right for the "they clearly know more than everyone else" reaction. Protect it.

Watchouts: (1) Luxury is proven by *specificity and proof*, and all proof is currently absent — the design is writing checks the content can't cash yet. (2) The monospace/eyebrow styling flirts with "tech startup" in a few spots (the `// PLACEHOLDER` comment styling, marquee) — fine once real photography grounds it in physical work. (3) Avoid adding any trend elements (glassmorphism, parallax, AI-generated imagery) when filling gaps — real job-site photography in consistent light is the entire art direction. (4) One naming-level note: "StonePro SD" vs. the brief's "StonePros" — resolve the brand name once, everywhere, including domain, GBP, and license records; inconsistent NAP (name/address/phone) data measurably hurts local SEO.

## 13. Copy Rewrites (exact replacements)

**Trust strip (post-launch version):**
> CSLB #XXXXXX — verify it · ★ 5.0 on Google · Written X-year warranty · You approve a sample first, always

**Hero note:**
> LICENSED & INSURED · CSLB #XXXXXX · RESPONSE WITHIN ONE BUSINESS DAY

**Cost module (new, homepage + restoration page):**
> **Tear-out and repour:** $15,000–$25,000+, two to three weeks, demolition crews on your property.
> **Restoration:** typically 20–40% of that, two to four days, no demolition.
> Same concrete. We'll tell you honestly which one yours needs — even when the answer is "neither, yet."

**Carlsbad H1 (replace "concrete done right"):**
> From the Village to La Costa — *finishes that survive the salt air.*

**Form aside (all pages):**
> Send a few details and photos. Within one business day you'll hear from [Name] — not a call center — with an honest read and a clear written quote. If your concrete doesn't need work yet, we'll tell you that too.

**Post-submit success:**
> **Got it — your photos are on [Name]'s desk.** Here's what happens next: we review today, you hear from us within one business day, and if it's a fit we schedule a no-cost on-site assessment. Prefer faster? Text us at (XXX) XXX-XXXX.

**Honest-assessment promise, promoted (under hero or as band):**
> **The assessment is free and the advice is honest.** Roughly one in five properties we look at doesn't need work yet — and we say so. When you do hire us, you'll know it's because your concrete actually needed it.
> *(Use the real ratio once known. Never invent it.)*

## 14. Wireframe Recommendations

**Homepage (post-launch order):** Hero (real B/A slider) → trust strip (credentials) → honest-assessment band → services grid → cost-comparison module → real gallery (3–6, city-labeled) → reviews → process → service areas → HOA banner (links to /hoa page) → FAQ → quote.

**Service page additions:** proof strip after process; warranty + sample-guarantee card beside FAQ; cost-range FAQ; mobile sticky bar.

**New pages, priority order:** /hoa-commercial (with report lead-magnet) → /pool-deck-restoration → /our-work (gallery hub, filterable by city/service) → /about (founder, why-specialists, license/insurance artifacts) → /concrete-recoloring → case-study pages → cost-guide content pages.

## 15. Missing Content Opportunities

- Pool deck restoration & resurfacing (head term, dedicated page)
- Concrete recoloring (faded colored-concrete intent)
- Grip additive / slip-resistant sealer (commercial intent)
- Cost guides: staining cost, sealing cost, restoration vs replacement (top-funnel, high intent)
- "Why glossy sealers turn pool decks into ice" (links to anti-slip; intensely shareable to HOA boards)
- "What salt air does to concrete" coastal-science explainer
- HOA board's documentation checklist for pool deck liability (gated lead magnet)
- Builder-grade concrete in newer communities (Carmel Valley angle, expandable to any new-build area)
- Seasonal: "Best time of year to seal concrete in San Diego" (answer drives off-peak bookings)

## 16. Competitive Advantage Recommendations

Against the typical top-50 CA field (commodity concrete contractors, coating franchises, pressure-washing upsellers):

| Competitor weakness | StonePro counter (mostly already latent in copy — make it explicit) |
|---|---|
| Generalists who pour, coat, and patch everything | Restoration-only specialists; name the category "surface restoration" |
| No geographic story | "Coastal North County, exclusively" + salt-air science |
| Coatings that peel (epoxy/paint crews) | "Color in the concrete, not on it" + breathable/UV system specifics |
| No documentation | Board-ready reports, written scopes, photographed before/after as standard |
| High-pressure sales | Free honest assessment, "one in five needs nothing" |
| Nobody touches artificial rock | Waterslide/rock restoration as visible flagship specialty |
| Transactional | Resealing calendar / named maintenance program |
| Anonymous crews | Named founder, who-answers-the-phone transparency |

The "obvious choice" formula: **specialist category + exclusive geography + visible proof discipline + honest-assessment risk reversal + documentation professionalism.** No franchise can copy the geography story; no commodity crew will copy the documentation discipline.

## 17. 90-Day Roadmap (ranked by revenue impact)

**Weeks 1–2 — Make the site able to take money (no photography required):**
form endpoint + notifications + spam protection; real phone + call tracking; texting CTA; mobile hamburger + sticky contact bar; GA4 + conversion events; sitemap/robots/OG/favicon; homepage schema + canonical fixes; real license everywhere + CSLB link; GBP created.

**Weeks 3–5 — First proof:**
photograph first 3–5 jobs (before/after discipline from job one); replace hero slider + gallery; first 3 reviews requested and published; founder/about section; named warranty + sample guarantee on all pages; remove pre-launch banner; success-state rewrite.

**Weeks 6–9 — Convert harder:**
cost-comparison module; honest-assessment band; /hoa-commercial page + board-report lead magnet; /pool-deck-restoration page; homepage FAQ + schema; photo upload on forms; review schema once ≥5 reviews.

**Weeks 10–13 — Compound:**
/our-work gallery hub; first 2 case studies; 2 cost-guide articles; city-page photo upgrades + cross-links; /concrete-recoloring page; GBP weekly posting + review velocity routine; A/B hero headline test; quarterly resealing-reminder email automation (the maintenance program's revenue tail).

**The discipline that makes all of it work:** every completed job produces, same-day, (1) before/after photos, (2) a review request, (3) a GBP post, (4) a resealing-calendar entry. Four assets per job, forever. That flywheel — not any single page change — is what makes a restoration company unbeatable in a local market.
