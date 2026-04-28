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
9. Troubleshoot and fix real startup/config/model/plugin errors.
10. Report the final installed version, commit, gateway status, health check results, config changes, and any remaining warnings.

### Additional

For this upgrade, update OpenClaw config to use GPT 5.5 instead of GPT 5.4:

- Set alias `gpt` to `openai-codex/gpt-5.5`.
- Set the default agent model to `openai-codex/gpt-5.5`.
- Set the default subagent model to `openai-codex/gpt-5.5`.
- Set heartbeat and any active-memory/default helper model config to `openai-codex/gpt-5.5` if those are currently pinned to GPT 5.4.
- Update every cron job model in `~/.openclaw/cron/jobs.json` to `openai-codex/gpt-5.5`, including disabled jobs, so stale cron jobs do not silently use GPT 5.4.


Right now, our OpenClaw is configured by compiling from the source code. I want you to uninstall the current OpenClaw and then install it via the script installer, so that way I can easily update. Make sure you keep the same configuration and settings, but I just wanna be able to easily just type OpenClaw update to be able to update. Take your time and do this correctly. curl -fsSL https://openclaw.ai/install.sh | bash read docs as needed https://docs.openclaw.ai/install




Now I want you to do a deep audit of your OpenClock configuration. We recently switched from compiling OpenClock from source to running it via the normal installer and normal upgrade path, so I can just run OpenClock update to keep you updated in the future. But what I need you to do is go through and I need you to do an audit of your OpenClock configuration to make sure it's correct. You need to check your models. Tell me all the models that are configured. You needed to check memory. We need our optimal memory settings, so you need QMD enabled. You need session memory, and we need to make sure that we are able to have memory optimized to the fullest extent possible, so double-check it. You need to be able to read all the OpenClock documentation. That all needs to be indexed in QMD, and everything needs to be up to date, and you need to be able to remember what you do every day and what you've done in the past and not forget things. And we need to be able to switch between models, and you need to be able to remember things. You need to check for any issues. You need to make sure that tail scale is up and configured. Make sure that you are able to use your Chrome browser, so you have your browser profile, and you're able to open and do things, and you need to make sure that everything is good to go. So tell me if we need to change anything or tweak anything, and then tell me if there's anything that you could optimize or enable in your OpenClock configuration that would make my life better and easier and make you more powerful, okay? There's been a lot of updates over the last few versions, and I haven't really kept up with it, so you need to look through the last four versions and the release notes, okay? But give me a concise summary of all this. You know, don't go overboard, but I want you to tell me everything that we need to do, okay? We also need to make sure that GPT 5.5 is the default model for our OpenAI configuration, both for sub-agents as well as cron jobs and tasks. Okay? Make sure that that's configured. And so if you need to make any changes and optimize and turn anything on, do that and then restart the gateway, but tell me what you're gonna do. Okay?
