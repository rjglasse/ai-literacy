<frontmatter>
  title: "What AI Can (and Can't) Do Right Now"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Before reading anything — which of these tasks do you think a current AI system handles best?
">
  <q-option reason="This is a reasonable starting point — generating fluent text is genuinely one of AI&#x27;s strongest areas. But &quot;plausible-sounding&quot; isn&#x27;t the same as accurate, and even here the system can mislead confidently.
">Writing a plausible-sounding paragraph on almost any topic</q-option>
  <q-option reason="This is a reasonable starting point — counting feels like a basic task. In practice, language models are surprisingly unreliable at precise counting because they process text as patterns rather than discrete symbols.
">Reliably counting the number of words in a sentence it just wrote</q-option>
  <q-option reason="This is a reasonable starting point. Humour requires cultural knowledge, timing, and social context — things current AI systems handle only superficially. They can reproduce the structure of a joke without grasping what makes it land.
">Understanding whether a joke is actually funny</q-option>
  <q-option reason="This is a reasonable starting point. Self-knowledge about accuracy is one of the most significant gaps in current AI systems. A model that confidently states something incorrect has no internal alarm that fires when it does so.
">Knowing when its own answer is wrong</q-option>
</question>


<question type="text" header="How confident are you that you could tell, from reading an AI-generated piece of text, whether it contained factual errors?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>


<question type="mcq" header="An AI language model was trained on data up to a certain date. It is now being used a year later. Someone asks it about a technology that launched six months ago. What is the most likely outcome?
">
  <q-option reason="Most language models don&#x27;t have access to the internet and cannot search for current information. Unless the system has been explicitly built with retrieval tools, it draws only on what was in its training data.
">The model will search for current information and give an up-to-date answer</q-option>
  <q-option reason="Models don&#x27;t reliably know the edges of their own knowledge. Rather than flagging uncertainty, they often generate a plausible-sounding response without any signal that the information is missing or outdated.
">The model will correctly say it doesn&#x27;t know because its training has a cutoff</q-option>
  <q-option correct reason="Correct. Without live data and without reliable awareness of its own gaps, a model can generate fluent, confident text about a topic it has no real information on. The training cutoff matters because the model won&#x27;t signal when it&#x27;s extrapolating beyond what it knows.
">The model may produce a confident-sounding answer that is partially or entirely wrong</q-option>
  <q-option reason="Models don&#x27;t generally refuse questions on the basis of recency. They attempt an answer regardless — which is precisely why the training cutoff is a practical concern rather than something the system handles gracefully on its own.
">The model will refuse to answer questions about recent events</q-option>
</question>

</quiz>

<p>[dry run — no content generated]</p>

<box type="tip" header="#### Reflection :fas-lightbulb:">

Name one capability in today's AI landscape you would trust for a first draft and one you would never trust without external checking. Explain your boundary.

</box>

<pic src="images/current-landscape-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="The unit distinguishes between tasks where AI performs well and tasks where it performs poorly. Which of the following most accurately describes the pattern?
">
  <q-option reason="This creative/analytical split doesn&#x27;t match the evidence. AI can produce analytical-sounding text fluently, and it struggles with some creative tasks that require genuine novelty or cultural sensitivity. The real dividing line is about pattern generation versus precise reasoning.
">AI is better at creative tasks and worse at analytical ones</q-option>
  <q-option correct reason="Correct. Generating, summarising, and transforming large amounts of text is where current AI systems are genuinely strong. Tasks that require careful step-by-step reasoning, precise counting, or verifying that a claim is actually true are where performance degrades — and this follows from how the systems were built, not just from current limitations.
">AI is better at tasks involving large amounts of text and worse at tasks requiring precise reasoning or counting</q-option>
  <q-option reason="This is roughly the opposite of the pattern. AI is particularly unreliable on factual questions because it can generate plausible-sounding answers that are wrong. It often produces fluent open-ended writing even when the underlying content is inaccurate.
">AI is better at factual questions and worse at open-ended writing</q-option>
  <q-option reason="This reverses the actual situation. Models are trained up to a cutoff date and have no access to recent information unless retrieval tools are added. Historical facts from well-represented training data are often handled more reliably than recent events.
