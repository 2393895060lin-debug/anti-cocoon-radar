# Setup

## Prepare local state

1. Copy `config/radar_config.example.yaml` to `config/radar_config.local.yaml`.
2. Fill in local paths, topics and optional notification settings.
3. Create the configured log directory locally. Do not add it to Git.
4. Keep authentication material outside the repository.

## Test manually

Run `prompts/automation_prompt.zh-CN.md` once in a normal conversation before scheduling it. Verify that the run:

- Uses the intended last-successful-run baseline.
- Rejects repeated or low-value news.
- Includes contrary evidence and limitations.
- Creates no more than the configured maximum number of items.
- Produces and re-reads the expected local report.
- Does not perform installs, purchases, credential operations or unrelated writes.

## Schedule

Create a scheduled task only after the manual test passes. Give it the narrowest filesystem and network access that can complete the job. If it needs local files, the computer and desktop app must be available at run time.

Official OpenAI documentation for scheduled tasks: <https://developers.openai.com/codex/app/automations/>

The repository deliberately does not include a local automation metadata file. Schedule, model, project binding, working directory, account identifiers and connector authorization belong to each user's local environment.

## Notifications

Notifications are optional. Enable them only after confirming the destination and the minimum content that may leave the machine. Send the verified report body only; do not attach configuration, logs from other systems or workspace files.
