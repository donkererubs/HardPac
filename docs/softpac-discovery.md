# SoftPac discovery log

Everything we learn about SoftPac (Softpak), the client (ITL B.V.), and the
candidate foundation (Fluxzero). Facts are dated and sourced; analysis belongs
in `decisions/`.

Sources consulted: softpak.nl (+ product pages), fluxzero.io (+ /docs),
itlbv.com. Last update: 2026-09-03.

---

## The cast

### Softpak B.V. — the incumbent vendor (`softpak.nl`)
Ridderkerk (NL), ~45+ years serving the logistics sector. One of the Dutch
"logistics software giants". Suite of modular, patch-updated products:

| Product | What it does |
|---|---|
| **CDS** Customs Declaration System | Electronic import/export/transit declarations to Dutch & Belgian customs (DMS, IDMS/EDMS, NCTS/DVA, AES, EMCS, NVWA, KvK certificates of origin, T2L(F), fiscal representation, excise AC4, bonded warehouse). Comms via Digipoort, Crossroad, Descartes — or ISDN lines (legacy signal). |
| **ProStore** (WMS) | Warehouse management for LSPs; niches: refrigerated/frozen, metals, excise goods, hazardous substances, liquids, general cargo, bulk/breakbulk. |
| **ProFor** (Freight Forwarding) | The forwarder's system: sea/air/road/rail, groupage, intermodal, multimodal; quotations → files; invoicing (PDF/UBL, consolidated, mirror recharge); tariff management; document mgmt; workflow/planboards; time & labour; XML/EDI import-export; customer track & trace portal; driver mobile QR app w/ POD + CMR; integrations: Portbase (incl. CargoController, Secure Chain), NxtPort, Dockflow, Cargonaut (eAWB), Transporeon. Integrates with CDS & ProStore. |
| **ProLine** | Liner & liner agency system for shipping companies / shipbrokers. |
| **ProTerm TOS** | Terminal operating system for container terminals (ship/train/truck moves, real-time dashboards). |
| **ProTerm Depot & Repair** | Container depot M&R: intake, damage inspection, repair process. |

Other signals: patch-download model per product (helpdesk portal, manuals per
customs procedure, FAQ pages); "works closely with Microsoft Office"; recently
Peppol-ready e-invoicing (2025). Notable CDS customers: DFDS, Stena Line, P&O
Ferrymasters, Vopak, KGH, Varo Energy. ProFor customers: Mitsubishi Logistics
Europe, VDH, LCL Logistics, Kreglinger, Thermotraffic, etc.

**Read on it:** old, expensive, and "immovable" (user, 2026-09-03) — desktop-era
architecture with patch updates, locked data, custom-change friction.

### ITL B.V. — the client (`itlbv.com`)
International forwarder, Moerdijk (NL), Plaza 6. "A fresh approach in transport".

- **Focus:** EU road transport via a certified partner carrier network; also
  container trucking, special/project transport, warehousing.
- Sister company of the **Euro-Rijn group** (ER Logistics branding on site 2026).
- MD: Edwin Koetsenruijter.
- Existing group app: **Eurorijn** driver app (iOS/Android, `nl.circle.eurorijn`).
- Testimonials: DFDS, Henk de Jong, Rene de W, "Charter".
- Softpak product used: **not yet confirmed** — most plausible is ProFor
  (transport/quotation/invoicing/POD surface) possibly with CDS; MUST confirm in
  interview (which modules, seat count, since when).

### Fluxzero — candidate foundation (`fluxzero.io`)
"The production-ready foundation for AI" — a cloud runtime that removes backend
plumbing so you (and AI agents) write only product logic.

- **Model:** write **messages + handlers** in clean **Java/Kotlin**; runtime
  provides delivery, routing, persistence, retries, scheduling, search,
  event-sourcing, auditing, auth/permissions, access control, backpressure,
  observability. No DBs/queues/containers to run locally; given–when–then tests.
- **Deploy:** zero-ops — push to Fluxzero Cloud via GitHub Action/API, or
  self-host ("bring your own infrastructure"); same code either way.
