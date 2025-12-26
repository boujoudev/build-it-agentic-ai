# 1. What is an Agentic AI ? Core principle VS Passive LLMs

## Definition of Agentic AI :
**An agentic AI** is an autonomous system equipped with a **goal**, **erception**, **action**, and **memory**. Unlike a simple reactive chatbot, it doesn't just       
  respond to a single query: it actively pursues an objective, observes its environment, plans, acts, reflects on its actions, and adapts

![Agentic AI Loop: Goal → Observe → Plan → Act → Reflect](https://labs.sogeti.com/wp-content/uploads/sites/2/2025/03/Agentic-AI.png)

## Contrast with Passive LLMs:

| Aspect                  | Passif LLM (e.g., classic ChatGPT)                  | Agentic AI (e.g., AutoGPT, BabyAG)                          |
|-------------------------|-----------------------------------------------------|-------------------------------------------------------------|
| **Operating Mode**      | Reactive: responds to a single user input           | Proactive: pursues a goal autonomously                      |
| **Perception**          | None (context limited to the conversation           | Observes the environment (tools, memory, world state)       |
| **Action**              | Generates text only                                 | Uses tools (web search, code, API, etc.)                    |
| **Memory**              | Short-term memory (session context)                 | Long-term memory + reflection (reasoning traces, summaries) |
| **Planning**            | None or very limited                                | Breaks down the goal into sub-tasks, prioritizes, iterates  |
| **Reflecion**           | No self-evaluation loop                             | Reflects on past actions to improve                         |


Agentic AI often follows an iterative loop inspired by human cognition and frameworks like ReAct (Reason + Act):


## Core Principles of Agentic AI :

Agentic AI often follows an iterative loop inspired by human cognition and frameworks like ReAct (Reason + Act):

1. **Observe/Perceive**: Gather information from the environment, user input, tools, or sensors.
2. **Plan/Reason**: Break down the goal into sub-tasks, evaluate options, and formulate a strategy.
3. **Act/Execute**: Perform actions, such as calling tools, interacting with systems, or generating outputs.
4. **Reflect/Evaluate**: Assess results, identify successes/failures, update memory, and adjust the plan.

Additional key components:

1. **Memory**: Short-term (current context) and long-term (stored knowledge/experiences) for continuity.
2. **Tool Use**: Integration with external resources (e.g., browsers, databases) to extend capabilities beyond text.

→ This cycle enables persistence, learning, and handling of complex, dynamic tasks.

![ReAct Framework Loop in Agentic AI](https://www.kdnuggets.com/wp-content/uploads/react-pattern.png)


## Example:

**Single Generation (Passive LLM)** vs**Autonomous Agent (Agentic AI)**

**Scenario**: “Prepare a trip to Tokyo for Easter vacation.”

**Classic ChatGPT**: Gives a complete response in one go (list of hotels, attractions, etc.), but doesn't check real availabilities and stops there.
**AutoGPT (agentic)**:
1. Searches for the exact dates of Easter 2026
2. Checks the weather in Tokyo during that period
3. Searches for available flights from your city
4. Compares hotel prices on multiple sites
5. Creates a day-by-day itinerary
6. Asks for confirmation at each step or adjusts if a flight is too expensive
→ All of this **without human intervention between steps**


## In Our Project : 

 **Interview Council** (job interview council):

-**Passive Version**: An LLM responds once to “Prepare me for an interview at Google”.

-**Agentic Version**: The agent

  - Asks questions to understand the position, your CV, your weaknesses
  - Researches typical questions for that role at Google
  - Simulates a full interview (plays the recruiter)
  - Gives detailed feedback
  - Proposes exercises to fill in the gaps
  - Plans follow-up sessions

 → It initiates a complete session, adapts to your responses, and guides you until you're ready.



```mermaid
graph TD
    A[User: CV + Target Job] --> B[Interviewer Agent]
    B --> C[User Answers Questions]
    C --> D[Multi-Evaluator Council]
    D --> E[Vote & Score]
    E --> F[Coach Agent: Feedback + Advice]
    F --> User
    F --> B










