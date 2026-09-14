# Telegram MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/telegram)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Telegram to AI assistants: send and manage messages through your Telegram bot.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — use Telegram from Claude, ChatGPT, Cursor, and other AI assistants through the Model Context Protocol (MCP).

<img src="images/telegram-icon.svg" alt="Telegram MCP Server" width="64" height="64">

## MCP Server URL

```
https://telegram.insightfulmcp.com/
```

## What is Telegram MCP?

Telegram MCP is a **remote Model Context Protocol server** hosted by InsightfulPipe. Access messages, chats, channels, groups, and media data from your Telegram bot via the Bot API.

## Installation

### Claude

1. Copy the MCP Server URL: `https://telegram.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://telegram.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http telegram https://telegram.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "telegram": {
      "url": "https://telegram.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

24 actions: 9 read, 15 write.

### Read Actions (9)

| Action | Description |
|--------|-------------|
| `get_chat` | Get detailed information about a chat (group, supergroup, channel, or private chat) |
| `get_chat_member` | Get information about a specific member of a chat |
| `get_file` | Get basic info about a file and prepare it for downloading |
| `get_me` | Get basic information about the bot (id, name, username, capabilities) |
| `get_my_commands` | Get the list of the bot's default commands for a language |
| `get_my_description` | Get the bot's description for the given language |
| `get_my_name` | Get the bot's name for the given language |
| `get_my_short_description` | Get the bot's short description for the given language |
| `get_user_profile_photos` | Get a user's profile photos |

### Write Actions (15)

| Action | Description |
|--------|-------------|
| `copy_message` | Copy a message (sends a new message without 'Forwarded from' tag) |
| `delete_message` | Delete a message |
| `edit_message_caption` | Edit the caption of a message sent by the bot |
| `edit_message_text` | Edit the text of a message sent by the bot |
| `forward_message` | Forward a message from one chat to another |
| `pin_chat_message` | Pin a message in a chat |
| `send_audio` | Send an audio file to a chat |
| `send_contact` | Send a phone contact to a chat |
| `send_location` | Send a geographic location to a chat |
| `send_message` | Send a text message to a chat |
| `send_photo` | Send a photo to a chat |
| `send_poll` | Send a poll to a chat |
| `send_video` | Send a video to a chat |
| `unpin_all_chat_messages` | Unpin all pinned messages in a chat |
| `unpin_chat_message` | Unpin a message in a chat |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

```
"Send this week's update to our announcements channel"
```

```
"Show details about this chat"
```

```
"Pin the latest message in the channel"
```

## Pricing

The Telegram MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month with a 7-day free trial. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers.

- [Slack MCP](https://insightfulpipe.com/mcp-servers/slack)
- [Notion MCP](https://insightfulpipe.com/mcp-servers/notion)

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
