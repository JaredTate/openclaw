openclaw is running on this os. its code is in our Code folder. I need you to read '/home/jared/Documents/openclaw-claude-cli-setup-guide_v2.md' and i just pulled many commits to our openclaw repo. i need you to update openclaw and make sure our modification is good to go. read this guide for troubleshooting info https://docs.openclaw.ai/help/troubleshooting i want you to compile from most recent commit. ultrathink and do this correctly. update openclaw config if neededed and make sure you restart the gateway.

## OpenClaw Upgrade Prompt

OpenClaw is running on this OS. Its repo is in the `Code` folder, usually `~/Code/openclaw`. I just pulled many commits to the OpenClaw repo. Update OpenClaw from the most recent commit and make sure the local modification is good to go.

First read `/home/jared/Documents/openclaw-claude-cli-setup-guide_v2.md`. Also read the troubleshooting guide at `https://docs.openclaw.ai/help/troubleshooting`. Do not run `openclaw doctor --fix` unless explicitly told to, because the local setup guide may warn against it.

Do this carefully:

1. Check the repo status and current HEAD.
2. Install/update dependencies only as needed.
3. Compile/build OpenClaw from the current most recent commit.
4. Pack/install the built OpenClaw globally or by the repo's established local install flow.
5. Verify `openclaw --version` matches the built version/commit.
6. Update OpenClaw config only if needed, preserving existing local settings.
7. Restart the OpenClaw gateway.
8. Run health checks:
   - `openclaw gateway probe`
   - `openclaw channels status --probe`
   - `openclaw status`
   - `openclaw doctor`
9. Troubleshoot and fix real startup/config/model/plugin errors.
10. Report the final installed version, commit, gateway status, health check results, config changes, and any remaining warnings.

### Additional

For this upgrade, update OpenClaw config to use GPT 5.5 instead of GPT 5.4:

- Set alias `gpt` to `openai-codex/gpt-5.5`.
- Set the default agent model to `openai-codex/gpt-5.5`.
- Set the default subagent model to `openai-codex/gpt-5.5`.
- Set heartbeat and any active-memory/default helper model config to `openai-codex/gpt-5.5` if those are currently pinned to GPT 5.4.
- Update every cron job model in `~/.openclaw/cron/jobs.json` to `openai-codex/gpt-5.5`, including disabled jobs, so stale cron jobs do not silently use GPT 5.4.