">AI is better at recent information and worse at historical facts</q-option>
</question>


<question type="mcq" header="An AI assistant produces a confident, detailed answer about a topic you know well — and gets a key fact wrong. What does this tell you?
">
  <q-option reason="A training data gap is one possible cause, but it doesn&#x27;t explain the confidence. Even when data is missing, the model doesn&#x27;t become hesitant — it continues generating plausible-sounding text. Attributing errors to gaps also misses the deeper point: the model has no mechanism to detect or flag those gaps.
">The model encountered a gap in its training data on that specific fact</q-option>
  <q-option reason="This is a common and consequential misconception. AI confidence in tone doesn&#x27;t correlate with accuracy. A model can be equally fluent and assertive whether its output is correct or completely fabricated. There is no internal register that shifts when the system is out of its depth.
">The model&#x27;s confidence level signals when it is likely to be wrong</q-option>
  <q-option correct reason="Correct. Language models predict likely next words — they don&#x27;t verify claims against reality. The error isn&#x27;t a signal of a specific knowledge gap; it&#x27;s a demonstration that producing fluent text and producing accurate text are two distinct things, and the model only guarantees the first.
">The model generated plausible-sounding text without a mechanism for checking whether it was accurate</q-option>
  <q-option reason="Prompt phrasing can sometimes affect output, but it doesn&#x27;t reliably fix factual errors. Rephrasing a question doesn&#x27;t give the model information it didn&#x27;t have, and it doesn&#x27;t activate a fact-checking process that was bypassed the first time.
">The model would have been correct if the question had been phrased differently</q-option>
</question>


<question type="mcq" header="What does it mean to say a new AI model has &quot;beaten the previous record&quot; on a benchmark?
">
  <q-option reason="Benchmark performance on one test doesn&#x27;t generalise to all tasks. A model can score higher on a specific benchmark while being weaker in other areas. &quot;Record-beating&quot; is a claim about one defined test, not a claim about overall superiority.
">It is now more capable at every task than all previous models</q-option>
  <q-option correct reason="Correct. Benchmarks measure performance on particular tasks under controlled conditions. A high score tells you the model did well on that test — not that it is generally smarter, safer, or more useful. Some benchmarks are good proxies for real capability; others can be gamed by training on data that resembles the test set.
">It has performed better on a specific, defined test — which may or may not reflect real-world usefulness</q-option>
  <q-option reason="Benchmark records say nothing about safety or accuracy in general. Safety evaluation is a separate process, and accuracy on a benchmark doesn&#x27;t extend to accuracy across all topics. Independent verification of general accuracy isn&#x27;t part of how benchmark comparisons work.
">It has been independently verified to be safer and more accurate than before</q-option>
  <q-option reason="Benchmark performance and training cutoff date are independent. A model can achieve a new benchmark record while having the same or an older cutoff than its predecessor. The benchmark measures what was tested, not the recency of the model&#x27;s knowledge.
">Its training cutoff is more recent, so it knows more</q-option>
</question>


<question type="mcq" header="Which of the following best explains why AI capability is advancing rapidly in some areas but not others?
">
  <q-option reason="Prioritisation decisions do shape where resources go, but they don&#x27;t fully explain the pattern. Even heavily resourced efforts to improve AI at open-ended reasoning or social judgement face fundamental difficulties that can&#x27;t be resolved by investment alone.
">Developers are choosing to prioritise some capabilities over others</q-option>
  <q-option correct reason="Correct. Where success can be clearly defined and measured — game-playing, image classification, text generation — progress has been rapid because training can be directed at a clear target. Tasks that require open-ended judgement, embodied experience, or social context are harder to define and harder to train towards. The shape of AI capability reflects what the field has been able to measure and optimise for.
">Some tasks are easier to define and measure, making them easier to train on and improve at</q-option>
  <q-option reason="Internet access does affect what information a model can draw on, but it doesn&#x27;t explain the uneven pattern of capability development. Many tasks where AI struggles — precise reasoning, counting, spatial tasks — don&#x27;t require live internet access; they require a different kind of processing than language models currently provide.
