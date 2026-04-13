^ _link not tracked_ - [[project - Claude Code]] [[agent skill]] - `AskUserQuestion`

---

This is an example of _link not tracked_

```
Use a single `AskUserQuestion` call with three questions:

1. **Question**: "Bump the patch version before building?"
   - **Options**: "Yes (Recommended)" / "No, keep current version"

2. **Question**: "Which S3 bucket environment should the DMG be uploaded to?"
   - **Options**: "Production (Recommended)" (description: "Upload to meadow-prod-artifacts") / "Development" (description: "Upload to meadow-dev-artifacts for testing without impacting production releases")

3. **Question**: "Update the auto-update version after upload?"
   - **Options**: "Yes (Recommended)" (description: "Set auto-update-version.txt so existing installs will see this as an available update") / "No" (description: "Skip updating auto-update-version.txt — useful if you want to release without triggering auto-update prompts")
```


![[claude-asking-user-questions.png]]