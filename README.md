🤖 DystopAI
> **Premium command center for multi-model AI agents.**
DystopAI Agent Control Center is a local command surface for running, supervising, and coordinating OpenClaw agents. Use it to recruit agents, chat with your roster, launch missions, monitor live runtime activity, and manage gateway plugins like ClawTalk.
![Agents tab](assets/user-guide/agents.png)
---
📌 Table of Contents
✨ What DystopAI Does
⚡ Quick Start
🧭 Main Navigation
🧠 Agents
🆕 Recruit Agents
✏️ Edit Agents
🚀 Missions
📡 Monitor
🧩 Plugins
🔐 Provider Auth & Models
✅ Good Operating Habits
🛠️ Troubleshooting
📚 Documentation References
🧾 Glossary
🚑 Fast Recovery Checklist
---
✨ What DystopAI Does
DystopAI gives operators and builders a central control room for AI agent work.
Use it to:
🧠 Create and manage agents with profiles, models, workspaces, policies, skills, and runtime settings.
💬 Chat with one agent or a confirmed party through the Command Console.
🎯 Launch structured missions with objectives, modes, acceptance gates, verification commands, and timing controls.
📡 Monitor live activity across sessions, gateway health, runtime calls, logs, plugins, and channel traffic.
🧩 Enable or stop plugins such as ClawTalk, Browser Control, and other OpenClaw runtime surfaces.
🔐 Connect model credentials through OAuth or API keys depending on the provider.
Last updated: `2026-06-06`
---
⚡ Quick Start
1. Start the app
Choose the launch mode that matches your setup:
```bash
# Development mode
npm install
npm run dev
```
```bash
# Bundled server mode
npm run build:standalone
```
Or open the packaged DystopAI desktop app.
2. Open the Control Center
Mode	URL
🖥️ Local app	`http://127.0.0.1:4050/`
⚙️ Vite dev server	`http://127.0.0.1:5173/`
3. Log in
Default local development token:
```text
dev-token-change-me
```
To change it, set this environment variable before starting the server:
```bash
CONTROL_CENTER_TOKEN="your-new-token"
```
4. Connect model credentials
Open an agent.
Go to Model.
Pick the primary model.
If auth is missing, click Connect or Update Auth.
Use OpenAI Codex OAuth for Codex subscription-backed models.
Use API keys for provider API-key models.
5. Build your active party
Add agents to the active party.
Confirm the party.
Send a message or deploy a mission.
---
🧭 Main Navigation
The left rail is your command map.
Area	Use it for
🆕 `Recruit`	Create a new agent and bootstrap markdown files.
🧠 `Agents`	Browse your roster, build the active party, edit agents, and chat.
🚀 `Missions`	Define structured work and send it to one or more agents.
📡 `Monitor`	Watch active runs, sessions, gateway health, logs, and cleanup controls.
🧩 `Plugins`	Enable, disable, and inspect OpenClaw runtime plugins.
The header badges show live state:
👥 Total agents
🎛️ Active party size
🏃 Running turns
📡 Gateway state
💬 Open sessions
📈 Response count
---
🧠 Agents
![Agents tab](assets/user-guide/agents.png)
The Agents tab is the everyday command area for building your roster, selecting who works, and chatting with agents.
🎛️ Active Party
The Active Party strip holds the agents that receive party or mission work.
Use it like this:
Click Deploy on an agent card to add that agent.
Drag agents between slots to reorder them.
Click Remove or the slot x to remove an agent.
Click Confirm before running party-wide work.
> 💡 **Slot order matters:** Slot 1 is often treated as the commander or lead lane in mission modes.
🗂️ Agent Registry
The registry shows all available agents. Each card displays the agent name, class, role, level, high-level attributes, tags, and party status.
Useful controls:
🔎 Search by name, role, or keyword.
↕️ Sort by party priority, level, name, or rarity.
💎 Filter by rarity.
🧱 Switch between showcase, grid, and list layouts.
✏️ Use Edit to open the agent editor.
💬 Command Console
The Command Console sends direct messages or party broadcasts.
Common patterns:
Send one agent a direct prompt.
Send multiple agents a parallel request.
Use the confirmed party for coordinated work.
Attach files when the task needs extra context.
Watch responses appear as agents complete their turns.
Good prompt:
```text
Review the authentication flow. Report bugs first, then list exact files you inspected.
```
Weak prompt:
```text
Fix everything.
```
---
🆕 Recruit Agents
![Recruit agent modal](assets/user-guide/recruit-agent.png)
Recruit creates a roster card and the agent’s bootstrap files in one pass.
Recommended workflow:
Click Recruit.
Enter a human-readable name.
Confirm or edit the generated agent ID.
Add a profile picture URL, app-relative image path, or local path.
Choose a profile type:
⚒️ `Executor` — implementation and verification.
🏗️ `Architect` — system design and handoffs.
🛡️ `Auditor` — risk and regression review.
🔬 `Researcher` — evidence gathering.
🧬 `Hybrid` — mixed work.
Choose model, workspace, and runtime lanes.
Review the generated bootstrap markdown.
Click Recruit Agent.
The bootstrap files define the agent’s identity, behavior, tools, and operating memory. Keep them specific, practical, and mission-ready.
---
✏️ Edit Agents
![Agent editor](assets/user-guide/agent-editor.png)
Open the editor from any agent card with Edit.
Tab	What it controls
👤 `Profile`	Name, portrait, class, role, level, and behavior profile.
🧠 `Model`	Primary model, fallbacks, provider auth, thinking level, and run timeout.
⏱️ `Scheduler`	Cron cadence, idle timeout, loop flag, and recovery mode.
🛡️ `Policy`	Sandbox and tool allow/deny policy.
📁 `Workspace`	The folder this agent should work in.
🧰 `Skills`	Installed skills, learned skills, and ClawHub search/install flows.
📄 `Files`	Agent control files such as `SOUL.md`, `TOOLS.md`, and related resources.
Use Model when an agent fails because of missing credentials, stale OAuth, quota, or the wrong provider.
Use Policy when an agent needs access to specific tools or should be denied dangerous tools.
---
🚀 Missions
![Missions tab](assets/user-guide/missions.png)
Missions turn loose objectives into structured work. They are best when you need multiple agents, verification, or repeated background effort.
📋 Mission Templates
Template	Best for
🧹 `Code Sweep`	Parallel code review or cleanup.
🗺️ `Mission Plan`	Planning and ownership breakdown.
🔬 `Research Map`	Evidence gathering.
🚢 `Launch Push`	Implementation, verification, and polish.
🎛️ `Command Ops`	Lead-agent delegation and follow-up.
🎮 Mission Modes
Mode	Use when
👑 `Command`	Slot 1 should delegate and synthesize. Good default for coordinated work.
⚡ `Parallel`	Everyone should start immediately on separate lanes.
🎯 `Specialist`	Only agents matching the capability should run.
🔁 `Relay`	Agents should work in order, each building on the last handoff.
🐝 `Swarm`	You want broad ideas or many research angles.
🧱 Mission Types
Type	Best for
🏗️ `Build`	Code or artifact changes.
🧭 `Plan`	Scope, milestones, and risks.
🔎 `Research`	Source-backed findings.
🎛️ `Command`	Delegation and coordination.
🧠 `Memory`	Learning, recall, and continuity work.
✅ Acceptance Gates
Acceptance gates are the proof checklist. Write them as lines, one gate per line.
Example:
```text
At least one user-facing path is verified end to end.
Changed files are named and scoped to the requested feature.
Build or test evidence is reported, or the blocker is explicit.
Residual risks are listed before closing the mission.
```
🧪 Verification Commands
Use commands that prove the work is healthy.
Examples:
```bash
npm run build
npm run lint
```
> ⚠️ Avoid expensive or destructive commands as defaults. Agents may run these during verification.
⏳ Timing
Open Timing to choose the mission duration.
Timing	Behavior
⚡ `Strike`	One leader-worker-review cron cycle.
⏱️ `Timed`	Cron cycles until the configured duration ends.
🔁 `Loop`	Cron cycles until stopped.
👀 `Watch`	Persistent background mission controlled by cron.
Timed, Loop, and Watch missions run through backend-owned OpenClaw cron jobs. Slot 1 runs first, worker agents run after the leader pass, and Slot 1 reviews the round before the scheduler continues or stops.
---
📡 Monitor
![Monitor overview](assets/user-guide/monitor.png)
The Monitor tab answers one question:
> **What is the program doing right now?**
Top badges show:
🧵 Active sessions
🏃 Running agent calls
📡 Gateway health
💬 Open sessions
📊 Monitor Subtabs
Subtab	Use it for
📍 `Overview`	Agent state, current phase, uptime, memory, and average turn time.
⏱️ `Scheduler`	Cron cadence, retry count, loop flag, and recovery mode.
📈 `Performance`	Turns, success rate, runtime, stability, and efficiency metrics.
📜 `Logs`	Mission and runtime event tail.
🌐 `Gateway`	Gateway process, loaded plugins, live calls, open sessions, channel traffic, and log tail.
🌐 Gateway Panel
![Monitor gateway tab](assets/user-guide/monitor-gateway-redacted.png)
The Gateway panel is the best place to confirm whether background plugins are actually alive.
Key areas:
🧠 Gateway Runtime: port, PID, uptime, health, restart count, and stop control.
🧩 Plugin Surface: loaded or managed plugins with quick Stop controls.
🏃 Live Runtime Calls: active agent turns that are still running.
💬 Open Agent Sessions: sessions that can still receive context or be reused.
📡 Channel Activity: inbound, outbound, and system channel events.
📜 Gateway Log Tail: latest gateway stdout/stderr and parsed file-log entries.
Use Close on a session when you want to stop reusing that conversation context.
Use Close all when you want to clear every open runtime session.
Use Stop gateway when you want gateway listeners and channel plugins off until a gateway-backed action starts them again.
Use Clean Slate when the UI/runtime looks stuck, old sessions look live, or you want a fresh monitor surface.
---
🧩 Plugins
![Plugins tab](assets/user-guide/plugins.png)
Plugins are runtime modules and provider surfaces. Some provide model providers, some provide communication channels, and some provide tools.
📞 ClawTalk
ClawTalk is bundled with the desktop app and appears enabled on first run.
Setup flow:
Add the ClawTalk API key in Setup.
Refresh or restart the gateway.
Confirm the WebSocket connects.
Check Monitor > Gateway > Plugin Surface to verify ClawTalk is running.
🎯 Multi-Agent Routing
ClawTalk supports multi-agent targeting with `@agent` prefixes in SMS, voice, or walkie channels.
Examples that route to Diana when her agent ID is `hn-crypto-technical`:
```text
@Diana
@Diana Reyes
@diana-reyes
@hn-crypto-technical
```
Scheduled cron/reminder requests created from a routed message stay under that same target agent.
ClawTalk refreshes agent routing config before each routed turn. When you save model, workspace, thinking, timeout, or agent-list changes, the next SMS/voice/walkie turn uses the updated settings. If the config is temporarily invalid while being edited, ClawTalk keeps using the last usable snapshot until the next valid save.
🧰 Common Plugin Tasks
Use the search field to find a plugin.
Toggle the plugin on or off.
Watch the status chips:
🟢 `enabled` — configured to load.
⚫ `disabled` — configured not to load.
🔵 `loaded` or `running` — active in the current gateway process.
Click Refresh after changes or after restarting the gateway.
Important behavior:
Disabling a plugin should prevent new messages or channel events from waking it.
Some plugin changes need a gateway restart before the runtime matches the config.
Monitor > Gateway > Plugin Surface shows what is loaded in the current gateway process.
To stop ClawTalk, stop it from either Plugins or Monitor > Gateway > Plugin Surface. Confirm it no longer appears as running and that Channel Activity stops receiving ClawTalk events.
---
🔐 Provider Auth & Models
Most agent failures come down to model auth, provider quota, or stale sessions.
Use this checklist:
Open the agent editor.
Go to Model.
Confirm the Primary Model.
If the model shows missing auth, click Connect.
For Codex subscription-backed models, connect OpenAI Codex OAuth.
For provider API models, save the provider API key.
Save the model config.
Send a small test prompt.
If a model works in direct chat but fails from a plugin, check Monitor > Gateway logs and Plugin Surface. The plugin may be using a different runtime path, stale session, or disabled provider.
---
✅ Good Operating Habits
🎯 Keep the active party small for direct work.
🧪 Add verification commands when work touches code.
✅ Put proof in acceptance gates before launching missions.
🧹 Close stale sessions before testing changed auth or model config.
🛑 Stop communication plugins when you do not want external messages to wake agents.
🔐 Keep secrets out of mission descriptions and prompts unless required.
📡 Treat Monitor > Gateway as the source of truth for background activity.
---
🛠️ Troubleshooting
🔑 I cannot log in
Check the token.
Token type	Value
Default local token	`dev-token-change-me`
Custom token	`CONTROL_CENTER_TOKEN`
If the token changed, clear the browser’s stored `control-center-token` or log in again.
📡 The gateway says off, checking, or unhealthy
Open Monitor > Gateway.
Try this order:
Wait a few seconds for health polling.
Check whether port `18789` is shown.
Use Stop gateway, then run a gateway-backed action to start it again.
Restart the Control Center server.
Check the Gateway Log Tail for startup errors.
🧠 An agent does not respond
Check:
Is the agent selected or in the confirmed party?
Is the primary model configured?
Does provider auth show connected?
Is there a provider quota or rate-limit error?
Is the agent already busy?
Is there a stale open session that should be closed?
Does the prompt require tools that the agent policy denies?
🎯 The wrong agent responded
Check the Command Console To chips. Remove agents you do not want in the current chat. If using a party, confirm the party before sending.
🧵 Old context keeps affecting answers
Open Monitor > Gateway, then close the relevant session.
For a full reset, use Close all or Clean Slate.
🧩 A plugin still responds after I stopped it
Check both surfaces:
Plugins: the plugin should be disabled.
Monitor > Gateway > Plugin Surface: the plugin should not be running or loaded.
Channel Activity: no new inbound/outbound events should appear for that plugin.
If events still appear, restart the gateway from Monitor or restart the app server.
📞 ClawTalk does not show messages or replies
Open Monitor > Gateway.
Look at:
Plugin Surface: ClawTalk should be running if you expect SMS/voice activity.
Channel Activity: inbound SMS, outbound SMS, and system events should appear here.
Gateway Log Tail: handler errors, auth errors, and connection errors appear here.
Open Agent Sessions: SMS sessions should show activity when messages are routed to an agent.
If ClawTalk is stopped, new messages should not wake it until you enable it again.
🚫 I see `401 Unauthorized` or invalid token
Reconnect the provider used by the selected model.
Codex subscription models: reconnect OpenAI Codex OAuth.
API-key models: update the provider API key.
Google Vertex: check `gcloud` auth, project, and location.
After reconnecting, close stale sessions and retry with a small prompt.
🧠 I see `CLI transcript compaction failed for openai/gpt-5.5`
Current builds keep automatic Codex compaction inside the Codex runtime, so this should not stop a mission. If you see it on an older build or after changing runtimes, use this recovery order:
Restart the gateway or app so it loads the current bundled OpenClaw runtime.
Open the agent editor, go to Model, and confirm OpenAI Codex is connected for subscription-backed `openai/gpt-5.5` missions.
If the agent should use direct OpenAI API billing instead of Codex OAuth, save an OpenAI API key for that agent.
Close the stale session in Monitor > Gateway, then relaunch the mission with a small test prompt first.
⏳ I see a subscription or rate-limit message
The provider accepted the credential but denied the request because of account limits or quota.
Options:
Wait until provider usage resets.
Switch the agent to another configured model.
Reduce parallel lanes.
Avoid repeated mission loops until quota is available again.
🚀 A mission will not deploy
Check:
At least one agent is in the active party.
The party is confirmed.
The mission has a title and objective.
Acceptance gates are not empty.
Model auth is connected for every selected agent.
No selected agent is already running a long task.
🕰️ A mission is running too long
Use Stop Mission in the Missions tab, then open Monitor > Gateway and close any active sessions or runtime calls that remain.
📎 Attachments do not work
Check the file path, size, and whether the agent has access to the workspace or tool needed to inspect the file.
Some attachment-heavy prompts route through the OpenClaw runtime instead of direct streaming, so gateway health matters.
🌐 The Browser plugin is off
Open Plugins, search for Browser Control, and enable it. Refresh plugins, then retry the browser-related agent task.
---
📚 Documentation References
Local project docs
README.md
CORE_PROJECT.md
Bundled OpenClaw docs
OpenClaw docs index
Agent runtime architecture
OpenClaw agent runtime
Authentication credential semantics
Plugin management
Building plugins
Skills
Channels
SMS channel
Channel troubleshooting
Automation troubleshooting
---
🧾 Glossary
Term	Meaning
🤖 Agent	A configured OpenClaw persona with model, workspace, policy, cron cadence defaults, and skills.
🎛️ Active Party	The set of agents selected for party chat or mission work.
👑 Slot 1	The lead party position, often used as the commander in coordinated missions.
🚀 Mission	A structured task with mode, objective, acceptance gates, verification, and timing.
📡 Gateway	The OpenClaw background process that runs plugins, channels, and gateway-backed runtime activity.
🧩 Plugin Surface	The currently loaded or managed plugins visible from the gateway monitor.
💬 Session	A reusable conversation/runtime context for an agent or channel.
📞 ClawTalk	A communication plugin for voice, SMS, missions, and approvals.
🔌 Provider	A model or service backend such as OpenAI, OpenAI Codex, Google, DeepSeek, or others.
🔐 OAuth	Browser sign-in based credential flow, used by providers such as OpenAI Codex and Google.
🗝️ API key	Provider-issued secret used to call a provider API directly.
---
🚑 Fast Recovery Checklist
When something feels wrong:
📡 Open Monitor.
🩺 Check gateway health.
🏃 Check running calls.
🧹 Close stale sessions.
📜 Read the latest Gateway Log Tail.
🔐 Confirm provider auth.
🧪 Retry a small direct prompt.
🚀 Relaunch the mission or plugin flow only after the small prompt works.
---
🏁 Recommended First Test
After setup, run one tiny direct prompt before launching a mission:
```text
Confirm you are online. Reply with your agent name, primary model, workspace, and one sentence describing what you can do.
```
Then check Monitor > Gateway to confirm sessions, logs, and runtime state look healthy.
