# Denis Samoilenko

**Jira and Confluence administrator and automation engineer: ScriptRunner, Automation for Jira and Jira Service Management on Data Center and Cloud, plus AI-assisted tooling for the admin work itself.**

## What I work on

I administer Jira, Confluence and Jira Service Management in a regulated fintech environment, and I build the tooling that keeps a large instance understandable and safe to change.

- **Jira administration on Data Center and Cloud:** workflows, permission and issue security schemes, custom fields and their contexts, project standards.
- **ScriptRunner (Groovy):** validators, conditions and post-functions, listeners, scheduled jobs, UI fragments, and read-only probes against the object model and the database.
- **Automation for Jira:** building rules, auditing them at scale, and repairing the ones that fail quietly.
- **Jira Service Management:** request types, portal forms and customer access.
- **Governance:** configuration audits, clean-up programmes and a clear record of who changed what.
- **AI-assisted administration:** agents that read configuration and audit logs, measure before they conclude, and hand back drafts for a human to approve.

## Selected work

**[council](https://github.com/komsamoilenko/council)**: a local MCP server that lets the AI assistant you are working with consult another vendor's assistant (Claude Code, Codex or the Gemini API) under your own accounts. Consultations run as durable background jobs, and a local ledger records what each one cost. Windows is the implemented platform; MIT licence; releases ship with SHA-256 checksums.

**Restricted-issue helper for Jira Data Center** (publication in preparation): a ScriptRunner web panel that replaces Jira's "You can't view this issue" dead end with a useful card. It tells the person what to ask for and whom to ask, with a ready-to-send message, and decides first whether saying any of that is safe for that person, because on some issues the level name and the people are themselves the confidential part. The client script ships without comments, after two of them once carried a real name into browsers; the build step that strips them is part of the release.

## How I work

- **Measure first.** Before changing configuration I read the current state with read-only probes, and I treat an empty result as a question about the probe before I treat it as a fact about the system.
- **Dry run, then one record, then the batch.** Scripts that write start in dry-run mode, apply to a single record, read it back, and only then run in full.
- **Verified changes.** A change is finished when the live state has been read back and matches what was intended; deployed scripts are compared byte for byte with the built version.
- **Adversarial review.** Significant changes get an independent review whose job is to break them. A second opinion from a different vendor's model is the reason council exists.
- **A way back before a way forward.** Every production change ships with a rollback: the previous version, a kill switch, or a single toggle.

## Writing

I write on LinkedIn about real Jira administration work: ScriptRunner solutions, configuration forensics, governance clean-ups, and where AI tooling earns its place in an administrator's day. Read the posts on [LinkedIn](https://www.linkedin.com/in/komsamoilenko/).

<!-- Optional: once a post is worth pinning here, add it as a bullet, e.g. - [Post title](POST_URL) -->

## Contact

The best way to reach me is [LinkedIn](https://www.linkedin.com/in/komsamoilenko/). For council, please open an issue in the [repository](https://github.com/komsamoilenko/council/issues).
