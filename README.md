# PickedJobs plugins

Install [PickedJobs](https://pickedjobs.com) in your AI assistant and search curated tech jobs from chat: engineering, product, design, data, developer relations and solutions roles pulled straight from company career pages. Each plugin connects to the same OAuth-protected server at `https://pickedjobs.com/mcp` and offers three read-only tools: `search_jobs`, `get_job` and `get_usage`. You sign in with your own PickedJobs account; the plugin never submits applications or changes your account.

This repository is the public source for the installable packages. It contains Markdown, JSON and a brand icon only: no code runs on your machine, and no credentials are included. The maintained copy lives in the private PickedJobs monorepo and is synced here on each release.

## Claude Code

```text
claude plugin install pickedjobs --marketplace yashgandhe666/pickedjobs-plugins
```

Then run `/mcp` inside Claude Code, choose **pickedjobs** and sign in. The plugin adds the `/pickedjobs:find-jobs` skill and the PickedJobs server. Requires Claude Code 2.1.292 or later for the one-step form; on older versions run `claude plugin marketplace add yashgandhe666/pickedjobs-plugins` followed by `claude plugin install pickedjobs@pickedjobs`.

## Claude (web, desktop, mobile, Cowork)

[Add PickedJobs to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=PickedJobs&connectorUrl=https%3A%2F%2Fpickedjobs.com%2Fmcp). Claude opens its **Add custom connector** dialog with the name and URL filled in. Review them, choose **Add**, sign in to PickedJobs and approve access. Workspace owners may need to add the connector for Team and Enterprise members.

The plugin source for Anthropic's directory is [`plugins/pickedjobs`](plugins/pickedjobs). Once the directory listing is approved, that listing replaces this manual step.

## ChatGPT

In ChatGPT, open **Plugins → Add custom MCP server**, name it PickedJobs, paste `https://pickedjobs.com/mcp`, choose **OAuth**, then sign in to PickedJobs and allow access. The OpenAI package in [`openai/pickedjobs`](openai/pickedjobs) is the candidate for OpenAI's plugin directory; until that listing is live, the custom server route above is the supported path.

## Usage and help

Free accounts can fetch 250 jobs per UTC day. Every job returned by a search and every full posting read counts once; checking usage is free. See your usage, disconnect assistants and revoke keys in [Account settings](https://pickedjobs.com/account/settings). Setup details and troubleshooting: [pickedjobs.com/docs/agents](https://pickedjobs.com/docs/agents). Support: [contact@pickedjobs.com](mailto:contact@pickedjobs.com).

[Privacy](https://pickedjobs.com/privacy) · [Terms](https://pickedjobs.com/terms) · [Support](https://pickedjobs.com/support)