- **AI-first:** built so LLM agents (Claude Code, Codex, Cursor) generate real
  features; product code is a clean Java codebase a human team can take over.
- **Trust signals:** European-built/operated, ISO 27001 + SOC 2 Type 2
  infrastructure, 99.9% uptime target, claims of −90% token spend; customers
  incl. **Portbase** (Dutch port community system — logistics-adjacent), Zoef,
  OpenVoy, Flowmaps, Moxi.
- **Cost:** free to build, pay when you go live. Data export supported.
- **Not covered by Fluxzero:** the UI layer (web/mobile is ours to build).

---

## Interview backlog — questions for the client (and for you)

### Incumbent reality (Softpak)
- [ ] Which Softpak modules does ITL actually run today — ProFor? CDS? ProStore? Since when, how many seats/departments?
- [ ] What does it cost annually (licenses, support, per-patch, per-seat)? What makes it "expensive"?
- [ ] Where does it physically run (ITL servers? Softpak-hosted? per-site installs)?
- [ ] What do the daily workflows look like — which screens do operators live in (quotes → transport file → planning → POD → invoicing)?
- [ ] Concrete pain points: patch cadence/forced updates, refused custom changes, clunky UI, reporting locked (Power BI data access? "data analysts have access" per Softpak), print/PDF workflows, no modern API?
- [ ] What does "immovable" mean operationally: no data export? no API? customizations that would be lost? partner/carrier integrations locked in?
- [ ] Who is the Softpak contact/account manager, and what is the contractual exit path (notice period, data ownership)?

### Scope & ambition
- [ ] Replace the whole suite or start with the forwarding core (quotes → file → POD → invoice)? Where is customs handled (ITL itself vs broker)?
- [ ] Who are the end users and how many: planners, sales, finance, warehouse, drivers, customers (portal)?
- [ ] What must be *parity* on day 1 vs what is the *dream* (the "why now")?
- [ ] Is the **Eurorijn driver app** in scope (replace/connect/reuse)? Who owns/built it (`nl.circle.*`)?
- [ ] Group angle: is this ITL-only or does Euro-Rijn / ER Logistics matter (multi-company design)?
- [ ] Regulatory surface: e-invoicing (UBL/Peppol — mandatory trajectory in NL/EU), customs channels (Digipoort etc.), CMR/POD retention, GDPR on customer & driver data.

### Data
- [ ] Where does the history live (SQL Server? file shares?), how far back, what must migrate vs archive?
- [ ] Master data: customers, carriers/partners, tariffs, rates — size and quality?

### Integrations & ecosystem (from ProFor's public feature set — which apply to ITL?)
- [ ] Portbase / NxtPort / Dockflow (sea files, cargo visibility)? Transporeon (carrier tendering/orders)? Cargonaut (air)? Probably low for a road forwarder — confirm.
- [ ] EDI/XML with customers & carriers — which partners, which formats?
- [ ] Accounting package link (UBL/Peppol invoicing, purchase invoice matching)?
- [ ] Track & trace portal needs for ITL's customers; POD (photo/signature/CMR) capture today — app or paper?

### Fluxzero fit (for us to validate, partly with Fluxzero)
- [ ] Pricing model when live (per app? per user? throughput?) and contract terms; EU data residency guarantees in writing.
- [ ] Building EDI/Peppol/Digipoort-style channels: plain handlers/messages in our code, or does Fluxzero provide connectors?
- [ ] Multi-company/multi-tenant design for a possible group rollout.
- [ ] Frontend strategy on top of Fluxzero (web app for planners? portal? mobile for drivers?).
- [ ] How do long-running human workflows (file lifecycle, approvals) map onto message/handler + event sourcing?
- [ ] Reference call with a logistics-ish customer (Portbase?) or their team on rebuild projects.

### Process / commercial (for you)
- [ ] Kick-off date, timeline ambition, budget frame, who signs off at ITL.
- [ ] Who is the daily sparring partner at the client (ops lead? MD? office manager?).
- [ ] Proposal: how we structure discovery → prototype → pilot (e.g., one workflow end-to-end as the first vertical slice).
