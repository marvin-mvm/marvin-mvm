# Marvin

I build production systems where AI does real work under real constraints — budgets, compliance rules, human approval gates. Most of what I ship is the unglamorous part: the state machines, ledgers, and guardrails that make autonomous pipelines safe to leave running.

## Selected work

**[content-engine](https://github.com/marvin-mvm/content-engine)** — an autonomous social-content production system that ran daily for a DTC brand in a regulated vertical. The parts I care about: a single Red/Yellow/Green claims authority consulted by every layer instead of per-step filters; a credit-first state machine where the only paid generation step sits behind human concept approval; an append-only decision ledger that steers future generation away from rejected work. Python, Telegram review gates, launchd scheduling. *(Debranded public edition of a client system.)*

**[resinmind](https://github.com/marvin-mvm/resinmind)** — a full-stack SaaS for epoxy-resin artists that outgrew its subscription model and had to migrate to a credit economy mid-flight: internal wallet ledger, vouchers with redemption analytics, dual payment processors (PayPal + Xendit), 43 Supabase edge functions. All AI features are metered server-side — the client never computes entitlement.

**[aimeo](https://github.com/marvin-mvm/aimeo)** — AI personas generated from a person's public footprint, searchable and chattable. The recurring lesson in its history: LLM output drift is solved with schema-validated contracts and rule enforcement, not better prompts. Includes two-step social verification so a persona can only be claimed by its subject.

**[lead-pipeline](https://github.com/marvin-mvm/lead-pipeline)** — a small scraping-to-CRM pipeline whose design position is that a bad record is worse than no record: a 5-source phone waterfall, identity-based dedup, and a permanent no-result ledger, with the full operating spec written as an executable contract an agent can run unattended.

## How I work

Heavy use of AI coding agents (Claude Code, Lovable), which is exactly why the interesting problems shift to the boundaries: what the agent may do without asking, where money gets spent, what a human must approve, and how the system proves it followed the rules. The repos above are curated to milestone commits; the working histories were much noisier.

**Stack:** Python · TypeScript/React · Supabase (Postgres/RLS, edge functions) · payment APIs (PayPal, Xendit) · LLM APIs (Anthropic, Gemini, OpenRouter) · scraping/enrichment (Firecrawl, Apify, SearchAPI)
