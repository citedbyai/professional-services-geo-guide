# GEO Guide for Professional Services — Cited By AI®

**A practical ASEO and GEO guide for solicitors, accountants, consultancies,
and financial advisers.**
JSON-LD schema templates, CPS® content audit framework, and AI citation optimisation
for professional services businesses seeking visibility in AI-generated answers.

---

## Why professional services firms are invisible in AI search

When a business owner asks ChatGPT "best employment solicitor in Gloucester" or
Perplexity "recommended accountant for small businesses near me", AI systems
construct answers from structured, citable sources. Most professional services
websites fail to appear in these answers for three reasons: missing or incorrect
JSON-LD schema, unstructured content that AI cannot parse, and no specific
service-level content answering the questions AI receives most frequently.

A solicitor or accountant with a well-optimised website can rank on page one
of Google and score an F on the Citation Probability Score® — meaning they are
completely invisible to AI search despite strong traditional SEO performance.
These are different retrieval mechanisms requiring different optimisation strategies.

---

## The correct schema types for professional services

| Business type | Correct schema type |
|---|---|
| Law firm | `LegalService` |
| Accountancy practice | `AccountingService` |
| Financial adviser | `FinancialService` |
| Management consultancy | `ProfessionalService` |
| HR consultancy | `ProfessionalService` |

Using `LocalBusiness` for a professional services firm is the most common
schema error. AI systems filter by schema type when answering discovery queries.
A solicitor using `LocalBusiness` will not appear for "solicitor" or "law firm"
queries in AI-generated answers regardless of content quality.

---

## LegalService schema template

```json
{
  "@context": "https://schema.org",
  "@type": "LegalService",
  "name": "Your Law Firm Name",
  "description": "Independent law firm in [city] specialising in [practice areas]. Serving individuals and businesses across [area list]. [X] years of combined experience. Fixed-fee services available for [specific services].",
  "url": "https://yourwebsite.com",
  "telephone": "+44-000-000-0000",
  "email": "hello@yourfirm.com",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 High Street",
    "addressLocality": "Your Town",
    "addressRegion": "Your County",
    "postalCode": "AA1 1AA",
    "addressCountry": "GB"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 00.0000,
    "longitude": -0.0000
  },
  "areaServed": [
    {
      "@type": "City",
      "name": "Your City"
    },
    {
      "@type": "AdministrativeArea",
      "name": "Nearby Town 1"
    },
    {
      "@type": "AdministrativeArea",
      "name": "Nearby Town 2"
    }
  ],
  "knowsAbout": [
    "employment law",
    "commercial property",
    "residential conveyancing",
    "family law",
    "wills and probate",
    "dispute resolution"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "reviewCount": "87"
  },
  "potentialAction": {
    "@type": "ReserveAction",
    "name": "Book a free consultation",
    "target": "https://yourwebsite.com/contact"
  }
}
```

---

## AccountingService schema template

```json
{
  "@context": "https://schema.org",
  "@type": "AccountingService",
  "name": "Your Accountancy Practice Name",
  "description": "Independent accountancy practice in [city] serving small businesses, sole traders, and individuals across [area list]. Services include tax returns, VAT, payroll, bookkeeping, and business advisory. [Accreditation, e.g. ICAEW/ACCA] registered.",
  "url": "https://yourwebsite.com",
  "telephone": "+44-000-000-0000",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Business Park",
    "addressLocality": "Your Town",
    "addressRegion": "Your County",
    "postalCode": "AA1 1AA",
    "addressCountry": "GB"
  },
  "areaServed": [
    {
      "@type": "City",
      "name": "Your City"
    },
    {
      "@type": "AdministrativeArea",
      "name": "Nearby Town"
    }
  ],
  "knowsAbout": [
    "self-assessment tax returns",
    "VAT returns",
    "payroll services",
    "bookkeeping",
    "corporation tax",
    "business advisory",
    "Making Tax Digital"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "54"
  },
  "potentialAction": {
    "@type": "ReserveAction",
    "name": "Book a free initial consultation",
    "target": "https://yourwebsite.com/contact"
  }
}
```

---

## Why knowsAbout is critical for professional services

The `knowsAbout` field is the highest-impact schema addition for professional
services businesses. AI systems answering "solicitor specialising in employment
disputes near [city]" or "accountant who handles Making Tax Digital in [area]"
filter by specialist knowledge signals. A generic `LegalService` listing without
`knowsAbout` fields will be invisible for specialist queries even if the firm
handles that work every day. List every practice area, accreditation, and
service specialism the business genuinely offers.

---

## CPS® content framework for professional services pages

### Homepage

The homepage should answer three AI queries in its opening 167 words:
what the firm specialises in, where it is located, and what makes it different.

