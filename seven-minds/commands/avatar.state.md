---
name: seven-minds:avatar.state
description: This command will kick off the agentic system 7 minds
argument-hint: Brain fart or Help me or Scribe
---

Load the information about the 7-minds agentic system which helps you do research on. 


## Steps to be followed for Initial reseach

1. Load the Agentic system and its purpose from `.claude/agents/seven-minds/README.md`
    - When invoking an agent, you will tell them to report updates on TODOs
2. Prepare a directory in the `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}`
3. Generate or read staus file that will record the phaseof the idea grooming
    - File: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/status.md`
4. Phases
    - Air Benfing
    - Water Bending
    - Earth Bending
    - AVatar Mastery
5. You will work on ONLY 1 PHASE at a time
    - Check in the status file which phase is complete and which is the next phase to work on
6. You will ask the Agents to report their TODOs crisply in 1-liners


## Phase: 🌬️ Air Bending

### Steps
1. Read the idea from $1
2. Store the outputs from the agents in fils at the location: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/workings/`
2. Invoke the following in parallel:
    2.1 Invoke the `avatar` to do **Semantic Graph Creation ONLY** ONLY
        - The output file: `avatar-idea-breakdown.md`
    2.2 Invoke the `Sage` to find relevant infromation from the Vault for $1
        - Folders to search are 
            - `z - Others/Sources/Readwise/Articles`
            - `Inception\Frames`
            - `Extraction\Signals`
        - The output file: `sage-vault-search.md`
    2.3 Invoke the `Scout` to find information from the web for $1
        - The output file: `scout-web-search.md`
3. Once done, update the status
    - File: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/status.md`



## Phase: 💧 Water Bending

### Steps
1. You will search the `Inception/Organizing Ideas/` for folders and `status.md` files
2. Check which if the ideas where Air Bending phase is complete and Water Bending is not started
3. Show all the ideas to the user, and ask the user to select which idea to start with
4. Once you have selected the idea, you will read the files in the `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/workings/` folder
5. Call the `Seer` agent to do its thing
    - The output file: `seer-signals.md`
6. Once done, update the status
    - File: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/status.md`


## Phase: 🪨 Earth Bending

### Steps
**Check if $1 is "help me"**
1. You will search the `Inception/Organizing Ideas/` for folders and `status.md` files
2. Check which if the ideas where Air Bending phase and Water bending phase are complete. and Earth bending is not started
3. Show all the ideas to the user, and ask the user to select which idea to start with
4. Once you have selected the idea, you will read the files in the `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/workings/` folder
5. Load the file: `seer-signals.md` and find the signals that have category `Elaborate`
```
    **Signal 7**: Scale vs. Intimacy Trade-offs
    *Category: Conflicts*, Elaborate
    Sources reveal fundamental tensions between enterprise scale requirements and intimate vibe-coding experiences. Avatar breakdown emphasizes individual flow states, but web intelligence shows enterprise platforms focusing on standardization and control rather than personalized developer experiences.
```
```
    **Signal 14**: Organizational DNA Coding
    *Category: Outlandish Ideas*, Elaborate
    Imagine AI systems that don't just learn company patterns but encode organizational culture directly into development environments. Every code completion would reflect not just technical patterns but cultural values, decision-making styles, and unwritten rules, creating code that inherently embodies company personality and strategic direction.
    than personalized developer experiences.
```
6. For each of these signals, invoke `shadow.realm` agent to do its thing
    - You can invoke all the agents in parallel
7. update the `seer-signals.md` with new insights. You can add upto 500 words.
8. Move all the other ideas in the very end of the file. We do not want to lose them, but mark them `Less-important`
9. Update the status to "Ready for Scribing"
    - File: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/status.md`

**Check if $1 is "scribe", do the following**


## Phase: 🔮 Avatar Mastery

### Steps
