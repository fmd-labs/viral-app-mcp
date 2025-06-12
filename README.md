# viral.app MCP Server - TikTok Analytics for AI

Connect your AI tools to live TikTok analytics with viral.app's Model Context Protocol (MCP) server. Get real-time TikTok data directly in Cursor, Claude Desktop, Raycast, and more.

**🚀 Get started at [viral.app/mcp](https://viral.app/mcp)**

## What is viral.app MCP?

viral.app MCP is a powerful bridge between your AI assistant and TikTok's analytics data. Using the Model Context Protocol standard, it enables your AI to:

- Look up TikTok user profiles and statistics
- Analyze video performance metrics
- Retrieve video transcripts
- List recent videos from any profile

No more manual data gathering—just ask your AI and get instant TikTok insights.

## Quick Setup

### 1. Create Your Free Account

Sign up at [viral.app/auth/sign-up]([https://viral.app/mcp](https://viral.app/auth/sign-up)) to get started. No credit card required, and you don't need a paid subscription to use the MCP server.

### 2. Configure Your AI Client

Add the viral.app MCP server to your preferred AI tool:

#### Cursor

```json
{
  "mcpServers": {
    "viral.app": {
      "command": "npx",
      "args": ["-y", "mcp-remote@latest", "https://viral.app/api/mcp"]
    }
  }
}
```

#### Raycast

- Name: `viral.app`
- Command: `npx`
- Arguments: `-y mcp-remote@latest https://viral.app/api/mcp`

#### Claude Desktop, Windsurf, Cline

Use the same JSON configuration as Cursor in your MCP settings.

### 3. Authenticate

After adding the server, you'll be prompted to authenticate via OAuth. Complete the authentication, and you're ready to analyze TikTok data!

## Available Tools

### 🔍 Get TikTok Profile (`get-tiktok-profile`)

Retrieve comprehensive profile data including follower counts, engagement stats, and profile metadata.

**Example Usage:**

```
"How many followers does MrBeast have on TikTok?"
"Get the profile stats for @charlidamelio"
```

**Returns:**

- Profile information (nickname, bio link, verification status)
- Statistics (followers, following, videos, hearts given/received)

### 📹 Get Video Details (`get-tiktok-video`)

Analyze any TikTok video URL to get comprehensive stats, author details, and optional transcripts.

**Example Usage:**

```
"Analyze this TikTok video: https://www.tiktok.com/@user/video/123456"
"Get the transcript for this TikTok video: [url]"
```

**Returns:**

- Video metadata (description, duration, creation time)
- Performance metrics (views, likes, shares, comments)
- Author information
- Transcript (optional, costs 2 credits)

### 📊 List Profile Videos (`list-profile-videos`)

Retrieve up to 30 recent videos from any TikTok profile with detailed performance metrics.

**Example Usage:**

```
"Show me the last 10 videos from @nike"
"List the recent posts from @natgeo with their stats"
```

**Returns:**

- List of videos with metadata
- Performance statistics for each video
- Video URLs and dimensions

## Daily Credit System

Start analyzing TikTok data immediately with our free tier:

| Plan           | Daily Tool Calls | Best For                     |
| -------------- | ---------------- | ---------------------------- |
| **Free**       | 5                | Testing & personal use       |
| **Pro**        | 50               | Content creators & marketers |
| **Ultra**      | 500              | Agencies & power users       |
| **Enterprise** | Unlimited        | Large teams & automation     |

Learn more about pricing at [https://viral.app/mcp](https://viral.app/mcp)

## Coming Soon 🎉

We're expanding beyond TikTok! Get ready for:

- **Instagram MCP Server** - Track follower growth, post engagement, story insights, and competitor performance
- **YouTube MCP Server** - Analyze channel statistics, video metrics, audience demographics, and content trends
- **Personal viral.app MCP** - Access your own viral.app analytics data through AI

Your credits will work across all our MCP servers—one subscription, multiple platforms!

## Troubleshooting

### Authentication Issues

If you can't authenticate, try clearing the mcp-remote cache:

```bash
rm -rf ~/.mcp-auth
```

### Missing Node.js

The MCP server requires Node.js. Install it via:

- macOS: `brew install node` or [nodejs.org](https://nodejs.org)
- Windows: Follow [this guide](https://www.pulsemcp.com/posts/how-to-get-started-using-mcp)

## Support & Resources

- 📚 Full documentation: [https://viral.app/mcp](https://viral.app/mcp)
- 💬 Need help? Contact support through your viral.app dashboard
- 🐛 Found a bug? Let us know via [hello@viral.app](mailto:hello@viral.app) or on [Twitter](https://x.com/mikey_starts).

---

Built with ❤️ by [viral.app](https://viral.app) - Your AI-powered social media analytics platform.
