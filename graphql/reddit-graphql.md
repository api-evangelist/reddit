# Reddit GraphQL Schema

## Overview

This conceptual GraphQL schema represents the Reddit platform's data model, derived from the official Reddit Data API (https://www.reddit.com/dev/api/) and Reddit's OAuth 2.0 authentication system. Reddit is a social news aggregation, discussion, and community platform organized into topic-based communities called subreddits. The schema covers posts, comments, subreddits, users, moderation, messaging, search, and authentication objects.

## Source

- **Provider**: Reddit
- **API Reference**: https://www.reddit.com/dev/api/
- **Authentication**: OAuth 2.0 via oauth.reddit.com
- **Base URL**: https://oauth.reddit.com
- **Schema File**: reddit-schema.graphql

## Schema Design

The schema is organized around Reddit's core domain objects:

### Community & Content

- **Subreddit** — A topic-based community (e.g., r/programming). Contains metadata, rules, flair settings, wiki pages, and moderator lists.
- **SubredditDetails** — Extended subreddit metadata including subscriber counts, active users, creation date, and NSFW/quarantine flags.
- **SubredditRules** — The rules a subreddit enforces, including rule text, short names, and violation reasons.
- **SubredditFlair** — Flair templates available for posts and users within a subreddit.
- **SubredditStyle** — Custom CSS and banner/icon images applied to a subreddit.
- **SubredditWiki** — The wiki associated with a subreddit, listing pages and revision history.
- **WikiPage** — A single wiki page within a subreddit, including content and revision metadata.
- **WikiRevision** — A historical revision of a wiki page, capturing author and timestamp.
- **Multireddit** — A curated collection of subreddits grouped by a user into a named feed.
- **MultiredditSub** — A single subreddit entry within a Multireddit.

### Posts

- **Post** — The base type for all Reddit submissions, carrying common fields like title, score, author, subreddit, and timestamps.
- **LinkPost** — A submission that links to an external URL.
- **TextPost** — A self-post submission containing body text (selftext).
- **GalleryPost** — A multi-image gallery submission.
- **VideoPost** — A video submission, including hosted video metadata.
- **CrossPost** — A reposted submission referencing an original post from another subreddit.
- **PostDetails** — Extended post metadata including crosspost count, media embeds, and preview images.
- **PostFlair** — Flair applied to a post, including text, CSS class, and background color.
- **SavedPost** — A post that has been saved to a user's account.

### Comments

- **Comment** — A reply to a post or another comment, including body text, score, and threading depth.
- **CommentTree** — A hierarchical tree of comments attached to a post.
- **MoreComments** — A placeholder node in a comment tree indicating additional comments to load.
- **CommentCollapse** — Collapse state metadata for a comment thread.
- **Reply** — A direct reply comment in a thread.

### Voting & Awards

- **Vote** — A generic vote action on a post or comment.
- **Upvote** — A positive vote cast by a user.
- **Downvote** — A negative vote cast by a user.
- **Reaction** — An emoji-based reaction to a post or comment (Reddit newer feature).
- **Award** — An award given to a post or comment (e.g., Gold, Silver, Platinum).
- **Trophy** — A user-level trophy awarded for achievements on Reddit.

### Users

- **User** — Base user identity including username and account ID.
- **RedditUser** — Full Reddit user account including karma, creation date, premium status, and profile details.
- **UserProfile** — Public profile fields for a Reddit user, including bio, banner, and icon images.
- **Karma** — Breakdown of a user's link karma and comment karma.
- **UserFlair** — Flair assigned to a user within a specific subreddit.
- **RedditPremium** — Reddit Premium (formerly Reddit Gold) subscription status and coin balance.
- **UserTrophy** — Association between a user and a trophy they have earned.
- **UserFeed** — The personalized content feed for a user (home feed, popular, all).

### Moderation

- **Moderator** — A user who moderates a subreddit, including their permission set and mod date.
- **ModeratorAction** — A single moderation action taken within a subreddit.
- **ModLog** — The moderation log for a subreddit, listing all recent moderator actions.
- **Ban** — A ban record preventing a user from participating in a subreddit.
- **ModBan** — Extended ban information including ban message and permanent/temporary duration.
- **MutedUser** — A user muted in a subreddit (cannot send mod mail).
- **Report** — A user-submitted report on a post or comment.
- **ReportReason** — A predefined reason category for reporting content.
- **SpamFilter** — Spam filtering configuration for a subreddit.
- **ContentPolicy** — Reddit-wide content policy reference object.

### Messaging & Notifications

- **Message** — A private message sent between Reddit users.
- **ComposedMessage** — A new message being composed, including subject and body fields.
- **Inbox** — A user's message inbox, including sent, received, and mention threads.
- **Notification** — A notification event for a user (mention, reply, mod action, etc.).

### Search

- **Search** — A search query executed against Reddit content.
- **SearchResult** — A single result returned by a Reddit search, which may be a Post, Comment, or Subreddit.

### Authentication & Authorization

- **OAuthApp** — A registered Reddit OAuth application, including client ID, type, and redirect URI.
- **AccessToken** — A short-lived OAuth 2.0 access token granting API access.
- **RefreshToken** — A long-lived token used to obtain new access tokens.
- **Scope** — An OAuth 2.0 scope defining a specific permission granted to an application.
- **APIKey** — An API key or client credential pair for server-side authentication.
- **RateLimit** — Rate limit metadata returned in API response headers (60 req/min authenticated).
- **Webhook** — A webhook endpoint registration for receiving Reddit event notifications.

## Queries

The schema exposes queries for fetching:

- Individual subreddits, posts, comments, and users by ID or name
- Subreddit listings (hot, new, rising, top, controversial)
- User submissions, comments, saved content, and upvoted content
- Moderation logs, banned users, and moderator lists
- Search results across posts, comments, and subreddits
- User inbox, messages, and notifications
- Multireddits and their component subreddits

## Mutations

The schema exposes mutations for:

- Submitting new posts (link, text, gallery)
- Posting and editing comments
- Voting on posts and comments
- Saving and unsaving content
- Sending private messages
- Subscribing and unsubscribing from subreddits
- Moderator actions (approve, remove, ban, mute)
- Awarding posts and comments
- Managing OAuth applications

## Authentication

All queries and mutations require OAuth 2.0 authentication. The `AccessToken` obtained from `https://www.reddit.com/api/v1/access_token` must be passed as a Bearer token. Scopes control what data and actions are accessible to a given application or user session.
