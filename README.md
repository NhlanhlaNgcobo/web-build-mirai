# Mirai Stack — premium site (demo)

A single-page, premium dark site for Mirai Stack: hero, services, projects, process, an
instant project **estimator**, a working **booking** flow, and a scripted **"Ask Mirai"**
assistant. Static — no build step, no backend, no API keys.

## What's interactive

- **Estimate your project** — pick build type, size, complexity, features, and timeline; an
  indicative investment range + timeline updates live. Clearly labelled as an estimate, not a quote.
- **Book a discovery call** — a demo booking form. On submit it saves locally, shows a
  confirmation, and offers "Email this request" (opens a pre-filled email to
  info@miraistack.co.za) and "Add to calendar" (.ics download).
- **Ask Mirai** — a keyword-based FAQ assistant answering common questions about services,
  process, stack, pricing, and booking. No external calls.

## Run locally

Open `index.html` in a browser, or serve it:

```bash
npx serve .
```

## Deploy

Static site — deploys to Vercel as-is:

```bash
npx vercel --prod
```

## Notes

- The estimator figures (ZAR) are **placeholders** — edit the `BASE`, `PERUNIT`, and `FEAT`
  tables in the inline script to match real pricing.
- To make the booking actually deliver to an inbox (instead of opening a draft email), add a
  form backend (a Vercel serverless function or a service like Formspree/Resend).
- To upgrade "Ask Mirai" to live AI answers, add a serverless function that calls the
  Anthropic API and point the assistant's `ask()` at it.
