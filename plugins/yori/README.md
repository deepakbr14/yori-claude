# Yori for Claude — private development build 0.3.7

Yori is a personal AI designed to develop a deeper understanding over time. This package supplies five skills and a hosted MCP connector. It uses the existing Yori account and Personal/Shared Cortexes, Self activation, Lightning retrieval, evidence-grounded learning and turn completion. The Viewer stays at https://yori-prod-e70c6.web.app/ and Admin remains local.

## Before installing

This ZIP is built locally. API 10.62.3 and shared MCP 0.33.0 are deployed, including direct application files and owner-only application data administration. This private Claude ZIP has not been uploaded, and live Claude model acceptance is not claimed. No API keys or credentials belong in this ZIP. Existing Yori embedding/storage costs still apply.

## Install privately after deployment

1. Open Claude web → Customize → Plugins → Add → Upload plugin.
2. Choose Yori_Claude_0.3.7.zip. No directory submission or GitHub repository is needed.
3. Open Yori → Connectors → add/connect Yori. On an organization plan an Owner may need to add it first.
4. Use Claude's published OAuth identity if asked. Sign in on the existing Yori login page using your Yori account. Do not enter a Firebase/API secret. The connector URL is https://yori-plugin-mcp-w55m4wy4oa-uc.a.run.app/mcp/claude.
5. In a new chat type /yori and select the Yori skill; the picker may display yori:yori. Natural requests to talk with Yori also match it.

## Test

1. `/yori Call get_yori_profile and report the connected profile.` Confirm it is your intended Yori account.
2. `Validation only: what is my saved explanation preference? Use Cortex. Do not save anything.` Confirm current_self and situational_cortex were supplied and finish_turn completed.
3. `For a fictional test called Copper Finch Claude, retain this requirement: conversion creates a separate copy and preserves the original. Keep it fictional.` Require an actual persisted receipt. Then record a design intended to satisfy it, without claiming implementation or execution. Do not force an Edge.
4. In a fresh Yori chat ask what requirement that fictional design addresses, and whether implementation was established. Check saved IDs/relationship and qualifications.
5. Test an authorized Shared Cortex, attachment-backed learning and a GO turn. Shared access must match the existing account.
6. Keep an owner-authorized Program open in Viewer; inspect its observation and test a typed action. Only execution acknowledgement establishes success.

## Limitations

Claude web chooses when to load skills and has no guaranteed before/after-message hooks. Verify activation and completion rather than assuming them. Host permission prompts can interrupt tools. Claude's own memory is separate from Cortex. Attachments must be read and their bounded useful evidence explicitly passed to Cortex.

Yori Programs continue to work through MCP and the separate Viewer. Programs now support declared bounded shared data and are independent of Sites and Artifacts. Existing external applications are not migrated automatically. No inline Viewer is included. Browser/app icon placement is controlled by Claude; this package preserves the exact approved icon bytes.

## Local rebuild

Run `python3 build_plugin.py`, then `python3 -m unittest discover -s test -p '*_test.py'`. The build also refreshes `dist-github/`, the copy published to https://github.com/deepakbr14/yori-claude for friends to install as a marketplace; never edit `dist-github/plugins/yori` by hand. Raise the version in `.claude-plugin/plugin.json` for every release so installed copies update. The builder includes only the manifest, connector configuration, README, approved icon and five skill folders. It excludes server code, dependencies, development files and secrets. Private development only; no public license/distribution grant is added.

Programs are managed through direct source tools and verified server assets. See the packaged Programs contract.

Binary assets use write_program_binary_file: exact original bytes encoded by an authorized host, bounded Base64 chunks, owner-bound uploads and final SHA-256 verification. Supports static images, audio and web fonts; no provider file service or ZIP. See the Programs Contract for protocol, quotas and byte-access limitations. Local implementation/test results are in backend/docs/PROGRAM_BINARY_FILES.md (relative to current). Nothing is deployed by rebuilding a package.

Programs now have one current application. Temporary staging and internal hashes protect publication; historical applications and rollback are not retained. Backend deployment includes yori_program_asset_cleanup, an hourly bounded queue worker for expired source artifacts. Player/application data is outside cleanup. See backend/docs/PROGRAM_CURRENT_APPLICATION.md relative to current for owner deployment details.

Owner data tools are describe_program_data, list_program_data, export_program_data, preview_program_data and manage_program_data. Read the Programs skill and canonical contract before authorized data work. Refresh connector tools after installation; do not import Daily Dozen data merely to test the platform.
