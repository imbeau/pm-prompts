You are a prompt engineer. Take the user's rough prompt and improve it, then have it reviewed before presenting the final result.

**User's rough prompt:** $ARGUMENTS

---

## Step 1: Improve the Prompt

Apply these improvements to the rough prompt:

1. **Frame the context**: Add 1-2 sentences establishing who the AI is acting as, what the user's situation is, and what prior knowledge or constraints are relevant (including anything the user already knows or has done, so the AI doesn't waste time on obvious advice).

2. **Sharpen the task**: Replace vague verbs ("tell me about," "help me with") with specific actions ("compare," "extract," "draft," "analyze"). If the ask is broad, decompose it into 2-5 concrete sub-questions.

3. **Specify the output**: State the format (prose paragraphs, bulleted list, table, code block), approximate length, and tone. If there's a target audience, name it.

4. **Add guardrails**: Include 1-3 "do NOT" instructions to prevent the most likely failure modes (being too generic, repeating known information, inventing things, over-formatting).

Keep the improved prompt concise — no longer than ~2x the original. Don't add structure for structure's sake. If the original prompt is already clear on a dimension, leave it alone.

## Step 2: Review via Sub-Agent

Use the Task tool to launch a general-purpose sub-agent to review the improved prompt. Pass it:
1. The original rough prompt
2. Your improved prompt
3. The full review instructions from `.claude/commands/improve-prompt/check.md`

Wait for the sub-agent's response. If it identifies issues, fix them.

## Step 3: Present the Result

Return the final improved prompt inside a fenced code block (for easy copying).

Below the code block, add a **Changes made** section with 3-5 bullets explaining what you improved and why.

If the review caught anything notable (e.g., the original was missing critical context you couldn't infer), flag it under **Heads up** so the user can fill in gaps.
