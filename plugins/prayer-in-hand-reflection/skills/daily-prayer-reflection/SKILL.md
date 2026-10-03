---
name: daily-prayer-reflection
description: "Find public Prayer in Hand prayer guides and create a static morning, midday, and evening reflection rhythm. Use for a gentle daily spiritual practice using the read-only Prayer in Hand integration."
---

# Daily prayer reflection

Use the public, read-only `prayer-in-hand` integration. It cannot access local app data. Keep Prayer in Hand, Claude, and this plugin distinct; never imply that one brand operates, endorses, or has access to another beyond the public integration.

## Tools

- Call `search_prayer_guides` to discover public guides. `query` is optional and has a maximum length of 100 characters; `limit` must be from 1 through 20.
- Call `get_prayer_guide` with a `slug` returned by `search_prayer_guides`. Do not guess slugs.
- Call `build_reflection_rhythm` to create a static rhythm of exactly three pauses. `minutesPerPause` must be from 1 through 15 and defaults to 5; the total duration is three times that value.

## Resources

- `prayer://guides` lists public guides.
- `prayer://daily-reflection` provides the static daily reflection resource.
- `prayer://guides/{slug}` identifies a public guide using a slug returned by search.

## Safety and attribution

Never put private writing, prayer-journal text, names, health information, or other sensitive details into `query`. Use only a short, non-sensitive topic or omit the query. The integration has no access to the user's local Prayer in Hand app data.

Cite the `sourceUrl` or canonical `url` returned by the tool or resource whenever presenting guide content. Never invent citations, URLs, guide text, or product capabilities. If no URL is returned, say that no source link was provided.

Use the user's faith language when provided; otherwise keep wording simple and broadly Christian. Present guides and rhythms as optional reflection aids, not spiritual authority. Do not claim divine certainty, diagnose, replace professional care, or make medical, mental-health, or wellbeing claims.
