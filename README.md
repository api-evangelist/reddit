# Reddit (reddit)

Reddit is a social news aggregation, discussion, and community platform where users submit, vote, and comment on content organized into topic-based communities called subreddits. Reddit provides developer APIs for accessing platform data, managing communities, running advertising campaigns, and embedding content. The Reddit Data API provides access to posts, comments, subreddits, user profiles, and moderation tools via OAuth 2.0. The Reddit Ads API enables programmatic management of advertising campaigns, audiences, and conversion tracking. All API access requires OAuth 2.0 authentication via the oauth.reddit.com server at 60 requests per minute.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/reddit/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Advertising
- Communities
- Content
- Social Media
- Social News

## Timestamps

- **Created:** 2026-01-01
- **Modified:** 2026-05-19

## APIs

### Reddit Data API

The Reddit Data API provides programmatic access to Reddit content including subreddits, posts, comments, user profiles, and voting data. Developers can use the API to read and submit content, manage subreddits, search across the platform, interact with Reddit communities, handle private messages, and manage flair. All requests require OAuth 2.0 authentication via oauth.reddit.com with rate limits of 60 requests per minute for authenticated clients. A Data API Terms agreement is required for high-volume access.

- **Human URL:** [https://www.reddit.com/dev/api](https://www.reddit.com/dev/api)
- **Base URL:** `https://oauth.reddit.com`

#### Tags

- Comments
- Communities
- Content
- Posts
- Social Media
- Subreddits

#### Properties

- [Documentation](https://www.reddit.com/dev/api)
- [Authentication](https://github.com/reddit-archive/reddit/wiki/OAuth2)
- [Terms of Service](https://www.redditinc.com/policies/data-api-terms)
- [OpenAPI](openapi/reddit-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reddit-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Reddit Ads API

The Reddit Ads API allows advertisers and their marketing partners to programmatically create, edit, manage, and report on advertising campaigns on the Reddit platform. It provides endpoints for managing ad accounts, campaigns, ad groups, ads, creatives, targeting configurations, custom audiences (email lists, mobile IDs, pixel-based), conversion pixels, and performance reporting. Authentication uses OAuth 2.0 with a rate limit of one request per second per advertiser account.

- **Human URL:** [https://ads-api.reddit.com/docs/](https://ads-api.reddit.com/docs/)
- **Base URL:** `https://ads-api.reddit.com/api/v3`

#### Tags

- Advertising
- Campaigns
- Marketing
- Social Media
- Targeting

#### Properties

- [Documentation](https://ads-api.reddit.com/docs/)
- [Terms of Service](https://business.reddithelp.com/s/article/Reddit-Ads-API-Terms)
- [OpenAPI](openapi/reddit-ads-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reddit-ads-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-ads-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Reddit Embeds (oEmbed)

Reddit Embeds allows developers and content creators to embed Reddit posts and comments directly into external websites and applications. The service provides oEmbed endpoints that return embed codes and metadata for rendering Reddit content in a visually consistent format outside of the Reddit platform. It follows the oEmbed specification for content discovery and embedding, returning HTML embed code for any Reddit post or comment URL.

- **Human URL:** [https://oembed.com/](https://oembed.com/)
- **Base URL:** `https://www.reddit.com`

#### Tags

- Content
- Embedding
- oEmbed
- Social Media

#### Properties

- [Documentation](https://support.reddithelp.com/hc/en-us/articles/14945211791892-Developer-Platform-Accessing-Reddit-Data)
- [OpenAPI](openapi/reddit-embeds-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reddit-embeds.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-embeds.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Reddit OAuth 2.0 Authorization

Reddit's OAuth 2.0 authorization system provides authentication for all Reddit API access. Developers register applications at reddit.com/prefs/apps to obtain client credentials. Supported grant types include authorization_code (for user-delegated access), client_credentials (for app-only access), and implicit (for installed apps). Access tokens are obtained from https://www.reddit.com/api/v1/access_token and must be refreshed using refresh tokens. All scopes and permissions are listed at https://www.reddit.com/api/v1/scopes.

- **Human URL:** [https://github.com/reddit-archive/reddit/wiki/OAuth2](https://github.com/reddit-archive/reddit/wiki/OAuth2)
- **Base URL:** `https://www.reddit.com/api/v1`

#### Tags

- Authentication
- Authorization
- OAuth 2.0
- Security

#### Properties

- [Documentation](https://github.com/reddit-archive/reddit/wiki/OAuth2)
- [Scopes](https://www.reddit.com/api/v1/scopes)
- [App  Registration](https://www.reddit.com/prefs/apps)
- [Postman Collection](collections/reddit-ads-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-ads-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/reddit-data-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-data-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/reddit-embeds.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reddit-embeds.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/reddit-com)
- [Website](https://www.reddit.com)
- [Developer  Portal](https://www.reddit.com/dev/api)
- [Documentation](https://support.reddithelp.com/hc/en-us/articles/16160319875092-Reddit-Data-API-Wiki)
- [GitHub Organization](https://github.com/reddit-archive)
- [Blog](https://www.redditinc.com/blog)
- [Privacy Policy](https://www.reddit.com/policies/privacy-policy)
- [Terms of Service](https://www.redditinc.com/policies/user-agreement)
- [Status Page](https://www.redditstatus.com/)
- [Support](https://support.reddithelp.com/hc/en-us)
- [Sign Up](https://www.reddit.com/register)
- [OpenAPI](openapi/reddit-data-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/reddit-ads-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/reddit-embeds-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/reddit-post-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reddit-comment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/reddit-subreddit-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N L D Context](json-ld/reddit-context.jsonld)
- [JSON Structure](json-structure/reddit-post-structure.json)
- [Spectral Ruleset](rules/reddit-rules.yml)
- [Vocabulary](vocabulary/reddit-vocabulary.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
