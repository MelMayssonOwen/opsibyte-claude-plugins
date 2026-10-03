---
name: read-only-content-planning
description: "Analyze existing TimeToPost content, prompts, timing, and engagement to create a content plan without drafting, scheduling, publishing, sending, uploading, approving, or changing accounts. Use only after verifying the customer-explicitly intended workspace."
allowed-tools: mcp__plugin_timetopost-planner_timetopost__whoami, mcp__plugin_timetopost-planner_timetopost__get_capabilities, mcp__plugin_timetopost-planner_timetopost__prompt_suggest, mcp__plugin_timetopost-planner_timetopost__prompt_library_list, mcp__plugin_timetopost-planner_timetopost__list_integrations, mcp__plugin_timetopost-planner_timetopost__list_posts, mcp__plugin_timetopost-planner_timetopost__get_post, mcp__plugin_timetopost-planner_timetopost__get_engagement_summary, mcp__plugin_timetopost-planner_timetopost__get_optimal_times, mcp__plugin_timetopost-planner_timetopost__scheduler_status, mcp__plugin_timetopost-planner_timetopost__list_drafts, mcp__plugin_timetopost-planner_timetopost__list_approvals, mcp__plugin_timetopost-planner_timetopost__list_brands, mcp__plugin_timetopost-planner_timetopost__get_engagement_by_tag, mcp__plugin_timetopost-planner_timetopost__get_post_metrics
---

# Read-only TimeToPost content planning

1. Ask which workspace the customer explicitly intends to use, then call `whoami` first. Continue only when the returned workspace clearly matches that stated intent. A legitimately authorized agency workspace is allowed when the customer explicitly selected it. If the result differs or is ambiguous, stop and ask the customer to switch or clarify; do not inspect any content first.
2. Use `get_capabilities` to interpret current fields. Read only what the task needs: existing posts, prompt suggestions/library, timing, integrations, engagement, metrics, brands, drafts, approvals, or scheduler health.
3. Produce the plan in chat. Label observed data, interpretation, and proposed copy separately. A proposed idea is not a TimeToPost draft.
4. Never call tools that create drafts, upload media, connect or regroup accounts, schedule, publish, approve, reject, cancel, send, configure, or otherwise mutate state—even if the server exposes them.

The `allowed-tools` list pre-approves these calls for this skill's invocation turn; it does not restrict the available tool pool or enforce read-only access. The workflow's read-only behavior comes from the instructions above. Ask for no production credentials and do not claim platform publication or approval status.
