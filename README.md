# 🚀 Third Bridge AI Skills

This guide explains how to integrate Third Bridge (TB) proprietary workflows—such as credit underwriting, transcript analysis, and investor processes—into your AI assistants. We refer to these modular toolsets as **"Skills."**

---

## 📂 Step 1: Prepare Your Skill Package
Before installation, ensure you have the official Skill Package from the internal portal.

* **File Format:** A single `.zip` file (e.g., `tb-investor-workflows.zip`).
* **Contents:** Inside this ZIP is a core file named `SKILL.md` (the AI's "instruction manual") and supporting templates.
* **Important:** **Do not unzip the file.** Both Claude and ChatGPT 2026 are designed to process the ZIP package directly for better version control.

---

## 🤖 Step 2: Using Skills in Claude (Desktop & Web)
Claude is optimized for deep reasoning and complex investment logic.

### 1. Installation
1.  **Log in:** Open [claude.ai](https://claude.ai) or the Claude Desktop App.
2.  **Open Settings:** Click your profile icon in the bottom-left and select **Settings**.
3.  **Navigate to Skills:** On the left sidebar, click **Capabilities**, then select **Skills Library**.
4.  **Upload:** Click the **Add / Upload Skill** button and select your `tb-investor-workflows.zip`.
5.  **Enable:** Ensure the toggle switch for the new skill is set to **Active**.

### 2. How to Use
* **Natural Trigger:** Simply start a chat. Claude will detect the skill based on your request.
    * *Example: "Build a credit underwrite for this issuer using the TB investor workflow."*
* **Explicit Mention:** To ensure Claude uses the correct logic, mention the skill name.
    * *Example: "Apply the tb-investor-workflows skill to the transcript I just uploaded."*

---

## 💬 Step 3: Using Skills in ChatGPT (Desktop & Web)
ChatGPT offers two primary ways to use TB Skills: **Modular Skills** or a **Dedicated Custom GPT**.

### Option A: The "Skills" Feature (Recommended for Flexibility)
*Best for users who want to "summon" TB expertise within any conversation.*

1.  **Install:** Click your profile icon -> **Skills**.
2.  **Upload:** Click **Install New Skill** and upload the ZIP package.
3.  **Use:** * Type a **forward slash `/`** in the message box to see your active skills.
    * *Example: "Use /tb-underwrite to analyze this issuer's financial data."*

### Option B: Custom GPT (Recommended for a Dedicated Assistant)
*Best if you want a standalone "TB Investment Assistant" in your sidebar.*

1.  **Create:** Click **Explore GPTs** in the sidebar, then click **Create**.
2.  **Configure:** * **Instructions:** Open your `SKILL.md` file, copy all the text, and paste it into the "Instructions" box.
    * **Knowledge:** Click **Upload files** and upload any reference PDFs or templates from the ZIP.
3.  **Save:** Click **Create/Update** (Top right) and select "Only me" or "Anyone with a link."
4.  **Use:** Click your "TB Assistant" in the sidebar whenever you need to start a focused task.

---

## 💡 Pro Tips for Better Results

1.  **Reference Attachments:** If you upload a PDF transcript, be specific: *"Use the **TB Skill** to extract key risks from the **attached document**."*
2.  **Updates:** When Third Bridge releases a new version of a skill, simply repeat the upload process to overwrite the old version.
3.  **Multi-Skill Mode:** In 2026, you can use multiple skills at once. For example, you can call a "Financial Analysis Skill" and a "Compliance Skill" in the same chat for a dual-check.

---

## ❓ FAQ

* **Q: Why is the AI not recognizing my Skill?**
    * A: Ensure the `SKILL.md` file is present at the root of your ZIP folder. If you renamed the file, the AI might fail to index it.
* **Q: Can I use this on my phone?**
    * A: Yes! Once you install a Skill on your desktop, it syncs to your account and is available on the Claude or ChatGPT mobile apps.
