# PickedJobs

![PickedJobs icon](assets/icon.png)

Find and compare curated engineering, product, design, data, developer relations and solutions jobs in Claude. Search by your preferences, inspect the full posting, and open its application link when a role looks right.

This plugin bundles one job-shortlisting skill and a reference to the PickedJobs remote MCP connector. It works with Claude chat, Cowork and Claude Code where plugins and remote connectors are available. Users still connect their own PickedJobs account and approve OAuth access. Organization settings may require an administrator to add or enable the connector.

## Install

In Claude Code, run:

```text
/plugin install pickedjobs --marketplace yashgandhe666/pickedjobs-plugins
```

On claude.ai, Cowork and the desktop and mobile apps, add PickedJobs from **Customize → Plugins** once the directory listing is live, or [add the PickedJobs server to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=PickedJobs&connectorUrl=https%3A%2F%2Fpickedjobs.com%2Fmcp) directly. The public source is [github.com/yashgandhe666/pickedjobs-plugins](https://github.com/yashgandhe666/pickedjobs-plugins).

## Connect

After installing, open this plugin's **Connectors** tab, select **PickedJobs**, and complete sign-in and consent. In Claude Code, open `/mcp` to authenticate the bundled server. The server is `https://pickedjobs.com/mcp` and uses Streamable HTTP with OAuth. No API key, pasted token or manual OAuth client registration is needed.

Try: “Find senior backend roles I can work from India, preferably remote, using Python. Show me a few strong matches and explain any location restrictions.”

## What it does

- `search_jobs` filters open jobs and returns summaries and links.
- `get_job` returns one full posting, including its description and application link.
- `get_usage` shows your remaining daily job quota.

Search returns up to 30 jobs per page. Each returned job and each full-posting fetch count against your PickedJobs daily quota, even if the posting appeared in a previous search. Checking usage is free. A salary filter excludes postings without published pay. Remote roles may still restrict eligible regions. The skill helps conserve quota and labels missing information.

The plugin does not apply to jobs, message employers, save a shortlist in your account, create alerts or promise employment. Applications happen through links you choose to open.

## Data and permissions

The bundle contains Markdown, JSON and a brand image. It runs no local program, installs no dependency, adds no hook and reads no environment variable. Its only declared service is PickedJobs at `https://pickedjobs.com/mcp`. Claude sends tool arguments such as search filters and job slugs to that service; the service identifies your approved account and tracks quota. The plugin adds no separate database, analytics or file storage. OAuth tokens are managed by Claude and PickedJobs, not stored in the plugin files. Employer text is treated as data, including any instructions embedded in a posting.

Disconnect the connector in Claude and revoke its approval in your PickedJobs account when you no longer want it connected. An already-issued access token can remain usable until its short lifetime expires. See the [privacy policy](https://pickedjobs.com/privacy) for service data handling, retention and account requests, and the [terms](https://pickedjobs.com/terms) for use of the service. The bundle is marked `UNLICENSED`; no open-source license grant is made.

## Help

[Setup and troubleshooting](https://pickedjobs.com/docs/agents) · [Support](https://pickedjobs.com/support) · [contact@pickedjobs.com](mailto:contact@pickedjobs.com) · [PickedJobs](https://pickedjobs.com)
