# Third Bridge Skills
 
## Using skills in Claude (desktop and web)
 
### Install
1. Package the skill you want to use as a ZIP:
   - Each skill is a folder containing `SKILL.md` and any supporting files.
   - For example, zip the `tb-investor-workflows/` directory into `tb-investor-workflows.zip`.
2. Open Claude Desktop or Claude in the browser.
3. Go to the Skills section (for example: Settings → Customize → Skills).
4. Click Add / Upload skill and select the ZIP file.
5. Enable the newly added skill.
 
### Use
- Start a new chat or continue an existing one.
- Describe your task in natural language using phrases covered by the skill’s description, for example:
  - “Run the TB investor workflows process to build a credit underwrite on this issuer.”
- You can also explicitly mention the skill name, for example:
  - “Use the tb-investor-workflows skill to structure this analysis.”
 
Claude will load the corresponding skill and follow the workflow defined in `SKILL.md`.
 
---
 
## Using skills in ChatGPT
 
### Install
1. Package the skill as a ZIP (for example `tb-investor-workflows.zip`).
2. Open ChatGPT (web or desktop).
3. Open the skills / tools management area in settings.
4. Upload the ZIP as a new skill.
5. Enable the skill.
 
### Use
- In a ChatGPT conversation, describe your task using the workflow’s language, for example:
  - “Using the TB investor workflows process, and the transcript excerpts I provide, produce an initial issuer underwrite.”
- If the UI exposes a skill picker or explicit invocation, select or call the skill by name.
 
ChatGPT will load the `SKILL.md` frontmatter and instructions from the uploaded skill and apply the workflow to your conversation.
