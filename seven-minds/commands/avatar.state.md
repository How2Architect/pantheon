---
name: seven-minds:avatar.state
description: This command will kick off the agentic system 7 minds
argument-hint: "Brain fart"
---

Load the information about the 7-minds agentic system which helps you do research on. 


## Steps to be followed for Initial reseach

1. Load the Agentic system and its purpose from `.claude/agents/seven-minds/README.md`
    - When invoking an agent, you will tell them to report updates on TODOs
2. Prepare a directory in the `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}`
3. Generate a staus file that will record the phaseof the idea grooming
    - File: `Inception/Organizing Ideas/{yyyy-mm-dd}/{Idea name}/status.md`
4. Phases
    - Air Benfing
    - Water Bending
    - Earth Bending
    - AVatar Mastery
5. You will work on ONLY 1 PHASE at a time
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



## Phase: 🪨 Earth Bending

### Steps


## Phase: 🔮 Avatar Mastery

### Steps
