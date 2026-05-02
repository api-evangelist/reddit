# Reddit

Reddit is a social news aggregation, discussion, and community platform where users submit, vote, and comment on content organized into topic-based communities called subreddits. Reddit provides developer APIs for accessing platform data, managing communities, running advertising campaigns, and embedding content. All API access requires OAuth 2.0 authentication via the oauth.reddit.com server at 60 requests per minute.

**URL:** [https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/apis.yml)

## Tags

Advertising, Communities, Content, Social Media, Social News

## APIs

### [Reddit Data API](openapi/reddit-data-api-openapi.yml)
The Reddit Data API provides programmatic access to Reddit content including subreddits, posts, comments, user profiles, and voting data. Developers can use the API to read and submit content, manage subreddits, search across the platform, interact with Reddit communities, handle private messages, and manage flair.

**Base URL:** `https://oauth.reddit.com`

- [Documentation](https://www.reddit.com/dev/api)
- [Authentication](https://github.com/reddit-archive/reddit/wiki/OAuth2)
- [Terms of Service](https://www.redditinc.com/policies/data-api-terms)
- [OpenAPI](openapi/reddit-data-api-openapi.yml)

### [Reddit Ads API](openapi/reddit-ads-api-openapi.yml)
The Reddit Ads API allows advertisers and their marketing partners to programmatically create, edit, manage, and report on advertising campaigns on Reddit. It provides endpoints for managing ad accounts, campaigns, ad groups, ads, creatives, targeting configurations, custom audiences, conversion pixels, and performance reporting.

**Base URL:** `https://ads-api.reddit.com/api/v3`

- [Documentation](https://ads-api.reddit.com/docs/)
- [Terms of Service](https://business.reddithelp.com/s/article/Reddit-Ads-API-Terms)
- [OpenAPI](openapi/reddit-ads-api-openapi.yml)

### [Reddit Embeds (oEmbed)](openapi/reddit-embeds-openapi.yml)
Reddit Embeds allows developers and content creators to embed Reddit posts and comments directly into external websites and applications. The service provides oEmbed endpoints that return embed codes and metadata for rendering Reddit content in a visually consistent format outside of the Reddit platform.

**Base URL:** `https://www.reddit.com`

- [Documentation](https://support.reddithelp.com/hc/en-us/articles/14945211791892-Developer-Platform-Accessing-Reddit-Data)
- [OpenAPI](openapi/reddit-embeds-openapi.yml)

### Reddit OAuth 2.0 Authorization
Reddit's OAuth 2.0 authorization system provides authentication for all Reddit API access. Developers register applications at reddit.com/prefs/apps to obtain client credentials. Supported grant types include authorization_code, client_credentials, and implicit.

**Base URL:** `https://www.reddit.com/api/v1`

- [Documentation](https://github.com/reddit-archive/reddit/wiki/OAuth2)
- [Scopes](https://www.reddit.com/api/v1/scopes)
- [App Registration](https://www.reddit.com/prefs/apps)

## Capabilities

### Workflow Capabilities

| Capability | Description |
|-----------|-------------|
| [Community Engagement](capabilities/community-engagement.yaml) | Content discovery and community interaction including subreddit browsing and post submission (6 MCP tools) |
| [Advertising](capabilities/advertising.yaml) | Programmatic ad campaign creation and management with audience targeting (6 MCP tools) |

### Shared Definitions

| File | API |
|------|-----|
| [data-api.yaml](capabilities/shared/data-api.yaml) | Reddit Data API |
| [ads-api.yaml](capabilities/shared/ads-api.yaml) | Reddit Ads API |

## Artifacts

| Type | File |
|------|------|
| OpenAPI | [Data API](openapi/reddit-data-api-openapi.yml) |
| OpenAPI | [Ads API](openapi/reddit-ads-api-openapi.yml) |
| OpenAPI | [Embeds API](openapi/reddit-embeds-openapi.yml) |
| JSON Schema | [Post](json-schema/reddit-post-schema.json) |
| JSON Schema | [Comment](json-schema/reddit-comment-schema.json) |
| JSON Schema | [Subreddit](json-schema/reddit-subreddit-schema.json) |
| JSON Structure | [Post Structure](json-structure/reddit-post-structure.json) |
| JSON-LD Context | [Reddit Context](json-ld/reddit-context.jsonld) |
| Spectral Rules | [Reddit Rules](rules/reddit-rules.yml) |
| Vocabulary | [Reddit Vocabulary](vocabulary/reddit-vocabulary.yml) |

## Examples

- [Get Subreddit Hot Posts](examples/reddit-get-subreddit-hot-example.json)
- [Create Campaign](examples/reddit-create-campaign-example.json)

## Common Properties

- [Website](https://www.reddit.com)
- [Developer Portal](https://www.reddit.com/dev/api)
- [Documentation](https://support.reddithelp.com/hc/en-us/articles/16160319875092-Reddit-Data-API-Wiki)
- [GitHub Organization](https://github.com/reddit-archive)
- [Blog](https://www.redditinc.com/blog)
- [Privacy Policy](https://www.reddit.com/policies/privacy-policy)
- [Terms of Service](https://www.redditinc.com/policies/user-agreement)
- [Status](https://www.redditstatus.com/)
- [Support](https://support.reddithelp.com/hc/en-us)
- [Sign Up](https://www.reddit.com/register)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
