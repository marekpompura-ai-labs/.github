# Marek Pompura AI Labs

Governance- and security-focused tooling for IBM Db2 and AI assistants.

The premise behind everything here: an AI assistant with database access is
genuinely useful and a genuine risk, and the difference between the two is
whether the **server** enforces the policy or the model is trusted to behave.

## Projects

### [Governed Db2 MCP Server](https://github.com/marekpompura-ai-labs/db2-mcp-server)

A Java 21 Model Context Protocol server that gives AI assistants governed,
read-only access to IBM Db2 — typed MCP tools for schema exploration,
dependency analysis, stored-procedure inspection, reference-data lookup and
bounded diagnostic queries.

AI-generated SQL is treated as untrusted. Read-only access is enforced
independently at the database, connection and application layers; queries
are parsed as an AST rather than pattern-matched, and a schema allowlist
rejects everything not explicitly permitted. Capability profiles decide
which tools the assistant can even discover.

Current release: **[v1.0.1](https://github.com/marekpompura-ai-labs/db2-mcp-server/releases/tag/v1.0.1)**

### Db2 AI Incident Copilot

An incident-analysis client for Db2 environments. In development; it will be
published here.

## How these are built

Every significant decision is written down at the point it was made, with
the alternatives that were rejected and the consequences that were actually
verified — 49 architecture decision records in the MCP server alone,
alongside a threat model, an adversarial test catalogue, and external
reviews with the disposition of every finding recorded, including the ones
that found real defects.

Claims are checked rather than asserted. The build fails on an unverified
licence obligation, on a prohibited dependency reappearing at any nesting
level inside a shipped archive, and on documentation drifting out of step
with the artifact it describes.

## Licensing

Original project material is published under source-available terms:
readable, buildable and runnable by anyone, free for noncommercial use
including by charitable, educational, public research, public safety and
health, environmental and government organizations. Commercial organizations
may evaluate without charge and without a time limit. Commercial deployment
and collaboration are by agreement.

Each repository states its own terms precisely; this is a summary, not a
licence.

## Contact

**Marek Pompura** — [marek.pompura.it@gmail.com](mailto:marek.pompura.it@gmail.com)

Open to collaboration with developers, technical co-founders and partners
interested in turning this work into a product.

## Disclaimer

Db2 is a trademark of IBM. These are independent projects, not affiliated
with, sponsored by, or endorsed by IBM.
