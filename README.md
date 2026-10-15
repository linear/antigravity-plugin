<p align="center">
  <a href="https://linear.app" target="_blank" rel="noopener noreferrer">
    <img width="64" src="assets/logo.svg" alt="Linear logo">
  </a>
</p>
<h1 align="center">
  Linear for Antigravity
</h1>
<h3 align="center">
  Bring your Linear workspace into Antigravity
</h3>
<p align="center">
  Find issues, manage projects, and keep your work up to date.<br/>
  Connect your code to the work happening in Linear.
</p>

## Overview

The Linear plugin connects Antigravity to your Linear workspace. Find issues,
read project updates, and create or update issues and documents without leaving
your development workflow.

The plugin uses [Linear's hosted MCP server](https://linear.app/docs/mcp).
Sign in with your Linear account to get started. No API key or local server is
required.

## Quick start

### 1. Install from the marketplace

Open **Customizations → Plugins** in Antigravity, find **Linear** in the
marketplace, and click **Install**.

### 2. Connect your Linear account

**Installing the plugin is the first step. Connect your account before using
Linear tools.**

1. Open **Agent settings → Customizations** (`Cmd+,` on macOS).
2. Click **Authenticate** next to the plugin's Linear MCP server.
3. Sign in to Linear in your browser and authorize your workspace.
4. Copy the authorization code shown after approval.
5. Return to Antigravity, paste the code into the authentication field in
   settings, and click **Submit**.

Paste the code into settings, not agent chat. Antigravity reconnects the server
after authentication and refreshes expired access tokens automatically.

### 3. Try it out

Ask Antigravity:

> Show my assigned Linear issues, grouped by priority.

Once Antigravity retrieves your issues from Linear, you're connected. You can
also try:

- Summarize recent updates to my Linear projects.
- Find Linear issues related to the code I am working on.
- Create a Linear issue for the bug we just found.
- Add a progress update to the issue I am working on.

## Troubleshooting

### Installed, but Linear tools are unavailable

Check that the plugin is enabled, then open **Agent settings → Customizations**
and authenticate its Linear MCP server. Installation does not sign you in
automatically.

### Browser sign-in finished, but Antigravity is still waiting

Copy the authorization code from the browser, return to the authentication field
in Antigravity settings, and click **Submit**. This manual handoff is part of
[Antigravity's OAuth flow](https://antigravity.google/docs/mcp#oauth).

### The connection stopped working

Refresh or reconnect the Linear MCP server in Antigravity. Complete authentication
again if prompted. For workspace access and authentication help, see the
[Linear MCP documentation](https://linear.app/docs/mcp).

## Development

For local installation, package details, and release validation, see
[RELEASING.md](RELEASING.md).
