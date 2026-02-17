# pm-prompts
A collection of skills, slash commands, and prompts that I find useful in my day-to-day.

## Getting Started

### [PM Copilot Instructions (Simple)](instructions/getting-started/pm-copilot-instructions-simple.md)
A starter prompt for using Claude or ChatGPT as a product management coach and advisor. Paste it into a custom instruction or system prompt and start chatting. This is the training-wheels version — a good foundation to build on as you get more comfortable with what these tools can do.

## Skills

### [The People's Post Generator](peoples-post-generator/)
An AI skill for writing social posts you're proud of. Feed it a messy idea — screen recording transcript, Slack thread, meeting notes, or a speech-to-text rant — and it walks you through focusing, drafting, and polishing a post. Works with ChatGPT, Claude, Cursor, and other LLMs. Originally created by [Tal Raviv](https://github.com/talsraviv/peoples-post-generator).

## Commands

### `/improve-prompt`
Takes a rough prompt and rewrites it — sharpening the task, adding guardrails, and specifying output format. Automatically launches a review sub-agent to stress-test the result before presenting it.

### `/improve-prompt:deep`
Research-oriented variant. Uses a structured framework (Situation/Task/Objective/Knowledge/Voice/Output/Guardrails) for prompts that need to produce in-depth, well-sourced output aimed at practitioners.

### `/improve-prompt:check`
Review agent used internally by the other two commands. Evaluates improved prompts for ambiguity, competing objectives, weak guardrails, overengineering, and fidelity to the original ask.
