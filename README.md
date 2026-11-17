# GTM Brain sample sales data

A fictional sales operation selling GTM Brain setup, training and handover. The CRM, calls, emails and research refer to the same companies and people, so you can follow an account across sources.

**[Download the dataset as a ZIP](https://github.com/gtm-week/berlin-codex-dummy/archive/refs/heads/main.zip).** Unzip it and use the CSV and Markdown files directly. No installation or connectors are required.

**Using this with Codex?** Read [More context for Codex](#more-context-for-codex) for the business scenario, people, account stories and how to interpret the sources.

![Dataset map: product context and sales materials alongside CRM, calls, emails, research and exclusions. The same Alderpath account connects the sources.](docs/dataset-map.png)

## What's inside

| Folder | Contents | What it tells you |
|---|---|---|
| [product/](product/) | GTM Brain brief, website copy and documentation excerpt | What we sell, what it can do and its limits |
| [data/crm/](data/crm/) | 30 company records, 45 contacts, 18 deals and seller owners | Who we know, their roles, deal stages and next steps |
| [data/transcripts/](data/transcripts/) | 8 sales-call transcripts | Problems, objections, buying criteria and onboarding needs |
| [data/email/](data/email/) | 10 email threads | Introductions, follow-ups, stakeholder changes and timing updates |
| [data/web/](data/web/) | 12 fictional company-page extracts | What an account does, its team and hiring signals |
| [data/prospecting/](data/prospecting/) | The same 15 prospects before and after research | Missing information and what the research adds |
| [data/enrichment/](data/enrichment/) | 15 prepared results: 10 matched, 3 unmatched, 2 ambiguous | Contact matches and unresolved identities |
| [data/operators/](data/operators/) | 18 exclusion records | Existing customers, active opportunities and do-not-contact accounts |
| [content/](content/) | Sample offer, two posts, outreach example, voice guidance and brand assets | Material to adapt when drafting offers and content |

The 18 deals are split evenly: **New lead, Discovery, Evaluation, Proposal, Won and Lost**, with three in each stage. Accounts include SaaS teams, agencies and consultancies with different existing stacks.

## How the files connect

The company is the shared reference. Its contacts and deals point to its CRM record; calls, emails and company pages identify the same account. [source-index.csv](data/source-index.csv) lists each conversation or page, its date and the file that contains it.

**Example: Alderpath Systems**

| Source | What it adds |
|---|---|
| [Companies](data/crm/companies.csv), [contacts](data/crm/contacts.csv) and [deals](data/crm/deals.csv) | The account, people involved, proposal stage and next step |
| [Discovery call](data/transcripts/t01-alderpath.md) | Why the team needs help and what a useful pilot would do |
| [Email thread](data/email/e01-alderpath.md) | The follow-up and stakeholder involvement |
| [Company page](data/web/w01-alderpath.md) | What the company does |

Read these together to prepare an account brief or a relevant offer. Product documents explain what you can offer; the content folder supplies examples to adapt.

For joins, use `company_id` across tables and `contact_id` for people. Deals use `primary_contact_id`. The [schema](data/SCHEMA.md) explains the fields; the [source map](SOURCE-MAP.md) shows which tools the files stand in for.

## What to expect in the data

There are 30 company records representing **29 businesses**, including one intentional duplicate. Some budgets and buying-authority fields are empty because they are unknown. A contact's enthusiasm does not mean they can approve a purchase.

The files also include an older CRM note superseded by a later email, a stalled evaluation, a customer needing onboarding help, a lost deal with a stated reason and one incomplete transcript. Dates and missing information are part of the account history.

## What's real and what's fictional

Customer companies, people, conversations, activity and commercial terms are fictional. Addresses use `.example` domains. Do not send to or run live enrichment on them.

GTM Brain product context comes from the sources listed in [product/source-provenance.md](product/source-provenance.md). The sample EUR 2,400 service offer is fictional, not official product pricing. No customer results are claimed.

**Snapshot: 16 November 2026.** These are simple sample schemas, not native exports from the named tools.

## More context for Codex

### Your role and the business

You are helping the seller's GTM team understand its market and move suitable accounts forward. The team already has prospects, open opportunities, customers and lost deals. Use that history to answer the user's specific task: who to target, what an account needs, what to do next, or what material to create.

GTM Brain is the real product used in this fictional scenario. The included documentation describes an open-source plugin that keeps company context, evidence and reusable working methods across agent chats and projects. Read the [product brief](product/gtm-brain-brief.md) for capabilities and limits. This repository supplies sample business inputs; using it does not require installing the product.

The fictional commercial offer is help adopting that way of working: scope one workflow, prepare account briefs from approved sources, run two training sessions and hand over a method the team can repeat. The [sample offer](content/sample-offer.md) is EUR 2,400 before tax and covers five briefs. Individual deals can have different scopes and amounts. These are one-off services, not software subscriptions or official GTM Brain prices.

### Who we sell to and why they care

The starting audience is B2B SaaS teams, agencies and consultancies. Treat this as a targeting hypothesis to assess from the data, not a validated ICP.

These teams already have tools. Typical stacks include HubSpot or Attio, Gmail, Granola, Notion and Drive; larger accounts use Salesforce, Outlook, Teams and SharePoint. Their recurring problems are:

- Sellers reconstruct account history before every meeting.
- A newer decision is buried in an email while an old summary remains in the CRM.
- Research loses its reasoning when it passes to another colleague.
- Teams copy a previous brief and accidentally carry over another account's facts.
- A useful demonstration never becomes a repeatable routine with a clear owner.

The proposed value is a brief with traceable evidence and a working method colleagues can reuse. The dataset does not establish measured time savings, revenue gains or a need to replace the existing CRM.

### Who is involved

Lena Ortiz, Samir Hale and Jo Chen are the fictional sellers. Their names appear as CRM owners and in conversations. The 45 contacts are on the prospect/customer side and include users, internal supporters, approvers and reviewers. A primary contact is not necessarily the person who can approve spending.

Eight accounts have both a call and an email thread. These summaries orient you; read the linked sources before making a recommendation.

| Account and stage | People | Situation and evidence |
|---|---|---|
| Alderpath Systems - Proposal | Mira Stein, Head of RevOps; Elias Brandt, VP Sales | Five sellers assemble account history across several tools. Mira wants a five-account trial; Elias must approve spending. [Call](data/transcripts/t01-alderpath.md), [email](data/email/e01-alderpath.md). |
| Brindle Growth - Evaluation | Jonas Vale, GTM Engineer; Iris Bloom, Managing Director | Jonas wants a consistent method across client teams but cannot buy it. Iris joins the review; budget and client-data access remain unapproved. [Call](data/transcripts/t02-brindle.md), [email](data/email/e02-brindle.md). |
| Cobalt Ledger - Evaluation | Rhea Malik, RevOps Lead; Nolan Price, IT Director | The meeting-brief use case is relevant, but IT needs the data flow and permissions explained. An infrastructure migration delays review; no start date is approved. [Call](data/transcripts/t03-cobaltledger.md), [email](data/email/e03-cobaltledger.md). |
| Dovetail Route - Won | Anika Frost, Sales Operations Manager; Tomas Birch, VP Revenue | Tomas accepted the engagement. Anika is coordinating source preparation, but training and adoption have not happened yet. [Call](data/transcripts/t04-dovetailroute.md), [email](data/email/e04-dovetailroute.md). |
| Emberlane Advisory - Lost | Soren Reed, founder; Maya Finch, consultant | The nine-person consultancy cannot allocate an internal owner. Soren says price is not the main blocker and asks to stop active follow-ups. [Call](data/transcripts/t05-emberlane.md), [email](data/email/e05-emberlane.md). |
| Fjordline Metrics - Discovery | Leonie Hart, Revenue Enablement Lead; Omar Lind, CRO | Account managers need the latest approved decisions. The recording misses budget and sign-off discussion; the email confirms both remain unknown. Omar's title does not establish his authority for this purchase. [Call](data/transcripts/t06-fjordlinemetrics.md), [email](data/email/e06-fjordlinemetrics.md). |
| Grovebridge Labs - Proposal | Marta Voss, Head of Sales Enablement; Felix Rowan, VP Sales | The CRM and call retain a tentative November start. The later email moves the earliest possible window to the week of 11 January 2027, still subject to scope and budget approval. [Call](data/transcripts/t07-grovebridge.md), [email](data/email/e07-grovebridge.md). |
| Harborwell Studio - Discovery | Theo Marin, agency partner; Sofia Crane, Delivery Director | Research loses its reasoning between strategy and outreach. They want three briefs for one client, a repeatable method and an outreach draft. Sofia owns delivery; Theo decides whether to buy. [Call](data/transcripts/t08-harborwell.md), [email](data/email/e08-harborwell.md). |

The remaining deals have thinner histories. Pinecrest Flow has an [inbound email](data/email/e09-pinecrestflow.md); Morrowfield Cloud has a [Finance scope discussion](data/email/e10-morrowfield.md). Other records add new leads, evaluations, wins and losses. Do not invent conversations for them. Not every company has a deal, transcript or website extract.

### How to use the evidence

Start with the product brief and [schema](data/SCHEMA.md), then select the files relevant to the task. For an account, join its company, contacts and deal records, and use [source-index.csv](data/source-index.csv) to find its calls, emails and page extracts. Product and writing guidance apply across accounts; customer facts stay attached to their account.

- Read dates against the fixed 16 November 2026 snapshot. A scheduled future step is not evidence it happened, even if today's date is later.
- Compare conflicting statements by date, speaker and what was actually confirmed. Explain the change and cite both sources. A newer email can change timing without changing the deal stage.
- Empty budget or authority fields mean unknown. A proposed fee is not an approved budget. Won records establish fictional commercial acceptance, not payment, adoption or customer results.
- The transcript gap stays missing. Prepared enrichment can identify a contact but cannot prove need, authority or permission to contact them.
- Check exclusions by company ID and domain before recommending outbound prospects. The duplicate company record can otherwise bypass the filter.
- Use the supplied fictional website extracts and enrichment results. Do not browse, enrich or contact the invented identities. Keep this scenario separate from any connected real CRM or company knowledge store.

### What a useful result looks like

Follow the user's requested task; do not run every analysis by default.

| Task | Useful result |
|---|---|
| Define an ICP or shortlist prospects | Explain the recurring need and evidence for fit, distinguish fit from current buying readiness, and apply exclusions. |
| Prepare an account brief or next action | State the problem, relevant people, latest decision, blocker, unknowns and proposed next step, with source links or IDs. |
| Draft an offer or follow-up | Use that account's scope, language and decision process. Keep proposed terms separate from what the buyer accepted. |
| Turn a method into a reusable skill | Keep the instructions reusable and load each account's evidence separately. Check it on a second account. |
| Draft content or a lead magnet | Use recurring problems from the calls and the supplied voice guidance. Label fictional examples. For a calculator, expose editable assumptions and distinguish estimated effort from hypothetical savings. |

Separate what the sources say, what you infer and what you recommend. Cite the file or source ID for material claims and name missing information that could change the recommendation. All outreach remains a draft.
