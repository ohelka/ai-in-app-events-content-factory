---
name: app-store-in-app-events
description: Create and manage App Store In-App Event campaigns end to end, including event selection from a content plan, metadata drafting, localization, creative production, asset organization, and Apple featuring request copy. Use when Codex is asked to prepare, update, localize, create assets for, or organize an App Store In-App Event.
---

# App Store In-App Events

## Workflow

Follow this order unless the user requests only part of the process:

1. Identify the next event in the connected content plan.
2. Draft the English App Store metadata.
3. Localize the approved metadata into the standard language set.
4. Update the event record in the content plan.
5. Confirm the creative direction with the user.
6. Generate static creatives and, when requested, video assets.
7. Upload or replace the final assets in the connected storage folder.
8. Draft the Apple featuring request.

Treat the content plan, the user's latest brief, and the current Apple requirements as the sources of truth. Pause for approval after the copy stage and before generating final creative assets.

## Metadata

Create these fields for every event:

- `Event Name`
- `Short Description`
- `Long Description`

Use these working limits unless current Apple documentation specifies otherwise:

- `Event Name`: 30 characters
- `Short Description`: 50 characters
- `Long Description`: 120 characters

Do not end descriptions with terminal punctuation. Keep the copy concise, natural, and suitable for App Store editorial review.

## Locales

Use exactly 18 languages unless the user requests a different set. Keep English first:

1. English
2. Arabic
3. Chinese (Simplified)
4. Chinese (Traditional)
5. Finnish
6. French
7. German
8. Greek
9. Indonesian
10. Italian
11. Japanese
12. Korean
13. Polish
14. Portuguese (Brazil)
15. Spanish (Mexico)
16. Spanish (Spain)
17. Swedish
18. Turkish

For each locale, provide:

- `Language / Locale`
- `Event Name`
- `Short Description`
- `Long Description`

Check character counts after translation. Shorten naturally in the target language instead of translating the English structure literally.

## Content Plan

Use a separate event tab or record for each campaign. Preserve unrelated tabs, records, and user edits. Update only the event's metadata area unless the user requests a wider cleanup.

Before writing, verify the connected spreadsheet and target tab. Never store spreadsheet IDs, folder IDs, credentials, or private links in the skill itself.

## Creative Direction

Ask the user what the creative should highlight before generating final assets. Use the latest Apple In-App Event creative guidance as context.

Create App Store-ready event visuals:

- Make the event theme immediately understandable.
- Keep the product experience as the primary visual signal.
- Avoid visible text, logos, and UI overlays unless the user explicitly requests them.
- Avoid abstract or stock-like backgrounds that do not communicate the event.

Default static formats:

- Event card: `1920x1080`, `16:9`
- Event detail page: `1080x1920`, `9:16`

Use descriptive filenames such as:

- `<event-slug>-card-1920x1080.png`
- `<event-slug>-detail-1080x1920.png`

## Video

Use the approved static creative as the starting point. Keep animation subtle unless the brief calls for stronger motion.

- Preserve the composition, furniture, palette, and camera angle.
- Add only theme-appropriate ambient motion.
- Do not add text, captions, logos, UI, or distracting objects.
- Prefer silent video and report if audio is present.
- Verify current Apple media specifications before delivery.

Use descriptive filenames such as:

- `<event-slug>-card-1920x1080-video.mp4`
- `<event-slug>-detail-1080x1920-video.mp4`

## Asset Organization

Verify the connected storage location before writing. Create an event folder only if it does not already exist.

When revising an approved asset, replace the existing file in place when possible so its shared link remains stable. Create a new file only for requested variants or when replacement could remove a needed original.

After every upload or replacement, verify:

- file name
- MIME type
- size
- parent folder
- observed share link

Never invent links or expose private IDs in reports.

## Featuring Request

Write one concise featuring request in English after the metadata and creatives are approved.

The copy should:

- ask Apple to consider featuring the in-app event
- name the event and explain the user experience
- mention timely seasonal or cultural relevance when appropriate
- emphasize creativity, engagement, and product value
- be polished and ready to paste into the submission form

## Completion Report

Summarize:

- event records or tabs updated
- metadata and locales completed
- creatives generated or replaced
- storage folders and files updated
- featuring request status
- any remaining blocker or manual publishing step
