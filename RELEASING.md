# Developing and releasing the Linear plugin

## Local installation

Use an Antigravity build that supports the partner marketplace manifest format.
Clone into a directory named `linear` to match the plugin identifier:

```sh
git clone https://github.com/linear/antigravity-plugin.git linear
agy plugin validate ./linear
agy plugin install ./linear
agy plugin list
```

After installation, follow the account connection steps in [README.md](README.md).

## Package

- `.antigravity-plugin/plugin.json`: plugin identity and marketplace metadata.
- `mcp_config.json`: the hosted Linear MCP connection using `serverUrl`.
- `assets/logo.svg`: the logo used by
  [linear-release-action](https://github.com/linear/linear/blob/master/docs/logo.svg),
  with transparent padding.

The server implementation and credentials are not part of this package.

## Release validation

This package follows the partner publishing guide's marketplace manifest format.
The [public plugin documentation](https://antigravity.google/docs/plugins) currently
describes a smaller schema, so validate with the intended partner build before
submission. The public schema URL is deliberately omitted from the manifest
because that schema rejects the additional marketplace fields.

Before publishing:

1. Run `agy plugin validate ./linear` and install the package with the intended
   Antigravity build. Confirm the logo, display name, and three starter prompts
   render correctly on light and dark themes.
2. Complete a fresh Linear OAuth sign-in and verify that Linear tools appear.
3. Ask Antigravity to list your assigned issues, then read a known issue and
   verify its identifier, title, and description against Linear.
4. Restart Antigravity and repeat the read. Reconnect and verify sign-in recovery
   if the connection is disconnected or expired.
5. Confirm repository visibility and submission requirements with the Google
   marketplace contact before submitting. Increment the manifest version for
   subsequent published updates.

JSON and asset checks alone do not verify Antigravity installation, OAuth, tool
discovery, or reconnection. Record those results with the tested build before
release.
