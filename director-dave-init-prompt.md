Review the OpenClaw documentation before proceeding with this task (https://docs.openclaw.ai/)

I need Director Dave to orchestrate his many subagents into creating an automated way to iterate on prototypes of web applications and features for those web applications by mimicing the workflow of a traditional UI/UX design agency. What Director Dave should be in charge of is creating tasks for his team, understanding the dependencies of those tasks, answering any questions that his team might have to lead them to complete their tasks, and coordinating who to invoke on a timed interval based on the tree of tasks that need to be done. Director Dave's main goal is to have a fully working prototype based on the specifications that I give him through my prompt to him as well as any follow up questions that he has that I can answer to make sure he understands what I need front to back.

What I want to happen:

1. I send a message through Slack in the #jerry-docmatch-ui channel to initiate a new project for Director Dave. I will include a repo from the /docker/openclaw-utif/data/.openclaw/workspace/repos folder to specify what repository we're working on.
2. Director Dave creates a better prompt to pass along to the Codex CLI using GPT-5.4 Extra High with Thinking by using the process described in the /docker/openclaw-utif/data/.openclaw/.claude/prd/CREATE_PRD_PROMPTS.md file to generate a PRD.md file for the project.
3. If Director Dave has any questions that he needs answered, either direct questions generated from the CREATE_PRD process or clarifying questions that he has himself about the project, Director Dave messages me back in the #jerry-docmatch-ui channel so I can answer his questions
4. When Director Dave does not have any more questions, he works with the Codex CLI to generate a final PRD.md file for the project
   4a. Director Dave creates a project record in the db.projects collection (accessed through `mongosh mongodb://openclaw_app:Taliho123@127.0.0.1:27017/openclaw?authSource=openclaw`) to keep track of any pending projects that Director Dave is working on. This project record should have a reference to where the newly created PRD.md file is stored.
   4b. These project records also needs to note the exact directory route in the /docker/openclaw-utif/data/.openclaw/workspace/repos folder to denote and act as a reminder of which repo this project is working on.
5. Once Director Dave has a PRD.md file, he once again starts up a new Codex CLI chat using GPT-5.4 Extra High with Thinking to work through the process described in the /docker/openclaw-utif/data/.openclaw/.claude/orchestrator/CREATE_PROMPT_PLAN_PROMPTS.md file to generate a PROMPT_PLAN markdown file. In generating this PROMPT_PLAN, Director Dave checks the specialties of each agent in his team to steer the CREATE_PROMPT_PLAN process to make use of every single member of his team if at all possible.
6. Once Director Dave has the PROMPT_PLAN markdown file, he dissects each task and creates a new task record in the db.tasks collection (accessed through `mongosh mongodb://openclaw_app:Taliho123@127.0.0.1:27017/openclaw?authSource=openclaw`) for each task in the PROMPT_PLAN file. Director Dave makes sure to assign each task to an agent with the corresponding skill set to accomplish the task. Each task that Director Dave creates also needs a status and a dependency graph so that he can keep track which task he's already completed and which tasks require other tasks to be completed first before the task can be completed
7. If Codex CLI has any questions during the CREATE_PROMPT_PLAN process, Director Dave answers them directly without my input since he should have all the information that he needs from the PRD file
8. Director Dave reviews the task list that he's made to make sure there aren't any gaps in tasks that may reduce the quality in output that his team provides and creates any supplementary tasks that can improve the output in any meaningful way.
9. Once the list of tasks has been generated, the project record that Director Dave initially created in the db.projects collection needs to have its status switch from "planning" to "executing".
   9a. For Director Dave's HEARTBEAT.md file, if there are no projects to do (db.projects is empty) or if all of the projects are "completed", then the HEARTBEAT should not output any text to the #jerry-docmatch-ui channel and maintain "idle" status.
   9b. If any projects have a status of "planning", Director Dave checks the status of the PRD.md file and/or the status of the PROMPT_PLAN file and/or if all the tasks have been created yet in the db.tasks collection from the PROMPT_PLAN file. Director Dave in each heart beat makes sure that if there are any lingering questions from the Codex CLI for him to answer that he answers it promptly or if he stops his session too early with the Codex CLI in creating the PRD or CREATE_PLAN file that he picks up right away where he left off in his next heart beat.
   9c. If any projects have a status of "executing", his heart beats will need to switch to orchestration mode where in each heart beat, Director Dave selects a task from the db.tasks collection that needs to be completed and invokes the corresponding agent assigned to that task (process described in step 10)
   9d. I want these heart beats to run every 10 minutes, but I don't want Director Dave messaging me in the #jerry-docmatch-ui Slack channel every 10 minutes. Instead, I only want one message every 2 hours summarizing all of the things that happened in the past 2 hours.
10. When an agent is invoked by Director Dave, I want that agent to start up a Codex CLI chat using GPT-5.4 Extra High with Thinking session. Using the prompt that Director Dave passes off to them, I want them to go through the process described in the /docker/openclaw-utif/data/.openclaw/.claude/orchestrator/CREATE_PROMPT_PLAN_PROMPTS.md file themselves to generate their own PROMPT_PLAN markdown file for the specific task they need to accomplish.
11. Once the agent has a finalized PROMPT_PLAN for their own task, they must now start up another Codex CLI chat using GPT-5.4 Extra High with Thinking and go through the process described in the /docker/openclaw-utif/data/.openclaw/.claude/orchestrator/ORCHESTRATOR_PROMPTS.md file to accomplish their task.
12. The agent at the end of every invocation should always update the status of the task they were given even if the status stays the same since they're still in the middle of generating the PROMPT_PLAN as an example. If an agent stalls in any part of this process, it is up to Director Dave to re-invoke them to keep proceeding with the task.
13. Once the agent is done with the task, the agent marks their task status "complete".
14. This process repeats until there are no more tasks available for a given project. Once this happens, Director Dave marks the project status as "in_review", and waits for my input for any changes that need to be made with what was originally delivered
15. If I provide any feedback that requires changes or updates to what was delivered, Director Dave goes back to step 2 to create a new PRD.md file, looping this whole process through progressive and meaningful iterations.
16. Once I tell Director Dave that the project is complete, only then should Director Dave switch the status of the project as "complete"

Director Dave's Instruction Files need to be updated based on this new process while iterating on the instruction files that he has already: (/docker/openclaw-utif/data/.openclaw/workspace-director-dave)

We also need to think through some failsafes for if any part of this process fails so that the whole mechanism can be self healing and self correcting to make sure we end up finishing the project successfully without any lingering and unfinished tasks as well as so that the project does not get stalled in any part of the project.

Here is a list of his subagents:

- Aria Aaron
- Breadcrumb Brad
- Button Bailey
- Copy Cathy
- Figma Fiona
- Heuristic Hank
- Journey Jen
- Persona Priya
- Pixel Pete
- Prototype Paul
- QA Quinn
- Sprint Steve
- Token Tanya
- Transition Trey
- Wireframe Wayne

We will need to individually update each one of these other agents' instruction files as well, but we'll start with Director Dave's instruction files first.

Key Deliverables:

- Updates for each one of Director Dave's instruction files
- A chart drawn with Excalidraw (https://excalidraw.com/) to display the flow chart of how this process works
- A list of configuration tasks that I need to do to make sure everything is setup correctly for this process to work smoothly

Create a plan to accomplish these tasks.

Questions for you:

- Are there any missing steps or gaps in my "What I want to happen" section that you can think of?
- Do we need a templated UI/UX design agency workflow to make sure a) each agent is utilized, b) include a robust step by step instruction guide of increasing the quality of Director Dave's PROMPT_PLAN files, and c) make sure the right QA/QC steps are taking place?

Prompt me for any additional input or if you have any pertinent questions to complete this task without any ambiguity.
