<frontmatter>
  title: "Working with AI Agents"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Before reading anything — which of these situations is the clearest example of an AI agent rather than a normal chatbot?
">
  <q-option reason="This is standard chatbot behaviour. The system is generating a reply to your prompt, but it is not planning steps, using tools, or taking actions in the world on your behalf.
">You ask an AI to explain a concept, and it replies with a paragraph of text</q-option>
  <q-option reason="This is still a prompt-response interaction. The AI is generating options, which can be useful, but it is not autonomously carrying out a multi-step task or doing anything beyond producing text.
">You ask an AI to draft three possible essay titles for you to choose from</q-option>
  <q-option correct reason="Correct. This involves the three features that make agents different: the system must plan several steps, use tools such as web browsing, and act with some autonomy instead of waiting for a fresh prompt at each stage.
">You give an AI the goal of finding three train options, comparing prices, and emailing you the best one after checking the booking sites</q-option>
  <q-option reason="Summarising text can be helpful, but it is still a single-response task. The system is not deciding what to do next, using outside tools, or taking actions beyond generating an answer.
">You paste your lecture notes into an AI and ask it to summarise them in simpler language</q-option>
</question>


<question type="text" header="Before reading this unit — how confident are you that you understand the difference between an AI chatbot and an AI agent?" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>

</quiz>

<p>[dry run — no content generated]</p>

<box type="tip" header="#### Reflection :fas-lightbulb:">

When delegating to an AI agent, what checkpoint would you add to catch silent failure before final submission or action?

</box>

<pic src="images/working-with-ai-agents-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="According to the unit, which three properties distinguish an AI agent from a standard chatbot?">
  <q-option correct reason="Correct. These are the three defining properties the unit names: planning (breaking a goal into steps), tool use (search, code, APIs, files), and autonomy (acting across steps without waiting for human input at each one). A chatbot does none of these — it produces a response and stops.">It can plan steps, use tools, and act autonomously across a sequence of actions</q-option>
  <q-option reason="Speed, accuracy, and internet access are not the defining properties of an agent. A standard chatbot can be fast and connected to the web; an agent is defined by its ability to plan, use tools purposefully, and execute a sequence of actions toward a goal — not by how quickly it responds.">It is faster, more accurate, and connected to the internet by default</q-option>
  <q-option reason="Persistent memory and self-improvement are separate capabilities that some systems may have, but they are not what makes something an agent. An agent is defined by its ability to pursue a multi-step goal using tools and autonomous action — not by whether it remembers you from last week.">It stores memory between conversations, learns from your preferences, and improves over time</q-option>
  <q-option reason="Model size, training data, and output length have nothing to do with whether a system is an agent. A small model with a planning loop and tool access is an agent; a large model that simply responds to prompts is not. The distinction is architectural, not about scale.">It uses a larger language model, has access to more training data, and produces longer responses</q-option>
</question>


<question type="mcq" header="The unit warns that agents make mistakes that &#x27;compound across steps&#x27;. What does this mean?">
  <q-option reason="Steps in an agent task are not independent — they build on each other. The agent uses the output of each step as the input for the next. If a step produces a wrong result, the agent proceeds as if that result were correct, and the downstream steps inherit the error. Independence would actually make agents much safer; the problem is that they are interdependent.">Each step in a task is independent, so an error in one step does not affect the others</q-option>
  <q-option correct reason="Correct. Unlike a single prompt-response interaction where an error is contained, an agent&#x27;s steps are chained. A wrong assumption made in step two becomes the premise for step three, which builds on it for step four. By the time the agent completes the task, a small early error can produce a result that is badly wrong — and without a human checking each step, the problem may not be noticed until the end.">An error in an early step can feed into later steps, making the final outcome significantly wrong</q-option>
  <q-option reason="Current AI agents do not reliably detect or correct their own errors mid-task. They lack the kind of self-monitoring that would catch a wrong assumption and backtrack. This is precisely why compounding is a risk: the system does not flag that it has gone off track, so mistakes accumulate unnoticed until the task is complete — or until something goes visibly wrong.">Agents detect errors automatically and correct themselves before completing the task</q-option>
  <q-option reason="Errors can occur at any stage of an agent task — including during text generation, planning, and reasoning — not only when tools are involved. Tool-use does create specific failure modes (wrong search queries, misread results), but the compounding problem is about chained steps generally, regardless of whether those steps involve tools or pure text generation.">Mistakes only occur when an agent uses external tools, not when it generates text</q-option>
