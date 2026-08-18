# Scavio for OpenClaw

Structured web data for OpenClaw agents. One API key, 31 platforms, clean JSON
instead of HTML you have to parse.

This plugin bundles all 39 Scavio skills in a single install. If you only want
one platform, the skills are also published individually - see below.

## Install

```bash
openclaw plugins install @scavio-ai/scavio-clawhub
```

Get an API key at [scavio.dev](https://scavio.dev), then set it in the plugin
config:

```json
{
  "plugins": {
    "entries": {
      "scavio": {
        "apiKey": "sk_your_key_here",
        "platforms": "default"
      }
    }
  }
}
```

`platforms` picks the tool surface. Unset or `default` registers 106 tools
across 11 platforms. It is additive - `default,zillow,sec` adds to the default
set. `all` registers 191 tools, which is a large payload in every session.

## What you get

| Domain | Platforms |
|:-------|:----------|
| Search | Google SERP, AI Mode, News, Trends, Maps |
| Commerce | Amazon, Walmart, eBay, Target, Home Depot, Google Shopping, TikTok Shop |
| Social | YouTube, TikTok, Instagram, Threads, X, Reddit, Kuaishou |
| Travel and local | Booking.com, Airbnb, Tripadvisor, Yelp, Google Flights, Google Hotels |
| Property | Zillow, Redfin |
| Jobs and employers | LinkedIn, Indeed, Glassdoor |
| Software reviews | G2, Capterra |
| App stores | Apple App Store, Google Play |
| Ad libraries | Google Ads Transparency, Meta Ads |
| Company filings | SEC EDGAR, UK Companies House |
| Any URL | Extract - markdown, text or HTML |

## Individual skills

Every platform is also a standalone skill if you would rather not install all 39:

```bash
openclaw skills install @scavio-ai/scavio-amazon
openclaw skills install @scavio-ai/scavio-reddit
```

Full list at [clawhub.ai/scavio-ai](https://clawhub.ai/scavio-ai).

## Related

Scavio also ships a [Cursor plugin](https://github.com/scavio-ai/scavio-cursor)
and a [Claude Code plugin](https://github.com/scavio-ai/scavio-plugins). The
skill content is shared; setup guidance differs per host, so each is packaged
separately.

## License

MIT
