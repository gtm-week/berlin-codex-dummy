# Public product documentation excerpt

Retrieved 2026-11-16 from https://github.com/gtm-week/gtm-brain/blob/main/README.md
Source blob: ea3079da10e4e92a43f0e6a678774ee5806236f2
Only lines 1-90 retained. Reference text, not workshop setup instructions.

<a href="https://gtm-brain.ai/">GTM Brain product logo (see included brand asset)</a>

# GTM Brain

[Website](https://gtm-brain.ai/) · [Start here](https://github.com/gtm-week/gtm-brain/blob/main/README.md#start-here) · [Install](https://github.com/gtm-week/gtm-brain/blob/main/README.md#install-in-codex) · [Configure](https://github.com/gtm-week/gtm-brain/blob/main/README.md#configure-your-brain) · [Put it to work](https://github.com/gtm-week/gtm-brain/blob/main/README.md#put-it-to-work) · [Dashboard](https://github.com/gtm-week/gtm-brain/blob/main/README.md#the-dashboard) · [The four parts](https://github.com/gtm-week/gtm-brain/blob/main/README.md#the-four-parts-of-a-brain) · [Architecture](https://github.com/gtm-week/gtm-brain/blob/main/README.md#how-it-fits-together) · [Skills](https://github.com/gtm-week/gtm-brain/blob/main/README.md#shipped-skills)

**For GTM engineers building research, account and campaign workflows in Codex.**

A new chat should not mean pasting your ICP again, hunting down the last customer conversation,
or reconstructing where a playbook stopped. GTM Brain keeps your ICP, offer, customer evidence
and playbook progress in local files that your agent can use across chats and linked projects.

It installs as the **`gtm-brain` plugin**. Open source under [MIT](https://github.com/gtm-week/gtm-brain/blob/main/LICENSE).
[Codex](https://github.com/gtm-week/gtm-brain/blob/main/README.md#install-in-codex) is the primary host; [Claude Code support is in beta](https://github.com/gtm-week/gtm-brain/blob/main/README.md#claude-code-beta).

## Start here

**New to GTM Brain**

1. Install it: [Install in Codex](https://github.com/gtm-week/gtm-brain/blob/main/README.md#install-in-codex), one message to Codex.
2. Open a new Codex chat in an empty folder and send `/gtmb-start`. It creates the brain, asks
   about your business and connects your tools.
3. Work as usual. Say what happened ("just got off a call with ..."), ask what you need
   ("brief me on Acme", "what should I focus on this week?"), and say "open the dashboard" to
   see what the brain holds.
4. Shape it with the two commands that matter most: `/gtmb-rules` (what Codex saves and asks,
   where files go) and `/gtmb-schema` (what is kept about each person and company).

**Already using it**

1. Say "update GTM Brain" in Codex, then quit and reopen Codex.
2. Start a new chat in the brain folder and read the first reply: it says what was refreshed.
3. Since 0.36 the skills are `/gtmb-<name>` (they were `/gtm-brain-<name>`), and 0.36.1 names
   two after what they do: `/gtmb-icp` and `/gtmb-market-research`. An old name still works:
   Codex runs the new skill and tells you its name. If your brain's own files still use old
   names, Codex offers once to update them.
4. If the reply says the brain can be upgraded, say "upgrade the brain".

If several people use the same brain, everyone updates the plugin before anyone says "upgrade
the brain".

Details: [Updating and upgrading](https://github.com/gtm-week/gtm-brain/blob/main/README.md#updating-and-upgrading).

**How the brain works**

![The brain in one picture. Configuration, on the left, says what is allowed: it sets the fields and kinds of entities and checks every save into memories, and it changes only when you edit the file or approve a change Codex proposes. Entities are who and what the memories are about; names resolve and links derive from the memories. Codex, where you talk, is the only thing that reads your tools, reads the brain and saves into it. Notes and entities keep a link back to their source in your tools. Workflows, underneath, run through Codex under the rules and save each step as a note.](https://github.com/gtm-week/gtm-brain/blob/main/diagrams/brain-in-one-picture.svg)

Read it left to right. **Configuration** says what is allowed; it shapes the entities and checks
every save, and it changes only two ways (red): you ask in chat and approve what Codex proposes,
or you edit the file. **Memories** are what happened and **entities** are who and what they are
about. **Codex** is where you talk, and the only thing that reads your tools, reads the brain
and saves into it. **Your tools** keep the raw material; a dashed line is the link a note or an
entity keeps back to its original. **Workflows** are the part that acts: they run through
Codex, under the rules, and leave each step as a note.

- **It is a folder of plain files in git on your computer.** Nothing is stored anywhere else.
- **You talk, Codex saves.** What happened, was decided or is open becomes a dated note with
  its source. Notes are never edited; a correction replaces the old note and keeps it. Codex
  never guesses who someone is: it saves the note and asks.
- **People, companies and products are linked across notes,** with their relationships and
  history (who worked where, who is a customer).
- **Your base documents steer the work:** strategy, ideal customer profile, tone of voice,
  design system. Codex reads them before the work they apply to.
- **Your rules and schema decide** what Codex saves and asks, where files go, and what is kept
  about each person and company.
- **The dashboard shows the same files:** what needs you, housekeeping, entities, notes,
  workflows and configuration. Documents, entities and notes can be edited there.

More: [The four parts of a brain](https://github.com/gtm-week/gtm-brain/blob/main/README.md#the-four-parts-of-a-brain) · [The folders of a brain](https://github.com/gtm-week/gtm-brain/blob/main/README.md#what-is-stored-on-disk) · [How GTM Brain works](https://github.com/gtm-week/gtm-brain/blob/main/README.md#how-gtm-brain-works) · [How a brain works](https://github.com/gtm-week/gtm-brain/blob/main/plugins/gtm-brain/MANUAL.md).

**Configure it:** one table of commands in [Configure your brain](https://github.com/gtm-week/gtm-brain/blob/main/README.md#configure-your-brain).

## Install in Codex

Already have GTM Brain? Do not install again: see [Updating and upgrading](https://github.com/gtm-week/gtm-brain/blob/main/README.md#updating-and-upgrading).
Still on the plugin's old name, `gtm-os`? Follow [MIGRATING.md](https://github.com/gtm-week/gtm-brain/blob/main/MIGRATING.md).

Requires the **Codex desktop app** and **Node 22.16+ (22.x) or Node 24+**. The guided installer checks your environment.

Open a new Codex chat and send:

```text
Read https://github.com/gtm-week/gtm-brain/blob/main/INSTALL.md and follow it exactly. Read nothing else in that repository.
```

Follow the setup and permission prompts. Codex installs the plugin, opens your working folder,
and guides you through your business context and tool connections. No GitHub invitation or
sign-in is required to download the plugin.

[First-use walkthrough](https://github.com/gtm-week/gtm-brain/blob/main/ONBOARDING.md) · [Everyday guide](https://github.com/gtm-week/gtm-brain/blob/main/GUIDE.md) · [Manual installation](https://github.com/gtm-week/gtm-brain/blob/main/README.md#manual-installation) · [Claude Code (beta)](https://github.com/gtm-week/gtm-brain/blob/main/README.md#claude-code-beta)
