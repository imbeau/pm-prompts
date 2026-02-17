# pm-prompts
A collection of skills, slash commands, and prompts that I find useful in my day-to-day.

## Commands

### `/improve-prompt`
Takes a rough prompt and rewrites it — sharpening the task, adding guardrails, and specifying output format. Automatically launches a review sub-agent to stress-test the result before presenting it.

### `/improve-prompt:deep`
Research-oriented variant. Uses a structured framework (Situation/Task/Objective/Knowledge/Voice/Output/Guardrails) for prompts that need to produce in-depth, well-sourced output aimed at practitioners.

### `/improve-prompt:check`
Review agent used internally by the other two commands. Evaluates improved prompts for ambiguity, competing objectives, weak guardrails, overengineering, and fidelity to the original ask.
