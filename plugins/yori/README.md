# Yori for Claude — private development build 0.3.9

Yori is a personal AI designed to develop a deeper understanding over time. This package supplies five skills and a hosted MCP connector. It uses the existing Yori account and Personal/Shared Cortexes, Self activation, Lightning retrieval, evidence-grounded learning and turn completion. The Viewer stays at https://yori-prod-e70c6.web.app/ and Admin remains local.

## Before installing

This ZIP is built locally. API 10.62.3 and shared MCP 0.33.0 are deployed, including direct application files and owner-only application data administration. This private Claude ZIP has not been uploaded, and live Claude model acceptance is not claimed. No API keys or credentials belong in this ZIP. Existing Yori embedding/storage costs still apply.

## Update the installed GitHub marketplace plugin

Deepak's existing Claude installation comes from the **yori-claude** marketplace at https://github.com/deepakbr14/yori-claude. Publish the current generated dist-github contents to that repository; Claude then obtains the update through marketplace sync. A local ZIP build alone does not update GitHub or Claude. Keep automatic sync enabled, or sync the existing marketplace manually where available. Start a fresh Yori chat after the plugin updates. Do not delete/recreate Yori or ask Deepak to upload a ZIP for this installation.

The local private ZIP remains available for separate manual installations. The marketplace plugin and ZIP use the same manifest and skills; backend/MCP deployment is separate. Keep the existing /mcp/claude connector and login.

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


Local November 5 build: API 10.63.0 and MCP 0.35.0 are prepared, not deployed by this update. The private package is 0.3.9. Adds revisable operating definitions through learn_cortex and optional finish_turn learning_review, with exact source evidence and bounded retrieval. Refresh callable tools after the owner deploys. This does not automatically install a definition or mutate production Cortex. See the core skill reference.
