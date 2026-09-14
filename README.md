# VidGuy MCP

Connect your AI assistant to [VidGuy](https://www.vidguy.ai) to create short-form videos and images, manage brands and content, and schedule or publish to your connected social accounts.

This repository contains public client configuration and installation documentation. The MCP service is hosted by VidGuy.

## Endpoint and authentication

- **Server:** `https://www.vidguy.ai/api/mcp`
- **Transport:** Streamable HTTP. Use the `www.` hostname.
- **Authentication:** OAuth discovery, or a VidGuy API key as an `Authorization: Bearer` header. Never put an actual key in this repository or a public issue.
- **Account:** Starter, Pro, or Enterprise subscriptions support MCP access. VidGuy also offers an Agent plan; generation requires sufficient credits. Installing this client configuration does not include service credits.

Unauthenticated requests return HTTP 401 with an OAuth discovery challenge. Clients discover the authorization server through `https://www.vidguy.ai/.well-known/oauth-protected-resource`. The authorization server advertises dynamic client registration and PKCE.

## Gemini CLI

```sh
gemini extensions install https://github.com/vidguy-ai/mcp
```

Restart Gemini CLI, then use `/mcp auth vidguy` to sign in. The extension uses `httpUrl` for Streamable HTTP and preserves the client's tool confirmation behavior.

## Cursor

The repository contains a Cursor plugin manifest in `.cursor-plugin/plugin.json`. For a manual connection, add the following to your Cursor MCP configuration and complete the OAuth sign-in flow:

```json
{
  "mcpServers": {
    "vidguy": {"url": "https://www.vidguy.ai/api/mcp"}
  }
}
```

## Other MCP clients

Add the endpoint as a remote Streamable HTTP server and follow your client's OAuth flow. If your client supports API-key headers, supply your own key through its secure configuration. For client setup instructions, see [VidGuy MCP](https://www.vidguy.ai/mcp).

## Example requests

- List my brands and summarize the available brand assets.
- Show my current credit balance.
- Create a short vertical product video using the brand and brief I specify.
- Generate three image concepts for this campaign.
- Check the status of my video generation and return its output link.
- Review my scheduled posts before I decide what to publish.

Media generation may spend credits. Social publishing affects real accounts. Review the selected brand, destination, content, and schedule before authorizing these actions.

## Support and policies

For installation questions, [open an issue](https://github.com/vidguy-ai/mcp/issues). Do not include account credentials or private customer content.

[Website](https://www.vidguy.ai) · [Setup](https://www.vidguy.ai/mcp) · [Privacy](https://www.vidguy.ai/privacy) · [Terms](https://www.vidguy.ai/terms)

## License

The client configuration and documentation in this repository are MIT licensed. VidGuy's hosted service is governed by its separate terms. Brand assets remain VidGuy trademarks and are provided to identify this integration.
