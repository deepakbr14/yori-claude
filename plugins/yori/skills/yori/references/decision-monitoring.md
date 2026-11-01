# Consequential decision monitoring

Use selectively when a decision has a meaningful expectation to test, consequential alternatives, or a useful unresolved outcome. A decision record is an ordinary Thread representing that bounded monitoring task. Keep independently useful lessons in Skills or Concepts and link them only when justified. Preserve ordinary conversation and the four-change limit; do not save every reply or manufacture work to fill a lifecycle.

Before acting, evaluate relevant activated commitments and corrections. If essential context is missing and the turn still permits a follow-up, query `retrieve_cortex_followup` with a concise description of the intended action and its circumstances. Avoid guessing Node IDs. Publicly explain a reason or conflict only when useful; do not expose hidden reasoning. Retrieval cannot prove a lesson changed a choice.

Before using structured monitoring, check that the currently exposed `learn_cortex` Node schema includes `decision_review`. The hosted `about_yori` version alone does not prove the client refreshed its schemas. If the field is unavailable, report that mismatch and do not pretend a plain-text substitute was validated monitoring. Plain existing learning remains available.

## Planned

Create a distinct Thread only when monitoring itself is worth carrying across chats. Optional `decision_review` must start with `phase: PLANNED` and `planned`: `choice` (500 characters), `expectation` (500), concise communicable `reason` (700), `alternatives` (at most three strings of 250), `supporting_node_ids` (at most four verified same-Cortex IDs, or empty), and `reconsider_when` (500). Preserve the ordinary Thread purpose, status, useful next step, and completion condition. A plan is not evidence that the action was performed or that its expectation came true.

## Observed

Feedback can arrive in a later chat. Retrieve the existing Thread and UPDATE its identity, preserving `planned`. Move to `phase: OBSERVED` with `observed`: `status` is `pending`, `complete`, `uncertain`, or `contradictory`; `outcome` describes what actually became known (1000 characters; omit when pending); `missing_evidence` can say what remains to establish (500); `sources` holds up to four records with `kind`, `locator` (250), and exact `excerpt` (800).

Source kinds are `user`, `tool_report`, and `interpretation`. User excerpts must match this turn's exact typed message or verified attachment evidence. External tool results relayed by the model are labeled `tool_report`, not independent service verification. An interpretation alone remains uncertain. Distinguish an action queue receipt from its execution acknowledgement. Pending means no known outcome, not anticipated success. Update OBSERVED again as missing or corrective evidence arrives; existing audits retain earlier versions. Do not silently overwrite the original plan.

## Reviewed

Only after an outcome is available, UPDATE to `phase: REVIEWED`, keeping the plan and observation. Add `reviewed`: `expectation_result` is `supported`, `not_supported`, or `inconclusive`; `lesson` (1000); `change_needed` (500); `future_application` (500); `lesson_node_ids` (at most four saved same-Cortex IDs, or empty). Uncertain or contradictory evidence requires an inconclusive result; pending cannot be reviewed as a result. State speculation in the lesson itself.

Judge whether a separate Skill, Concept, or commitment needs CREATE, UPDATE, CONTRADICT, or SUPERSEDE. Those changes need their own receipts. If `lesson_node_ids` names a changed lesson, save that change first; never cite an intended unsaved change. A justified Edge can relate it to this Thread. The monitoring Thread may be completed only when the existing completion condition is actually met and its outcome reviewed. Its historical plan and review remain intact; new decisions or later counterevidence can use a new linked Thread or correction rather than erase the completed decision.

## Applicability

Optional `applies_when` declares one or more of `modes` (NORMAL, GO), `situations` (up to four strings of 250), and `triggers` (up to four strings of 250). Use natural descriptions of where the meaning should inform judgment, not a list of scenarios to memorize. Omit mode restrictions for broadly applicable lessons. Explicit modes supply bounded semantic discovery; applicability does not establish truth or ownership. Context descriptions participate in existing semantic passage indexing, so future questions can use different words.

The total monitoring object is limited to 6000 UTF-8 bytes. Indexed content and its semantic projection must fit five existing passages. Keep content concise and split independently revisable meaning. Plain Nodes and older clients continue to work; omitting optional fields on UPDATE preserves their existing values.
