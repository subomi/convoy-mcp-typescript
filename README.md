# mcp

Model Context Protocol (MCP) Server for the *mcp* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=mcp&utm_campaign=mcp-typescript"><img src="https://www.speakeasy.com/assets/badges/built-by-speakeasy.svg" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
> [!IMPORTANT]
> This MCP Server is not yet ready for production use. Delete this notice before publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

Convoy API Reference: Convoy is a fast and secure webhooks proxy. This document contains s API specification.
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [mcp](#mcp)
  * [Installation](#installation)
  * [Development](#development)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start Installation [installation] -->
## Installation

<details>
<summary>MCP Bundle (Desktop Extension)</summary>

Install the MCP server as a Desktop Extension using the pre-built [`mcp-server.mcpb`](https://github.com/subomi/convoy-mcp-typescript/releases/download/v0.4.0/mcp-server.mcpb) file:

Simply drag and drop the [`mcp-server.mcpb`](https://github.com/subomi/convoy-mcp-typescript/releases/download/v0.4.0/mcp-server.mcpb) file onto Claude Desktop to install the extension.

The MCP bundle package includes the MCP server and all necessary configuration. Once installed, the server will be available without additional setup.

> [!NOTE]
> MCP bundles provide a streamlined way to package and distribute MCP servers. Learn more about [Desktop Extensions](https://www.anthropic.com/engineering/desktop-extensions).

</details>

<details>
<summary>Cursor</summary>

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](cursor://anysphere.cursor-deeplink/mcp/install?name=Convoy&config=eyJtY3BTZXJ2ZXJzIjp7IkNvbnZveSI6eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyJtY3AiLCJzdGFydCIsIi0tYmVhcmVyLWF1dGgiLCIuLi4iXX19fQ==)

Or manually:

1. Open Cursor Settings
2. Select Tools and Integrations
3. Select New MCP Server
4. If the configuration file is empty paste the following JSON into the MCP Server Configuration:

```json
{
  "mcpServers": {
    "Convoy": {
      "command": "npx",
      "args": [
        "mcp",
        "start",
        "--bearer-auth",
        "..."
      ]
    }
  }
}
```

</details>

<details>
<summary>Claude Code CLI</summary>

```bash
claude mcp add mcp npx mcp start -- --bearer-auth ...
```

</details>
<details>
<summary>Windsurf</summary>

Refer to [Official Windsurf documentation](https://docs.windsurf.com/windsurf/cascade/mcp#adding-a-new-mcp-plugin) for latest information

1. Open Windsurf Settings
2. Select Cascade on left side menu
3. Click on `Manage MCPs`. (To Manage MCPs you should be signed in with a Windsurf Account)
4. Click on `View raw config` to open up the mcp configuration file.
5. If the configuration file is empty paste the full json
```
{
  "mcpServers": {
    "Convoy": {
      "command": "npx",
      "args": [
        "mcp",
        "start",
        "--bearer-auth",
        "..."
      ]
    }
  }
}
```
</details>
<details>
<summary>VS Code</summary>

Refer to [Official VS Code documentation](https://code.visualstudio.com/api/extension-guides/ai/mcp) for latest information

1. Open [Command Palette](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)
1. Search and open `MCP: Open User Configuration`. This should open mcp.json file
2. If the configuration file is empty paste the full json
```
{
  "mcpServers": {
    "Convoy": {
      "command": "npx",
      "args": [
        "mcp",
        "start",
        "--bearer-auth",
        "..."
      ]
    }
  }
}
```

</details>
<details>
<summary>Claude Desktop</summary>
Claude Desktop doesn't yet support SSE/remote MCP servers.

You need to do the following
1. Open claude Desktop
2. Open left hand side pane, then click on your Username
3. Go to `Settings`
4. Go to `Developer` tab (on the left hand side)
5. Click on `Edit Config`
Paste the following config in the configuration

```json
{
  "mcpServers": {
    "Convoy": {
      "command": "npx",
      "args": [
        "mcp",
        "start",
        "--bearer-auth",
        "..."
      ]
    }
  }
}
```

</details>


<details>
<summary> Stdio installation via npm </summary>
To start the MCP server, run:

```bash
npx mcp start --bearer-auth ...
```

For a full list of server arguments, run:

```
npx mcp --help
```

</details>
<!-- End Installation [installation] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

## Development

Run locally without a published npm package:
1. Clone this repository
2. Run `npm install`
3. Run `npm run build`
4. Run `node ./bin/mcp-server.js start --bearer-auth ...`
To use this local version with Cursor, Claude or other MCP Clients, you'll need to add the following config:

```json
{
  "mcpServers": {
    "SDK": {
      "command": "node",
      "args": [
        "./bin/mcp-server.js",
        "start",
        "--bearer-auth",
        "..."
      ]
    }
  }
}
```

Or to debug the MCP server locally, use the official MCP Inspector: 

```bash
npx @modelcontextprotocol/inspector node ./bin/mcp-server.js start --bearer-auth ...
```



## Contributions

While we value contributions to this MCP Server, the code is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### MCP Server Created by [Speakeasy](https://www.speakeasy.com/?utm_source=mcp&utm_campaign=mcp-typescript)