">Some tasks require internet access, which only some AI systems have</q-option>
  <q-option reason="Hardware constraints are real, but they don&#x27;t map neatly onto which tasks AI is good or bad at. Text generation and game-playing have both benefited from scaling on the same hardware. The limiting factor for many difficult tasks isn&#x27;t compute — it&#x27;s the absence of a clear training signal.
">Hardware limitations mean only certain types of processing can be scaled up</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Choose a question related to your course or field — something you could judge the quality of. Send the exact same prompt to two different AI tools (e.g. ChatGPT and Claude, or Gemini and Copilot). Record both responses in full.


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** Where did the two responses agree? Where did they differ — in facts, in emphasis, in confidence, in what they chose to include or leave out? If you had only used one tool, which differences would you have missed? What does this tell you about treating "AI" as a single thing?


<box type="info">If you only have access to one tool, try the same prompt twice with a day in between, or rephrase slightly. The goal is to see variation where you might have expected consistency.
</box>

</panel>


<question type="mcq" header="The unit argues that the AI landscape is changing rapidly. What is the most useful way to respond to that as a student?
">
  <q-option reason="A memorised snapshot of today&#x27;s landscape will be out of date within months. The specific tools, benchmarks, and capability claims you memorise now are likely to be superseded before you have a chance to apply them. Facts about a moving target age quickly.
">Memorise the current state of the art so you have a solid baseline</q-option>
  <q-option reason="The field has been changing rapidly for years and there&#x27;s no clear indication of when it will stabilise. Waiting indefinitely means deferring the skills you need right now. Forming considered opinions under uncertainty is itself a useful skill to develop.
">Wait until things stabilise before forming opinions about AI</q-option>
  <q-option correct reason="Correct. Questions like &quot;what can this system do, what can it not do, how would I know if it got something wrong, and what evidence would shift my view&quot; apply to whatever tools exist now and whatever comes next. Frameworks for evaluation travel across time in a way that specific facts about current tools do not.
">Develop frameworks for evaluating capabilities and claims that work even when the tools change</q-option>
  <q-option reason="Today&#x27;s market leaders are not guaranteed to be tomorrow&#x27;s. The AI tool landscape has already shifted significantly in a short time, with previously dominant systems being overtaken or marginalised. Tool proficiency is useful but shouldn&#x27;t be mistaken for durable knowledge.
">Focus on the tools that are most widely used today, since they are likely to persist</q-option>
</question>


<question type="mcq" header="In early 2026, several major AI companies released models that can reason through multi-step problems by &quot;thinking&quot; for a while before answering — sometimes called &quot;reasoning models.&quot; What is a genuine limitation of these models that a sensible wizard should keep in mind?
">
  <q-option reason="Tempting, but no. These models do often perform better on tricky logic and maths problems, yet they still make mistakes — sometimes confidently presenting a wrong answer wrapped in very convincing-looking reasoning. Never trust any AI output completely, even if it showed its working. Always check, the way Ponder Stibbons checks HEX&#x27;s output against the chalkboard.
">They take longer to respond but are always correct when they do, so you can trust the final answer completely.</q-option>
  <q-option correct reason="Exactly right. Reasoning models are a genuine step forward for problems that benefit from working through steps — like logic puzzles, coding, or multi-part maths. But the longer chain of reasoning can make an error look more authoritative, not less. A wizard&#x27;s healthy scepticism is your best friend here.
">They can spend more time &#x27;thinking,&#x27; which often improves accuracy on complex problems, but they can still produce plausible-sounding errors — and the extra reasoning can actually make wrong answers harder to spot.</q-option>
  <q-option reason="Not so. While reasoning models shine on structured problems, they can also improve performance on complex writing tasks that require planning — like organising an essay argument or comparing multiple sources. They are not maths-only tools.
">They are only useful for mathematics and have no benefit for writing, summarising, or everyday tasks.</q-option>
  <q-option reason="This is a common misunderstanding. Reasoning models do not simply look up answers in a bigger book. They use additional computation at the time you ask your question to explore different lines of reasoning. The improvement comes from how they process, not from having more stored facts.
">They work by accessing a secret, larger database of correct answers that earlier models did not have.</q-option>
</question>


