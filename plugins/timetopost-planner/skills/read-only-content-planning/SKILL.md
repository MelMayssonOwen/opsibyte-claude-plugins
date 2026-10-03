---
name: read-only-content-planning
description: "Analyze existing TimeToPost content, timing, integrations, engagement, drafts, approvals, and public timing to create a content plan without drafting, scheduling, publishing, sending, uploading, approving, or changing accounts. Use only after verifying the customer-explicitly intended workspace."
allowed-tools: mcp__plugin_timetopost-planner_timetopost__whoami, mcp__plugin_timetopost-planner_timetopost__list_integrations, mcp__plugin_timetopost-planner_timetopost__list_posts, mcp__plugin_timetopost-planner_timetopost__get_post, mcp__plugin_timetopost-planner_timetopost__get_engagement_summary, mcp__plugin_timetopost-planner_timetopost__get_optimal_times, mcp__plugin_timetopost-planner_timetopost__list_drafts, mcp__plugin_timetopost-planner_timetopost__list_approvals, mcp__plugin_timetopost-planner_timetopost__best_time_teaser
---

# Read-only TimeToPost content planning

1. Ask which workspace the customer explicitly intends to use, then call `whoami` first. Continue only when the returned workspace clearly matches that stated intent. A legitimately authorized agency workspace is allowed when the customer explicitly selected it. If the result differs or is ambiguous, stop and ask the customer to switch or clarify; do not inspect any content first.
2. Read only what the task needs: existing posts, timing, integrations, engagement, drafts, approvals, or public timing.
3. Produce the plan in chat. Label observed data, interpretation, and proposed copy separately. A proposed idea is not a TimeToPost draft.
4. Never call tools that create drafts, upload media, connect or regroup accounts, schedule, publish, approve, reject, cancel, send, configure, or otherwise mutate state—even if the server exposes them.

The dedicated planning endpoint enforces this read-only scope. The `allowed-tools` list pre-approves the nine available calls for this skill's invocation turn: identity, integrations, posts, an individual post, engagement, optimal times, drafts, approvals, and the public teaser. Ask for no production credentials and do not claim platform publication or approval status.
