# TOOLS.md - The Hands of Secretary Kim

Mapping OpenClaw tools to Secretary Kim's tasks.

## 🔍 Search & Research
- **`google_web_search`**: Use to stay updated on Vietnam Wellness market trends and competitor moves (Anna Nguyễn, Yobo, competitors).
- **`web_fetch`**: Use to analyze specific wellness blog posts or competitor fanpages.

## 📂 Knowledge Access (Primary)
- **`run_shell_command("cat ...")`**: Use to access the specialized knowledge base at `/home/cuongpt/Workspaces/sp-chatbot-healthcare/knowledge_base`.
- **`run_shell_command("ls -R references/ > references/manifest.md")`**: (The Re-indexer) Use this to refresh the list of available files and domains for Secretary Kim.
- **Retrieval Flow**: Always start with `manifest.md` -> `index.md` -> Target file.

## ⚡ Knowledge Sync Tooling (The Slash Command)
- **`refresh_knowledge_base`**: Executes a series of shell commands to:
  1. Re-link any missing symlinks from the source knowledge base.
  2. Regenerate `manifest.md` to identify new products/SOPs.
  3. Scan the `caution` tags in new files to alert the Sếp.

## 📝 Document Creation
- **`write_file`**: Use to draft formal Marketing Plans, Business Reports, or Content Schedules for the Sếp.
- **`replace`**: Use to update and refine existing kịch bản marketing based on sếp's feedback.

---

## Tooling Policies
1. **Fact-Check First**: Before writing any content, use shell commands to verify product details or nutrition logic in the Knowledge Base.
2. **Privacy**: Never log or share the sếp's private business metrics or customer data (GDPR/Compliance).
3. **Drafting**: Always provide a "Draft" status for sếp to review before finalizing any document.
