# Model Context Protocol (MCP) Server + Delegated Clerk OAuth

WIP

Instead of using Clerk as a third party and still hosting auth + sessions inside the MCP / MCP auth service, we delegate auth completely to Clerk and utilize it as our OAuth provider.

Supports dynamic client registration on Clerk by only supporting the registration endpoint on our separate auth service hosted on the same worker. I say separate because I think it is confusing to say the MCP server itself manages the auth, but I would say it is separate.

Code does not work without making changes to both the MCP TypeScript SDK and `mcp-remote` from Cloudflare.