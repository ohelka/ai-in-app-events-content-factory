# AI-Powered Content Factory for App Store In-App Events

A reusable AI-assisted workflow for producing App Store In-App Events—from planning and localization to creative production, asset handoff, and featuring copy.

It reduced the production time for a single event from **~5 hours to ~1 hour**, while keeping human approval at the moments where creative judgment matters.

## The Problem

App Store In-App Events were a recurring marketing task, but each event required the same manual production cycle from scratch.

For every campaign, I had to:

- select the next event from the content plan
- prepare App Store metadata
- adapt the copy to platform requirements
- localize it into 18 App Store languages
- create static or video assets
- organize and upload the final creatives
- prepare editorial copy for Apple featuring consideration

The process involved several tools, repeated handoffs, and a lot of copy-and-paste work. Producing one event typically took **around 5 hours**, even though most of the workflow was highly repeatable.

The problem I wanted to solve was simple:

> **Could I turn this recurring manual process into a reusable AI workflow where I provide the event context once, approve the key decisions, and let the agent handle almost the entire production cycle automatically?**

That became the foundation for the **AI In-App Events Content Factory**.

## The Solution

Instead of creating another one-off prompt, I built an AI workflow that executes the complete production pipeline.

The workflow starts with a dedicated Google Sheets content plan connected to Codex. The agent reads the upcoming event, drafts the English metadata, adapts it to App Store requirements, and localizes it into the 18 languages used for production.

After the copy is approved, the workflow moves to creative production. Codex asks what should be highlighted in the visuals and uses Apple's In-App Event creative guidelines as context. It can create static assets directly and, when video is required, send the approved creative direction to Higgsfield for motion generation.

Finally, the agent uploads each asset to the correct Google Drive folder, replaces files when revisions are requested, and prepares the editorial copy for Apple featuring consideration. The only remaining manual step is publishing the event in App Store Connect.

## AI Workflow

```text
Google Sheets Content Plan
            │
            ▼
Select Upcoming Event
            │
            ▼
Generate English Metadata
            │
            ▼
Localize to 18 Languages
            │
            ▼
Human Approval
            │
            ▼
Define Creative Direction
            │
            ▼
Generate Static Creatives
            │
            ▼
Generate Video in Higgsfield
            │
            ▼
Organize Assets in Google Drive
            │
            ▼
Draft Apple Featuring Request
            │
            ▼
Ready for App Store Connect
```

## AI Stack

| Tool | Purpose |
| --- | --- |
| **Codex (GPT-5.6 Sol)** | Workflow orchestration |
| **Google Sheets** | Content calendar and event source |
| **ChatGPT Image Generation** | Static creative generation |
| **Higgsfield** | AI video generation |
| **Google Drive** | Automatic asset organization and delivery |

## My Role

I designed and built the entire workflow:

- mapped the complete production pipeline
- designed the AI agent logic
- connected Google Sheets as the event source
- wrote the prompting strategy and workflow instructions
- incorporated Apple's In-App Event creative guidelines
- integrated Higgsfield for AI video generation
- automated asset delivery into Google Drive
- generated Apple featuring submission drafts
- tested and iterated the workflow across multiple events

## Results

- Reduced production time per In-App Event from **~5 hours to ~1 hour**
- Automated nearly the entire In-App Event production workflow
- Eliminated repetitive localization work across **18 languages**
- Connected planning, creative production, tracking, and asset handoff in one workflow
- Automated creative asset organization in Google Drive
- Created a reusable Codex skill for future campaigns

## Why Codex?

This project was also an experiment in evaluating different AI models for production workflows.

Instead of building the workflow in Claude, I intentionally chose **Codex** to understand how well it could orchestrate a multi-step marketing pipeline involving external connectors, structured reasoning, and creative generation.

Although my previous experience with Codex had been mixed, **GPT-5.6 Sol** handled the workflow reliably and became the foundation of this automation.

The result showed that Codex could coordinate a complex sequence of marketing tasks—not just generate text, but manage an end-to-end production process.

## Reusable Codex Skill

The workflow is implemented as a reusable **Codex skill** rather than a one-off prompt.

The skill defines the end-to-end process for:

- selecting upcoming events from the content plan
- creating App Store metadata
- localizing copy into 18 languages
- updating production tracking in Google Sheets
- preparing static and video creatives
- organizing assets in Google Drive
- drafting copy for App Store featuring consideration

**[View the App Store In-App Events skill](skills/app-store-in-app-events/SKILL.md)**

The goal was to encode the repeatable production logic once and reuse it for future events instead of rebuilding the workflow for every campaign.

## Repository Structure

```text
ai-in-app-events-content-factory/
├── README.md
├── LICENSE
├── images/
└── skills/
    └── app-store-in-app-events/
        └── SKILL.md
```

## License

This project is available under the [MIT License](LICENSE).
