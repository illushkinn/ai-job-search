# Search Queries for Job Scraper — Illya Grytsyk

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first.
Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`.

## Search Sites

Primary (LATAM market):
- **linkedin.com/jobs** - LinkedIn job listings (filter: Argentina / LATAM / Remote)
- **computrabajo.com.ar** - Argentina's largest general job board
- **zonajobs.com.ar** - Major Argentine job board
- **bumeran.com.ar** - Argentine job portal
- **getonbrd.com** - LATAM tech jobs
- **talent.com** - Global aggregator with LATAM filter

Secondary (NZ market — for advance outreach):
- **seek.co.nz** - New Zealand's primary job board
- **trademe.co.nz/jobs** - NZ job listings
- **linkedin.com/jobs** - LinkedIn jobs in New Zealand

Tertiary (company career pages via Google):
- Direct Google searches with `site:` filters for target companies

## Query Categories

All queries include roles target (original + discovered). Categories organized by priority.

### Priority 1: AI & Agentic Roles (Strongest Differentiation)

These match Illya's most distinctive skill set: AI evaluation + product + strategy.

```
site:linkedin.com/jobs "AI Agent" Argentina remote
site:linkedin.com/jobs "AI Product Manager" Remote
site:linkedin.com/jobs "AI Consultant" Latin America Remote
site:linkedin.com/jobs "AI Adoption" Specialist Remote
site:linkedin.com/jobs "Agentic AI" Remote
site:linkedin.com/jobs "AI Transformation" Consultant Remote
site:linkedin.com/jobs "AI Solutions Engineer" Remote
site:linkedin.com/jobs "AI Product Strategist" Remote
site:linkedin.com/jobs "AI Project Manager" Remote
site:linkedin.com/jobs "AI Evaluator" OR "AI Trainer" Remote
site:getonbrd.com "AI" "Product" LATAM
site:linkedin.com/jobs "AI" "Business Analyst" Remote
```

### Priority 2: Business Analysis & Product Engineering (Core Direction)

These match Illya's stated career transition.

```
site:linkedin.com/jobs "Business Analyst" Argentina Remote
site:linkedin.com/jobs "Product Engineer" Argentina Remote
site:linkedin.com/jobs "Product Manager" "AI" Remote
site:linkedin.com/jobs "Technical Product Manager" Remote
site:linkedin.com/jobs "Product Owner" Remote LATAM
site:linkedin.com/jobs "Product Operations Manager" Remote
site:linkedin.com/jobs "Business Analyst" "AI" Remote
site:linkedin.com/jobs "Product Manager" "Digital" Remote
site:bumeran.com.ar "Product Manager" remoto
site:computrabajo.com.ar "Business Analyst" remoto
site:zonajobs.com.ar "Product Owner" remoto
site:getonbrd.com "Product Manager" LATAM
```

### Priority 3: Digital Transformation & Consulting

These match consultancies like Globant, Accenture, Deloitte, Russell Bedford.

```
site:linkedin.com/jobs "Digital Transformation" Consultant Remote
site:linkedin.com/jobs "Innovation Consultant" Remote
site:linkedin.com/jobs "Solutions Consultant" Remote
site:linkedin.com/jobs "Digital Strategy" Remote
site:linkedin.com/jobs "Technology Consultant" LATAM Remote
site:linkedin.com/jobs "Digital Adoption" Remote
site:linkedin.com/jobs "Globant" "Project Manager" OR "Business Analyst" Argentina
site:linkedin.com/jobs "Accenture" "Business Analyst" Argentina
site:linkedin.com/jobs "Deloitte" "Digital" Argentina
site:linkedin.com/jobs "Russell Bedford" Argentina
site:linkedin.com/jobs "Consultor" "Transformación Digital" Argentina
site:linkedin.com/jobs "AI" "Consultoría" Argentina
```

### Priority 4: Growth & Strategy (Adjacent Roles)

These match Illya's founder background and consumer psychology interest.

```
site:linkedin.com/jobs "Growth Product Manager" Remote
site:linkedin.com/jobs "Growth Manager" Remote
site:linkedin.com/jobs "Go-to-Market" Strategy Remote
site:linkedin.com/jobs "Consultative Selling" Remote
site:linkedin.com/jobs "Solutions Engineer" Remote
site:linkedin.com/jobs "Product Marketing" Remote
site:linkedin.com/jobs "Internationalization" Manager Remote
site:linkedin.com/jobs "Consumer" "Product" Strategy Remote
site:linkedin.com/jobs "Ecommerce" "Product Manager" Remote
site:linkedin.com/jobs "Mercado Libre" "Product" OR "Business" Argentina
site:linkedin.com/jobs "Ualá" "Product" Argentina
site:linkedin.com/jobs "Despegar" "Product" Argentina
```

### Priority 5: NZ Market (Future Outreach — Advance Applications)

For companies in New Zealand that Illya can contact in advance of Work & Travel visa.

```
site:linkedin.com/jobs "Creative Agency" New Zealand
site:linkedin.com/jobs "Digital Agency" New Zealand
site:linkedin.com/jobs "Product" "Auckland" New Zealand
site:linkedin.com/jobs "Business Analyst" New Zealand Remote
site:linkedin.com/jobs "Project Manager" New Zealand Creative
site:linkedin.com/jobs "AI" "Wellington" New Zealand
site:seek.co.nz "Product Manager" contract
site:seek.co.nz "Digital" "Agency"
site:seek.co.nz "Creative" "Technology"
site:trademe.co.nz/jobs "IT" "Product"
site:linkedin.com/jobs "Xero" New Zealand
site:linkedin.com/jobs "Canva" New Zealand
site:linkedin.com/jobs "Bilingual" "Spanish" "English" New Zealand
site:linkedin.com/jobs "Latin America" "New Zealand" Remote
```

### Priority 6: Broader Net (Wider Opportunities)

```
site:linkedin.com/jobs "Project Manager" "Creative" Remote
site:linkedin.com/jobs "Project Manager" "Digital" Remote
site:linkedin.com/jobs "Operations Manager" Remote LATAM
site:linkedin.com/jobs "Freelance" "Project Manager" Remote
site:linkedin.com/jobs "Startup" "Product" Remote
site:linkedin.com/jobs "Bilingual" "Spanish" "English" Remote
site:linkedin.com/jobs "Multilingual" "Project" Remote
site:linkedin.com/jobs "Remote" "LATAM" "Project Manager"
site:linkedin.com/jobs "Work from home" "Product" Argentina
```

## Location Filter

When evaluating results, verify the job location:
- **Argentina (remote):** Ideal — no commute needed
- **LATAM (remote):** Ideal — similar timezone, cultural alignment
- **Buenos Aires (hybrid):** Acceptable — occasional travel from Mar del Plata
- **Global (remote):** Acceptable — verify English level requirement
- **New Zealand:** Future target — flag for advance outreach/application
- **Outside LATAM without remote:** Too far (unless NZ visa active)

## Keywords Summary

Primary keywords for search and CV optimization:
```
"AI Agent" "AI Product" "AI Consultant" "AI Adoption" "AI Transformation"
"Business Analyst" "Product Engineer" "Product Manager" "Product Owner"
"Product Operations" "Technical Product Manager" "Project Manager"
"Digital Transformation" "Innovation Consultant" "Solutions Consultant"
"Growth Product Manager" "Go-to-Market Strategy" "Consultative Selling"
"Internationalization" "Digital Strategy" "Technology Consultant"
"Consumer Psychology" "Agentic AI" "AI Product Strategist"
```

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus:
- `/scrape AI` → Priority 1 queries
- `/scrape producto` → Priority 2 queries
- `/scrape consultoria` → Priority 3 queries
- `/scrape growth` → Priority 4 queries
- `/scrape NZ` → Priority 5 queries
- `/scrape broad` → All categories
