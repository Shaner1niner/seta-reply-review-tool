# SETA Reply Review Tool

A local Python workflow for the u/DataAndFinance Reddit account.

The tool collects a small number of public Reddit posts, prepares candidate reply drafts using internal market/sentiment analytics, and stages those drafts in a local human review dashboard. Replies are only posted after manual review and approval.

The app does not vote, mass-message users, scrape at scale, impersonate users, bypass Reddit rate limits, or post without human approval.

## Workflow

1. Export candidate public posts.
2. Score and filter reply opportunities.
3. Generate draft replies using internal analytics.
4. Review and edit drafts in a local dashboard.
5. Publish only manually approved replies.
6. Store publish metadata for auditability.

## Data Stored

The workflow stores minimal operational data needed for review and auditability:

- Source post URL
- Author handle
- Source post text
- Generated draft text
- Review status
- Final approved reply
- Publish status
- Publish metadata

## Safety Controls

- Human approval is required before posting.
- Replies are staged before publishing.
- Duplicate publish prevention is enforced with database IDs and status tracking.
- Platform-specific limits are checked before dispatch.
- Reddit media/CDN URLs are blocked as non-replyable publish targets.

## Status

This is a local personal-use script workflow for the u/DataAndFinance account.