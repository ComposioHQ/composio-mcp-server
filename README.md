# Composio MCP Server
[![smithery badge](https://smithery.ai/badge/@ComposioHQ/composio-mcp-server)](https://smithery.ai/server/@ComposioHQ/composio-mcp-server)

A Model Context Protocol (MCP) server implementation that exposes Composio tools and actions.

## Overview

This server provides MCP-compatible access to various Composio applications like Gmail, Linear, and more through a standardized interface. It allows language models to interact with these tools in a structured way.

## Prerequisites

- Node.js 16 or higher
- A Composio API key, get it here by signing up at https://app.composio.dev

## Installation

### Installing via Smithery

To install Composio MCP Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@ComposioHQ/composio-mcp-server):

```bash
npx -y @smithery/cli install @ComposioHQ/composio-mcp-server --client claude
```

### Installing Manually
1. Clone the repository:
   ```bash
   git clone https://github.com/composio/composio-mcp-server.git
   cd composio-mcp-server
   ```

2. Install dependencies and build the project:
   ```bash
   pnpm install && pnpm build
   ```

## Configuration

- Create a `.env` file in the root directory of the project.
- Add the following environment variables to the `.env` file:
  ```
  COMPOSIO_API_KEY=<your_composio_api_key>
  COMPOSIO_APPS=gmail,linear
  ```

## Installation guide for composer 

   - Open Cursor Settings
   - Navigate to Features -> Add MCP Server
   - Add the following command:
     ```bash
     node /path/to/composio-mcp-server/start.js
     ```
   - Replace `/path/to/composio-mcp-server` with the actual path where you cloned the repository
   - Ensure your `.env` file is correctly configured with your Composio API Key and desired apps