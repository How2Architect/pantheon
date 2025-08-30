---
name: seven-minds:avatar.state
description: This command will kick off the agentic system 7 minds
argument-hint: Brain fart
---

Load the information about the 7-minds agentic system which helps you do research on. 


Steps
1. Load the Agentic system and its purpose from `.claude/agents/seven-minds/README.md`
    - When invoking an agent, you will tell them to report updates on TODOs
2. Prepare a directory in the `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}`
3. Read the idea from $1 and invoke the `avatar` for **Semantic Graph Creation ONLY**. Tell is to do this and this only
    - The output should be saved in `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/workings/avatar-idea-breakdown.md`