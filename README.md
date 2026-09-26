# Denis Samoilenko

**Jira and Confluence administrator and automation engineer: ScriptRunner, Automation for Jira and Jira Service Management on Data Center and Cloud, plus a self-hosted product analytics platform and the AI-assisted tooling that keeps both understandable and safe to change.**

## What I work on

I administer Jira, Confluence and Jira Service Management in a regulated fintech environment, own the company's self-hosted product analytics platform, and build the tooling that keeps large instances understandable and safe to change.

- **Jira administration on Data Center and Cloud:** workflows, permission and issue security schemes, custom fields and their contexts, project standards.
- **ScriptRunner (Groovy):** validators, conditions and post-functions, listeners, scheduled jobs, UI fragments, and read-only probes against the object model and the database.
- **Automation for Jira:** building rules, auditing them at scale, and repairing the ones that fail quietly.
- **Jira Service Management:** request types, portal forms and customer access.
- **Product analytics platform (self-hosted, iOS, Android and web):** project structure, event taxonomy and its intake gate, the access model, instrumentation audits, ingestion-failure forensics, storage and retention on the event store.
- **Governance:** configuration audits, clean-up programmes and a clear record of who changed what.
- **AI-assisted administration:** agents that read configuration and audit logs, measure before they conclude, and hand back drafts for a human to approve.

## Recent work

- Consolidated a product analytics estate from fourteen projects into two, because a project is a hard data wall, and wrote the access model that came with it: private by default, opened on a measured trigger rather than a judgement call.
- Put an intake gate in front of the event taxonomy, with a registry checked against live events; the first real run found one dimension carried under two names and a rule the team had obeyed for three years that no longer applied.
- Traced three ingestion failures to their mechanism: a feature flag at zero percent plus an app release that silenced a whole platform for a week, twelve days of failures behind a readiness probe that touched nothing, and an install event that can never be recovered because it fails closed with no retry.
- Sized the event store against the vendor's recommended ceiling (the estate runs at roughly two hundred and fifty times it) and worked out what retention can and cannot free.
- Audited a Jira Data Center estate against its own live usage: more than five thousand saved filters, including the broken ones still emailing on a schedule; more than five hundred automation rules against their audit tables, with the failure floods traced to leavers hard-coded inside rules; custom fields, screens and workflows, with every deletion gated on three independent oracles.
- Built the tooling this work runs on: read-only client libraries and probes for both platforms, a production UI harness that clicks every control with writes blocked at the network layer, and a leak gate for anything that leaves the machine.

## How I work

- **Measure first.** Before changing configuration I read the current state with read-only probes, and I treat an empty result as a question about the probe before I treat it as a fact about the system.
- **Dry run, then one record, then the batch.** Scripts that write start in dry-run mode, apply to a single record, read it back, and only then run in full.
- **Verified changes.** A change is finished when the live state has been read back and matches what was intended; deployed scripts are compared byte for byte with the built version.
- **Adversarial review.** Significant changes get an independent review whose job is to break them.
- **A way back before a way forward.** Every production change ships with a rollback: the previous version, a kill switch, or a single toggle.

## Writing

I write on LinkedIn about real administration work: ScriptRunner solutions, configuration forensics, governance clean-ups, running a product analytics platform, and where AI tooling earns its place in an administrator's day. Read the posts on [LinkedIn](https://www.linkedin.com/in/komsamoilenko/).

## Contact

The best way to reach me is [LinkedIn](https://www.linkedin.com/in/komsamoilenko/).