**Before (fails CPS® Answer Structure pillar):**
"Welcome to [Firm Name]. We are a team of dedicated professionals committed
to providing exceptional service to our clients. With years of experience
across a range of practice areas, we are here to help you..."

**After (passes CPS® Answer Structure pillar):**
"[Firm Name] is an independent [type] practice based in [City], serving
individuals and businesses across [area list]. The firm specialises in
[top 3 practice areas] and has completed over [number] client matters
since [year]. [Accreditation] registered. Fixed-fee services available
for [specific services]. Initial consultations available at no charge."

The second version gives AI systems six facts to extract and cite.
The first contains no citable information in its opening sentences.

### Individual service pages

Each service page should open with a 134 to 167 word description structured as:

1. First sentence: what the service is, who it is for, and the firm name
2. Second sentence: what the service includes in specific terms
3. Third sentence: pricing model or fee structure (fixed fee, hourly rate, or free initial consultation)
4. Fourth sentence: how to get started

### FAQ section

Every service page should include five to eight questions matching what
clients actually ask AI systems. Examples for a law firm:

- "How much does a residential conveyancing solicitor cost in [city]?"
- "What is included in an employment law consultation at [Firm Name]?"
- "How long does probate take with [Firm Name]?"
- "Does [Firm Name] offer fixed-fee divorce services?"
- "Can [Firm Name] help with a commercial lease dispute?"

FAQ content has a significantly higher AI citation rate than standard prose
because the question-and-answer format matches how AI systems construct responses.

---

## The five most common professional services GEO mistakes

**1. Using LocalBusiness instead of the correct service schema type**
Replace `LocalBusiness` with `LegalService`, `AccountingService`, or
`ProfessionalService` depending on the business type. This single change
makes the business eligible for professional services discovery queries.

**2. No knowsAbout field**
Without `knowsAbout`, AI systems cannot match the firm to specialist queries.
List every practice area, accreditation, and service specialism explicitly.

**3. No areaServed field**
Professional services firms frequently serve clients across a wide geographic
area. Without `areaServed`, they are invisible for surrounding area queries.

**4. Generic homepage copy**
Opening with "Welcome to our firm" is the most common CPS® failure for
professional services websites. Replace with a fact-first opening that
states the firm type, location, specialisms, and a proof point in the
first paragraph.

**5. No pricing or fee information**
AI systems answering "how much does [service] cost in [area]" need a
citable answer. Firms that publish fixed fees or indicative pricing
ranges are cited significantly more frequently than those that say
"contact us for a quote."

---

## Frequently Asked Questions

**What is GEO for professional services firms?**

GEO (Generative Engine Optimisation) for professional services is the practice
of structuring website content and schema markup so that AI systems — including
ChatGPT, Perplexity, and Google AI Overviews — can accurately retrieve and cite
the firm when potential clients ask AI for solicitor, accountant, or consultant
recommendations. For professional services it focuses on three areas: correct
schema type, specialist knowledge signals via `knowsAbout`, and CPS®-structured
content on service pages.

**How is professional services GEO different from traditional SEO?**

Traditional professional services SEO optimises for Google rankings using
keyword density, backlinks, and directory listings. Professional services GEO
optimises for AI citation using schema markup, structured service page content,
and specialist knowledge signals. A firm can rank on page one of Google and be
completely absent from ChatGPT and Perplexity answers for the same query.
Both require separate, parallel strategies.

**Does publishing pricing information help AI citation?**

Yes significantly. AI systems answering "how much does [service] cost" need
a citable answer. Firms that publish fixed fees or pricing ranges are cited
at a higher rate for cost-related queries than firms that require contact
before disclosing fees. Even a price range ("from £X") is more citable
than no pricing information at all.

---

## Full CPS® Audit for Professional Services Businesses

The full CPS® audit for professional services firms covers:

- Per-block CPS® scores across homepage, service pages, and team pages
- Schema audit identifying incorrect types, missing fields, and markup errors
- Share of Voice measurement across ChatGPT, Perplexity, Google AI, Gemini, Copilot
- Hallucination detection — identifying where AI misrepresents the firm
- Competitor citation analysis — which local competitors are being cited instead

Book a full audit: [citedbyai.info](https://citedbyai.info)

---

## Links

- 🌐 [citedbyai.info](https://citedbyai.info)
- 📋 [CPS® Framework](https://github.com/citedbyai/cps-framework)
- 💼 [LinkedIn](https://www.linkedin.com/in/citedbyai/)
- 🐦 [X / Twitter](https://x.com/citedbyai)

---

*CPS® (Citation Probability Score®) and Cited By AI® are registered trademarks of Cited By AI, United Kingdom.*