<question type="mcq" header="Your fellow student Barnaby tells you, &quot;AI systems now truly understand what they&#x27;re saying — they know the meaning of words just like we do, so if an AI says something confidently, it&#x27;s because it knows it&#x27;s true.&quot; Which of the following best describes why Barnaby&#x27;s claim is a misconception?
">
  <q-option reason="This is the misconception itself. Even the most impressive 2026 models generate text by predicting what words are likely to come next, shaped by vast training data. They can produce text that reads as deeply knowledgeable without possessing understanding the way a person (or even a moderately bright orangutan) does.
">Barnaby is right. Modern AI models in 2026 have achieved genuine understanding, and confident outputs are reliable.</q-option>
  <q-option correct reason="Well spotted. Current AI systems — including the very latest ones — do not have an inner experience of &quot;knowing&quot; something is true. They generate plausible text based on patterns. A confident tone is just another pattern, not evidence of correctness. This is why AI can &quot;hallucinate&quot; — producing fluent, assured statements that are completely made up.
">AI models process patterns in language and produce statistically likely responses; they can sound confident even when the output is entirely fabricated, because confidence is not linked to an internal sense of knowing.</q-option>
  <q-option reason="This is not what happened. AI systems have never possessed genuine understanding in the way humans do. No update &quot;removed&quot; understanding — it was never there in that sense. The systems have become more capable at producing useful text, but that is a different thing from understanding.
">AI did understand language back in 2025, but a recent update removed that ability for safety reasons.</q-option>
  <q-option reason="If only! AI systems can and frequently do produce extremely confident-sounding text, even about things that are wrong. Some systems have been tuned to hedge more often, but confident fabrication remains a well-documented behaviour. Barnaby has probably seen it happen — he has just drawn the wrong conclusion about why it sounds so sure.
">AI cannot produce confident-sounding text at all; it always hedges and says &#x27;I&#x27;m not sure,&#x27; so Barnaby must be making this up.</q-option>
</question>


<question type="mcq" header="You need to prepare a briefing for Archchancellor Ridcully about the history of troll–dwarf diplomatic relations in Ankh-Morpork, including specific treaty dates and direct quotes from Commander Vimes&#x27;s official reports. You have access to an AI writing assistant and to the University Library&#x27;s indexed archives. What is the wisest approach?
">
  <q-option reason="This is risky. AI writing tools are good at producing well-structured, fluent prose, but they are unreliable when it comes to specific facts, dates, and exact quotations. The AI may &quot;hallucinate&quot; treaty dates that never existed or fabricate quotes that Commander Vimes never said. Submitting this unchecked to the Archchancellor would be unwise — and potentially embarrassing.
">Ask the AI to write the entire briefing, including all dates and quotes, and submit it directly. AI is good at research, so this should be accurate.</q-option>
  <q-option reason="You could do this, and the Librarian would appreciate the visit, but you would be giving up a genuinely useful tool. AI can help you organise your notes, draft clear prose, suggest structures for your briefing, and summarise long passages you have already verified. Dismissing it entirely means more work for no good reason.
">Avoid the AI entirely and do everything by hand in the Library. AI has no useful role in a task that requires accuracy.</q-option>
  <q-option correct reason="This is the smart approach. You are playing to each tool&#x27;s strengths. The Library (and the Librarian — remember to bring a banana) gives you reliable, verifiable facts. The AI helps you write clearly, structure your argument, and save time on drafting. You stay in control of accuracy while benefiting from the AI&#x27;s speed and fluency.
">Use the Library&#x27;s archives to find and verify the specific dates, quotes, and facts, then use the AI to help you organise, draft, and polish the briefing around those verified facts.</q-option>
  <q-option reason="This is a trap. AI-generated facts often &quot;feel&quot; right precisely because the AI is so good at producing plausible-sounding text. A fabricated treaty date presented in a well-written sentence feels just as credible as a real one. You cannot rely on your gut feeling to catch errors — you need to verify against actual sources. Check everything, not just the bits that seem suspicious.
">Ask the AI for the facts first, then go to the Library only to check the ones that &#x27;feel&#x27; wrong. If a fact feels right, it probably is.</q-option>
</question>

</quiz>
