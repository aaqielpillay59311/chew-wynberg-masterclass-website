# Website Masterclass — Notes

Source: **Jack Roberts — "AI Automations by Jack" (Skool) → Claude Code Course → Level 2: Website Masterclass** (35:44 video). Extracted from the official lesson transcript on 2026-07-05. These are the principles the new Chew site is built on.

---

## The core philosophy — "find what works, then extract it"

> "The strategy I like to take — and this is a power law across everything — is you want to find out what's working. We don't need to reinvent the wheel. Find the things that are working, extract what that is, then use that to build our stuff."

Because of modern AI you can now build **beautiful, gorgeous, show-stopping** websites cheaply — so the constraint is no longer skill, it's **taste + a good source of truth**. The source of truth = the best competitors.

## Jack's 3-step website system

1. **Competitive Intelligence** — scrape/analyse the best competitors, find what makes them work (CTAs, purpose, structure), distil into a `best-principles.md`.
2. **Design Brief** — feed those principles to the builder; be **less prescriptive, not more** (let the research drive positioning so the model doesn't "fold itself into presets"). Focus on the **transformation**, not a narrow avatar.
3. **Host it** — GitHub (version control = "game-save state", easy rollback) → Vercel (hosting) → custom domain (lifts perceived quality).

---

## Step 1 — Competitive intelligence (the judging matrix)

Prompt pattern Jack uses (adapted per business + geography):
> "Use the Firecrawl connection to find the very best [BUSINESS] that are the most successful in [GEOGRAPHY]. Identify a big list, then the top five — assess them however you want (Google reviews, SEO ranking). **Develop a judging matrix.** Deliver a report of the five, then do a deep analysis: **what do the best five have in common that the worst five don't?** So we can use those principles to build."

Save the research into a `best-principles.md` file → this becomes the brief. **(Done for Chew — see `best-principles.md`.)**

## Step 2 — Build (parallelised "flavours")

- Give the **same brief 3+ times** and you get 3 completely different sites — build several "flavours" in parallel, then pick the best:
  1. **Pure** build from `best-principles.md` only.
  2. **Reference-HTML** build — extract a gorgeous site's HTML (View-Source / "HTML Website Extractor") and use it as *inspiration* (never publish it).
  3. **Design-system** build — feed a design system from the `awesome-design` GitHub repo (Framer, Vercel, etc.).
- "You'd be surprised how much they change. Build a beautiful winner."

### UI-sniping (the signature technique)
Grab best-in-class interactive components and integrate them:
- **21st.dev** → components → *best of the week / trending* (liquid cursor, testimonials, etc.). Prompt: "underneath the H1, integrate the below component but change the text — from 21st.dev [URL]".
- **codepen.io** → effects (expanding flex cards, credit-card animations).
- Testimonials rule: **"all people want is faces, for it to look real and authentic"** — don't overkill; nobody scrolls forever.

### Images
- Use a top image model (ChatGPT/OpenAI image API) to generate **gorgeous, relevant section imagery**. *(For Chew we used Higgsfield `nano_banana_pro` to generate editorial café photography.)*

## Step 3 — Deploy & polish

- Connect **GitHub CLI** → create repo (private ok; public if open) → push. Version control = safe rollbacks.
- Connect **Vercel CLI** → publish → live URL. Add **Speed Insights** + **Analytics**. Custom domain via Vercel, 301 redirect apex→canonical, ~12 min propagation.
- **UI/UX pass** — run the **`ui-ux-pro-max` skill**: apply best principles ruthlessly. It bakes ~50–60 accessibility/UX criteria (button sizes, contrast ratios, touch targets, impairment support). "Build an entire design system off one skill."
- **SEO pass** — run the **Claude SEO** repo/skill as a *separate agent*: find the keywords to rank for, **blend capturing attention + converting + ranking**, add **schema markup**. Copy changes happen in this pass.
- Ask the agent for **"a detailed list with green tick-marks per improvement."**

## Validation — the adversarial critique gate

- **Verify the agent's own work.**
- Open a **fresh agent as a "critically challenging individual"**: "go through the website, find inconsistencies, copy that doesn't make sense, design that looks bad, and come back with a Critical / High / Medium / Low list. Don't invent critical bugs where they don't exist. Bring in any relevant repos." Fix, then re-deploy.
- Ship **HTTPS**.

---

## Distilled build rules (what actually goes into the site)

| Area | Masterclass rule |
|---|---|
| **Above the fold** | A hero that instantly shows "what a website that works looks like" — clear promise, a real person/face, one interactive component under the H1. |
| **Offer / CTA** | **Risk-reversal, outcome-based** framing (Jack's winners: *"you only pay when the phone rings"*). One primary CTA, clear hierarchy. |
| **Copy** | Sell the **transformation**, not features. Sentences must "make sense for the business." Less prescriptive. Blend attention + conversion + SEO. |
| **Proof** | Real testimonials with **faces** → authentic. Show rating. Don't overdo length. |
| **Mobile-first / a11y** | ui-ux-pro-max: proper touch targets, contrast ≥ 4.5:1, button sizes, reduced-motion, responsive. |
| **Visual** | Crisp & premium. **Thin trendy divider lines** ("a very cool trendy thing on loads of sites now"). Light **and** dark mode. Beautiful generated imagery. |
| **Interactive** | UI-sniped micro-components: cursor/hover effects, expanding/animated cards, testimonial carousels, scroll reveals. Meaningful, not gimmicks. |
| **SEO / local** | Keyword-targeted copy, **schema markup** (LocalBusiness/CafeOrCoffeeShop, reviews, hours, geo), fast (Speed Insights). |
| **Deploy** | GitHub → Vercel, custom domain, HTTPS, analytics. |

## Resources referenced in the lesson
Open Design · HTML Website Extractor (View-Source) · **21st.dev** UI assets · **Codepen.io** · **ui-ux-pro-max** skill · **Claude SEO** repo · `awesome-design` GitHub repo (design systems) · Firecrawl (competitor scraping) · OpenAI image gen.
