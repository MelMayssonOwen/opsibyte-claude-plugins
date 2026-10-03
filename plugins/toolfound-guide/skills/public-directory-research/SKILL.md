---
name: public-directory-research
description: "Research public software listings, compare listed alternatives, inspect recent launches, or review launch timing with Toolfound. Use only for read-only discovery and review; never submit, claim, verify, or modify a listing."
allowed-tools: mcp__plugin_toolfound-guide_toolfound__toolfound_search_tools, mcp__plugin_toolfound-guide_toolfound__toolfound_get_product, mcp__plugin_toolfound-guide_toolfound__toolfound_get_alternatives, mcp__plugin_toolfound-guide_toolfound__toolfound_get_trending, mcp__plugin_toolfound-guide_toolfound__toolfound_list_categories, mcp__plugin_toolfound-guide_toolfound__toolfound_get_launch_calendar
---

# Toolfound public directory research

Use the smallest verified sequence:

1. For a broad need, call `toolfound_list_categories` or `toolfound_search_tools`.
2. Fetch selected records with `toolfound_get_product`; compare only when requested with `toolfound_get_alternatives`.
3. For launch research, use `toolfound_get_trending` and `toolfound_get_launch_calendar`. Treat the calendar as evidence for timing, not a reservation.
4. Report canonical listing URLs and distinguish returned facts from your recommendation. If no match appears, say so and suggest a broader query.

Never call submission, claim, verification, or other mutating tools. Do not imply that a review reserves a date, changes a listing, or guarantees launch results.

The `allowed-tools` list pre-approves these calls for this skill's invocation turn; it does not restrict the available tool pool or enforce read-only access. Follow the read-only instructions above even if the server exposes other tools.
