# Awesome Invoicing [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of invoicing and e-invoicing tools for freelancers and small businesses — with a focus on **free**, **standards-compliant**, and **AI-native** options.

Sending an invoice sounds simple until you factor in tax rules, formatting standards, and the growing number of countries that now mandate structured **e-invoicing** (EN 16931, XRechnung, ZUGFeRD, Peppol BIS, Factur-X). This list collects the tools worth knowing — from no-signup PDF generators to compliance networks to the new wave of AI-native invoicing that runs inside assistants like Claude and ChatGPT.

Everything here is a real, usable tool that a solo freelancer or a small business could adopt today. Enterprise-only compliance platforms are listed separately for reference.

## Contents

- [How to choose an invoicing tool](#how-to-choose-an-invoicing-tool)
- [Comparison matrix](#comparison-matrix)
- [AI-native & conversational](#ai-native--conversational)
- [Free invoice generators](#free-invoice-generators)
- [E-invoicing & compliance (EU / Germany)](#e-invoicing--compliance-eu--germany)
- [Freelancer & small-business suites](#freelancer--small-business-suites)
- [Enterprise compliance networks](#enterprise-compliance-networks)
- [Standards glossary](#standards-glossary)
- [Contributing](#contributing)

## How to choose an invoicing tool

Most invoicing tools are variations on four questions. Decide which of these matter to you before picking, because very few tools do all four well:

- **Is it free — actually free, forever?** Many "free" tools cap you at 3 clients or 5 invoices a month, then require an upgrade. A true free-forever tool has no such wall.
- **Is it standards-compliant?** If you invoice public-sector or business customers in the EU, you increasingly *must* send a structured e-invoice conforming to **EN 16931** — in Germany that means **XRechnung** or **ZUGFeRD**; across the EU, **Peppol BIS**; in France, **Factur-X**. A pretty PDF is not the same as a compliant e-invoice. (No such mandate exists for US domestic invoicing.)
- **Is it AI-native?** A new category of tools lets you create an invoice by *asking* — through a Model Context Protocol (MCP) server, an assistant skill, a CLI, or a chat interface — instead of filling out a web form. Distinct from tools that merely bolt an "AI assistant" onto a traditional app.
- **Can you start without signing up?** No-signup tools let you produce an invoice in seconds; account-based tools trade that friction for saved clients, history, and payment tracking.

Tools below are tagged so you can scan for the combination you need.

## Comparison matrix

Legend: ✅ yes · ⚠️ partial or conditional · ❌ no

| Tool | Free forever | EN 16931 e-invoicing | Conversational / AI-native | No signup to start | Surfaces |
|------|:---:|:---:|:---:|:---:|---|
| [Scribo](https://causa-prima-scribo.vercel.app/) | ✅ | ✅ | ✅ | ✅ | Web · API · MCP · Skill · CLI |
| [einvoice-mcp](https://glama.ai/mcp/servers/makririch/einvoice-mcp) | ✅ | ✅ (XRechnung) | ✅ | ✅ | MCP |
| [Mavri](https://mavri.nodedr.com/) | ✅ | ⚠️ (exports only; not validated) | ✅ (MCP) | ❌ (local owner account) | Web · API · MCP |
| [Invoice My Clients MCP](https://www.invoicemyclients.com/features/mcp-server) | ❌ | ❌ | ✅ | ❌ | MCP · Web |
| [Zoho Invoice](https://www.zoho.com/invoice/) | ✅ | ❌ | ⚠️ in-app (Zia) | ❌ | Web · API · Mobile |
| [sevDesk](https://sevdesk.de) | ⚠️ generator only | ✅ | ❌ | ⚠️ generator only | Web · API |
| [Lexware Office](https://www.lexware.de/lexware-office) | ❌ | ✅ | ⚠️ community MCP | ❌ | Web · API |
| [easybill](https://www.easybill.de) | ✅ (50 docs/mo) | ✅ | ❌ | ❌ | Web · API |
| [PDF24 e-invoice](https://tools.pdf24.org/de/elektronische-rechnung-erstellen) | ✅ | ✅ | ❌ | ✅ | Web |
| [kostenlose-erechnung.de](https://kostenlose-erechnung.de/xrechnung-generator/) | ✅ | ✅ | ❌ | ✅ | Web |
| [B2Brouter](https://www.b2brouter.net/) | ✅ (SMB tier) | ✅ | ❌ | ❌ | Web · API |
| [Qonto](https://qonto.com/de) | ⚠️ with account | ✅ | ❌ | ❌ | Web · API · Mobile |
| [Wave](https://www.waveapps.com/) | ✅ | ❌ | ❌ | ❌ | Web · Mobile |
| [PayPal Invoicing](https://www.paypal.com/us/business/accept-payments/invoice) | ✅ | ❌ | ❌ | ⚠️ PayPal account | Web · API · Mobile |
| [Invoice Simple](https://www.invoicesimple.com/invoice-generator) | ⚠️ freemium | ❌ | ❌ | ✅ | Web · Mobile |
| [FreshBooks](https://www.freshbooks.com/) | ❌ | ❌ | ⚠️ light | ❌ | Web · API · Mobile |
| [Bonsai](https://www.hellobonsai.com/) | ❌ | ❌ | ⚠️ light | ❌ | Web · Mobile |

## AI-native & conversational

Tools you operate by asking, rather than by filling out a form — via MCP servers, assistant skills, CLIs, or dedicated chat interfaces.

- **[Scribo](https://causa-prima-scribo.vercel.app/)** — Free, conversational e-invoicing that generates EN 16931–compliant invoices (ZUGFeRD, XRechnung, Peppol BIS) from natural language. Runs as an MCP server, a Claude skill, a CLI, a public API, and a web app — no signup required to create your first invoice. `Free forever` `EN 16931` `MCP` `Skill` `CLI` `No signup`
- **[einvoice-mcp](https://glama.ai/mcp/servers/makririch/einvoice-mcp)** — Open-source MCP server that creates and validates German XRechnung e-invoices from an assistant. `Free` `EN 16931` `MCP`
- **[Mavri](https://mavri.nodedr.com/)** — Self-hosted invoicing and quote app with an MCP server and REST API; exports UBL 2.1 and XRechnung, but does not validate generated files for jurisdictional compliance ([source](https://github.com/Raktim94/mavri)). `Free` `MCP` `API`
- **[Invoice Generator MCP (M1Vision)](https://smithery.ai/server/@M1Vision/invoice-mcp)** — MCP server that turns natural-language requests into PDF invoices; published on Smithery. `Free` `MCP`
- **[invoice-mcp (markslorach)](https://github.com/markslorach/invoice-mcp)** — MCP server that generates PDF invoices from natural language with an editable template. `Free` `MCP`
- **[Invoice My Clients MCP](https://www.invoicemyclients.com/features/mcp-server)** — MCP server bundled with a hosted SaaS; create invoices and log billable hours from an assistant. `Paid` `MCP`
- **[Zoho Invoice](https://www.zoho.com/invoice/)** — Forever-free invoicing with in-app AI (Zia) for natural-language invoice creation and reminders; part of the wider Zoho suite. `Free forever` `In-app AI` `API`
- **[Jenova AI](https://www.jenova.ai/en/resources/ai-invoice-generator)** — General AI agent platform with an invoice-generation capability; web-based, no external assistant integration. `Free` `Web`
- **[HubSpot AI Invoice GPT](https://www.hubspot.com/invoice-template-generator/ai-invoice-gpt)** — HubSpot-branded invoice GPT on the OpenAI GPT Store. `Free` `GPT Store`
- **[Poe — InvoiceGenerator](https://poe.com/InvoiceGenerator)** — Invoice-creation bot on Poe. `Free` `Poe`
- **[Invoicer.ai](https://invoicer.ai/)** — Web SaaS pairing an AI invoice generator with an AI expense manager. `Paid` `Web`

## Free invoice generators

No-signup or free-tier tools for quickly producing a PDF invoice. Most are US/global and produce a formatted document rather than a compliant structured e-invoice.

- **[invoice-generator.com](https://invoice-generator.com/)** — The canonical no-signup, no-watermark online invoice generator, from Invoiced. `Free` `No signup`
- **[Invoice Simple](https://www.invoicesimple.com/invoice-generator)** — Widely-used free generator and top-ranked mobile app with no-signup PDF download. `Freemium` `No signup` `Mobile`
- **[Wave](https://www.waveapps.com/)** — Genuinely free invoicing plus bookkeeping, backed by H&R Block; one of the most complete free-forever options in the US. `Free forever`
- **[PayPal Invoicing](https://www.paypal.com/us/business/accept-payments/invoice)** — Free invoicing inside a PayPal merchant account, with payment collection built in. `Free` `Payments`
- **[Canva Invoices](https://www.canva.com/invoice/)** — Template-driven invoices inside Canva; strong on design, requires a Canva account. `Free` `Templates`
- **[Wise Invoice Generator](https://wise.com/us/invoice-generator/)** — Free no-signup invoice templates aimed at cross-border freelancers. `Free` `No signup`
- **[SumUp Invoices](https://www.sumup.com/en-gb/invoices/)** — Mobile-first invoicing inside SumUp's payment ecosystem (formerly Debitoor). `Free` `Payments` `Mobile`

## E-invoicing & compliance (EU / Germany)

Tools that produce structured, standards-compliant e-invoices — required for public-sector and, increasingly, B2B invoicing across the EU.

- **[kostenlose-erechnung.de](https://kostenlose-erechnung.de/xrechnung-generator/)** — Free, no-signup XRechnung and ZUGFeRD generator with Leitweg-ID support. `Free` `EN 16931` `No signup` `🇩🇪`
- **[PDF24 e-invoice generator](https://tools.pdf24.org/de/elektronische-rechnung-erstellen)** — Free no-signup ZUGFeRD and XRechnung generator from the well-known German PDF-tools brand. `Free` `EN 16931` `No signup` `🇩🇪`
- **[xrechnung-erstellen.com](https://xrechnung-erstellen.com/)** — Free XRechnung generator with assisted data extraction. `Free` `EN 16931` `🇩🇪`
- **[easybill](https://www.easybill.de)** — Cloud invoicing for SMEs and marketplace sellers, with a meaningful free tier (50 documents/month) and full e-invoice support. `Free tier` `EN 16931` `API` `🇩🇪`
- **[sevDesk](https://sevdesk.de)** — Popular German cloud invoicing and accounting suite; also runs a free public e-invoice generator. `Paid` `Free generator` `EN 16931` `🇩🇪`
- **[Lexware Office](https://www.lexware.de/lexware-office)** — Market-leading German cloud accounting and invoicing suite; a community MCP server exists. `Paid` `EN 16931` `API` `🇩🇪`
- **[Accountable](https://www.accountable.de)** — English-first freelancer tax and invoicing app with native EN 16931 support; strong in Germany and Belgium. `Freemium` `EN 16931` `🇩🇪` `🇧🇪`
- **[Norman Finance](https://norman.finance)** — English-friendly accounting and invoicing for German freelancers, with a free tier. `Free tier` `EN 16931` `🇩🇪`
- **[Papierkram](https://www.papierkram.de)** — German accounting with a project- and time-tracking-led invoicing workflow; free tier available. `Free tier` `EN 16931` `🇩🇪`
- **[B2Brouter](https://www.b2brouter.net/)** — Peppol Access Point with a free portal for SMEs and freelancers, plus a public REST API. `Free tier` `EN 16931` `Peppol` `API`
- **[Storecove](https://www.storecove.com/)** — Developer-first Peppol Access Point with a RESTful JSON API and a free sandbox. `Paid` `Peppol` `API`
- **[Qonto](https://qonto.com/de)** — EU SMB neobank bundling a compliant e-invoicing module into its business account. `Paid` `EN 16931` `Banking` `API`

## Freelancer & small-business suites

Broader tools where invoicing is one feature among CRM, contracts, time-tracking, or payments. Mostly US-focused; strong brands, generally paid.

- **[FreshBooks](https://www.freshbooks.com/)** — Cloud invoicing and accounting built for freelancers and service businesses; one of the largest SMB accounting brands. `Paid` `API`
- **[Bonsai](https://www.hellobonsai.com/)** — All-in-one freelancer operations: contracts, proposals, invoicing, and time tracking. `Paid`
- **[HoneyBook](https://www.honeybook.com/)** — Client-flow CRM and invoicing for service entrepreneurs, with strong in-app AI. `Paid` `In-app AI`
- **[Harvest](https://www.getharvest.com)** — Time tracking with built-in invoicing; long-standing, with a real free tier. `Free tier`
- **[Indy](https://weareindy.com/)** — All-in-one freelancer suite with a genuine free tier and AI assistance for contracts and proposals. `Free tier`
- **[Square Invoices](https://squareup.com/us/en/invoices)** — Free invoicing tied to the Square payments ecosystem. `Free` `Payments`
- **[Zoho Invoice](https://www.zoho.com/invoice/)** — See [AI-native & conversational](#ai-native--conversational); notable here for its forever-free plan. `Free forever` `API`

## Enterprise compliance networks

Reference only — enterprise-grade e-invoicing and Peppol networks, generally sold to larger organizations rather than freelancers or small businesses.

- **[Pagero](https://www.pagero.com/)** (Thomson Reuters) — Global e-invoicing network and Peppol-certified service provider. `Enterprise` `Peppol`
- **[Sovos](https://sovos.com/)** — Tax and e-invoicing compliance cloud across 65+ countries. `Enterprise`
- **[Basware](https://www.basware.com/)** — Large purchase-to-pay and e-invoicing network. `Enterprise` `Peppol`
- **[Avalara E-Invoicing](https://www.avalara.com/us/en/products/e-invoicing.html)** — E-invoicing and live reporting layered on Avalara's tax-compliance platform. `Enterprise` `API`
- **[Tradeshift](https://tradeshift.com/)** — Cloud platform for e-invoicing, AP automation, and global compliance. `Enterprise`

## Standards glossary

- **EN 16931** — The European standard defining the semantic data model of a compliant electronic invoice. Most EU e-invoicing formats are compliant implementations of it.
- **XRechnung** — The German XML-based e-invoice format for public-sector (and increasingly B2B) invoicing.
- **ZUGFeRD** / **Factur-X** — Hybrid formats that embed structured XML inside a human-readable PDF/A-3 (Factur-X is the French equivalent, technically aligned with ZUGFeRD).
- **Peppol BIS** — The pan-European delivery network and business specification for exchanging e-invoices between trading partners.

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Please suggest tools that a freelancer or small business could actually use, and keep descriptions neutral and factual. Spotted an error or a missing tool? Corrections to any entry are welcome via pull request.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

To the extent possible under law, the maintainers have waived all copyright and related or neighboring rights to this work.
