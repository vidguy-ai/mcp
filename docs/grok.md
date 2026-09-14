# Connect VidGuy to Grok

This guide follows [Grok's custom MCP documentation](https://docs.x.ai/grok/connectors). VidGuy's end-to-end Grok OAuth flow has not yet been verified. A custom connection is separate from a catalog listing.

1. Open [Grok Connectors](https://grok.com/connectors).
2. Choose **New Connector**, then **Custom**.
3. Enter `https://www.vidguy.ai/api/mcp` and complete the requested authentication.
4. Start with “List my VidGuy brands” and “Show my current credit balance.”

Business or Enterprise workspaces may need an administrator to provision the connector. If authorization fails, retain the error message without tokens or credentials and [open an installation issue](https://github.com/vidguy-ai/mcp/issues).

After confirming read-only access, give Grok a specific creative brief, brand and budget. Generation can consume credits. Review the actual asset, destination account and schedule before publishing to social media. Each user must connect their own VidGuy account.

## First workflow

> List my brands and existing videos. Help me select one brand and one finished video for a product post. Draft a caption and propose a schedule. Show me the exact destination and content, and wait for my approval before scheduling it.

This workflow does not require generating new media. If you want a new video, provide an explicit brief and approve its cost first.

[VidGuy setup](https://www.vidguy.ai/mcp) · [Privacy](https://www.vidguy.ai/privacy)