</question>


<question type="mcq" header="The unit names a concrete risk of using AI agents. Which of these is the example it gives?">
  <q-option reason="This describes a cautious, human-in-the-loop design — the opposite of the risk scenario. The risk the unit names comes from agents that act autonomously without prompting you to review each step, not from agents that ask too often. Requiring approval at every step would reduce autonomy and reduce the compounding-error risk, at the cost of some efficiency.">An agent that refuses to complete a task unless you approve every individual step</q-option>
  <q-option correct reason="Correct. The unit names exactly this kind of scenario: an agent taking a consequential real-world action — sending a message, making a transaction — before the user has reviewed what it is about to do. This is not a hypothetical edge case; it is a routine risk whenever you grant an agent access to email, calendars, or payment systems. The action may have been reasonable from the agent&#x27;s perspective and still be something you would have stopped if you had seen it first.">An agent that sends an email you did not review, or makes a purchase you did not authorise</q-option>
  <q-option reason="Speed is not the risk the unit names. Agents are typically slower than chatbots because they execute multiple steps, but latency is a usability issue, not a safety one. The risks the unit focuses on are about autonomy: actions taken in the world without adequate human oversight, and errors that compound across steps before anyone notices.">An agent that generates text more slowly than a standard chatbot</q-option>
  <q-option reason="Output length is a quality issue, not an agent-specific risk. The risks that agents introduce — compounding errors, unintended actions, diminished oversight — all follow from their ability to act autonomously across multiple steps. Producing a short response is something any chatbot might do and carries none of those consequences.">An agent that produces slightly shorter responses than you asked for</q-option>
</question>


<question type="mcq" header="The unit describes the &#x27;trust calibration problem&#x27; as currently unsolved. What does it mean to say it is unsolved?">
  <q-option reason="The unit does not take this position. It acknowledges genuine useful applications of agents alongside real limitations — the point is not that agents should be avoided, but that deciding how much autonomy to grant them requires judgment that neither you nor the field has fully worked out yet. Avoiding them entirely is one choice, but it misses the nuance the unit is trying to build.">Agents are too unreliable to be useful, so the only sensible choice is to avoid them entirely</q-option>
  <q-option reason="The unit explicitly says this is unsolved &#x27;not just technically but personally and socially&#x27;. It does not frame the trust calibration problem as a temporary engineering gap that will close soon. Even if agents become more reliable, questions about how much autonomy to grant a capable-but-not-infallible system remain — those are human and institutional questions, not purely technical ones.">There is a technical fix being developed that will make agents fully reliable, after which the problem disappears</q-option>
  <q-option correct reason="Correct. The unit closes on this point deliberately: there is no universal formula for how much to trust an agent. The right level of autonomy depends on the task, the stakes if something goes wrong, how reversible the actions are, and your own risk tolerance. This is a judgment skill — and one that students entering a world full of agent-powered tools will need to develop through practice and reflection, not just by reading about it.">How much autonomy to grant an agent is a judgment call each person must make, and the right answer depends on context, stakes, and risk tolerance</q-option>
  <q-option reason="The unit does not draw this line. While it is true that lower-stakes, reversible tasks are generally safer to delegate to an agent, the unit frames trust calibration as a general challenge — not a solved problem in one domain and an impossible one in another. Complexity is one relevant factor, but so is reversibility, oversight availability, and the consequences of specific failure modes.">Trust calibration is a solved problem for simple tasks but impossible for complex ones</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Choose a multi-step task from your own life — something that genuinely involves several stages, not just a single question. Give an AI tool the goal as a single instruction and let it attempt to plan or execute the steps without you guiding each one. Observe closely: what does it do first? Where does it ask for help? Where does it act without checking? Where does it go wrong?

**Capture:**

- tool_used
- goal_you_set
- steps_the_ai_attempted
- where_it_needed_human_input
- one_action_it_took_that_surprised_you

**Reflect:** Compare what happened to the unit's account of agents. Did the system plan? Did it use any tools? How autonomous was it really? Did you find yourself wanting to intervene — and if so, at what point? What would you need to know or control before you trusted this system to complete the task without you watching?

<box type="info">Most general-purpose AI tools are not full agents, so students may observe a hybrid: some planning, minimal autonomous action. That gap between what an agent could do and what the tool actually did is itself useful data.</box>

</panel>


<question type="text" header="Now that you have read the unit — how confident are you that you could explain the difference between an AI agent and a chatbot, and name one genuine risk of using agents?" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>

</quiz>
