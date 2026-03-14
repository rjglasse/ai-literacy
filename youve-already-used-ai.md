<frontmatter>
  title: "You've Already Used AI"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Before reading anything — which of these do you think counts as AI? Pick the one you&#x27;re most confident about.
">
  <q-option reason="This is a reasonable starting point — spam filters were among the earliest practical machine learning applications, and they do count as AI. If you hesitated here, it&#x27;s worth examining what you expected AI to look like.">A spam filter that moves junk email to a separate folder</q-option>
  <q-option reason="This is a reasonable starting point — keyboard autocomplete is a language model in miniature, predicting likely next words from your typing history and patterns across many users. It&#x27;s a useful example to hold onto as the unit develops.">The autocomplete suggestions on your phone&#x27;s keyboard</q-option>
  <q-option reason="This is a reasonable starting point — music recommendation systems are a classic application of machine learning, specifically collaborative filtering. If this felt more like AI than the others, it&#x27;s worth asking why.">A music app that recommends songs based on what you&#x27;ve played</q-option>
  <q-option reason="This is a reasonable starting point — and it&#x27;s actually the most accurate of the four options. All three examples are AI systems. If you picked this confidently, you&#x27;re ahead of where most people start.">All of the above</q-option>
</question>


<question type="text" header="How confident are you that you could explain the difference between AI and ordinary software to someone who&#x27;s never studied either?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>


<question type="mcq" header="A friend says: &quot;I&#x27;ve never really used AI — I don&#x27;t have any of those chatbot apps.&quot; What would you say?
">
  <q-option reason="This underestimates how embedded AI has become in everyday services. Even without a dedicated AI app, most people interact with AI systems dozens of times a day through email filtering, search ranking, social feeds, and keyboard suggestions.">They&#x27;re probably right — AI is still fairly niche</q-option>
  <q-option correct reason="Correct. AI is built into the infrastructure of services most people use constantly — search, email, social media, maps, streaming. You don&#x27;t need a dedicated AI app to be using AI many times a day.">They&#x27;re likely wrong — AI is in many apps they already use daily</q-option>
  <q-option reason="Smartphone ownership is not the determining factor. Many AI-powered services are web-based or present in non-smartphone contexts (smart speakers, email clients, search engines). And many basic smartphones already use AI for keyboard prediction and photo sorting.">It depends whether their phone is a smartphone</q-option>
  <q-option reason="The definition of &#x27;app&#x27; isn&#x27;t really the issue here. Whether the AI is delivered through an app, a website, or built into the operating system, the point is that AI is pervasive across many services your friend almost certainly uses — regardless of how we classify the delivery mechanism.">It depends on how you define &#x27;app&#x27;</q-option>
</question>

</quiz>

<p>[dry run — no content generated]</p>

<box type="tip" header="#### Reflection :fas-lightbulb:">

Which everyday AI feature now feels less "invisible" to you after this unit, and what assumption about it did you have to revise?

</box>

<pic src="images/youve-already-used-ai-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="What distinguishes &quot;narrow AI&quot; from the AI depicted in most science fiction?
">
  <q-option reason="Speed and accuracy are not the defining distinction. A narrow AI system can be extremely fast and highly accurate within its domain — a chess engine or a radiograph classifier may outperform any human. The difference is scope, not performance.">Narrow AI is slower and less accurate</q-option>
  <q-option correct reason="Correct. A spam filter cannot translate French; a translation system cannot recommend music. Each narrow AI system is built and trained for a single task and has no ability to transfer that competence elsewhere. Science fiction&#x27;s general AI — capable across many domains — does not currently exist.">Narrow AI is designed for one specific task and cannot generalise beyond it</q-option>
  <q-option reason="Narrow AI is not obsolete — it is still the dominant form of deployed AI today. Spam filters, recommendation engines, image classifiers, and fraud detectors are all narrow AI systems in active use. The distinction is conceptual, not historical.">Narrow AI is older technology that has mostly been replaced</q-option>
  <q-option reason="Hardware requirements have nothing to do with whether a system is &#x27;narrow&#x27;. Many narrow AI systems run on general-purpose hardware; the narrowness refers to the scope of the task the system was built to perform, not the physical infrastructure it runs on.">Narrow AI can only run on specialised hardware</q-option>
</question>


<question type="mcq" header="Early software used hand-written rules (e.g. &quot;if the email contains this word, mark it as spam&quot;). What changed with modern AI systems?
">
  <q-option reason="Better rules were tried, but they hit a ceiling. Real-world language is too varied and adversarial to capture with hand-written rules — spammers quickly learn to work around any fixed pattern. The shift to learning from data wasn&#x27;t an incremental improvement to rule-writing; it was a different approach entirely.">Programmers started writing better and more complete rules</q-option>
  <q-option correct reason="Correct. Instead of a programmer anticipating every case, the system is shown millions of examples and learns what patterns correlate with the right outcome. This works across a much wider range of situations than hand-coded rules, and it generalises to cases the programmer never explicitly considered.">Systems learned statistical patterns from large amounts of example data</q-option>
  <q-option reason="Checking every possibility (brute force) only works for problems with a bounded search space, like some games. For open-ended tasks like identifying spam or recognising speech, the space of possibilities is effectively infinite — no amount of computing power makes brute-force search feasible.">Computers became fast enough to check every possibility</q-option>
  <q-option reason="Crowdsourcing rules is not the same as learning from data. The shift to modern AI involved systems inferring patterns automatically from labelled examples — not collecting more rules from more people. The internet did provide vast amounts of training data, but the key change was the learning approach, not the sourcing of rules.">The internet made it easier to crowdsource the rules</q-option>
</question>


<question type="mcq" header="Why does the unit argue that your existing intuitions about AI are a &quot;starting point&quot;?
">
  <q-option reason="The unit doesn&#x27;t assume your intuitions are correct — some of them will hold up under examination, and some won&#x27;t. The point is that they&#x27;re worth examining, not that they need endorsing.">Because your intuitions are probably correct and just need confirming</q-option>
  <q-option correct reason="Correct. You&#x27;ve been interacting with AI systems for years, and that experience has produced real intuitions about when to trust a recommendation, when autocomplete goes wrong, when a result feels off. Those intuitions are data. The course invites you to examine them carefully, not discard them.">Because intuitions formed from years of real use are worth examining, even if some need revising</q-option>
  <q-option reason="The opposite is closer to true: the course assumes you have prior experience with AI systems and treats that experience as a genuine starting point. Students who have been using search, autocomplete, and recommendations for years are not beginners — they&#x27;re experienced users whose intuitions are worth interrogating.">Because this course is designed for complete beginners with no prior experience</q-option>
  <q-option reason="AI systems are not designed to match intuitions — they&#x27;re optimised for metrics like engagement, accuracy, or fluency. Sometimes their outputs align with intuition; sometimes they diverge sharply. One goal of the course is to help you notice when your intuitions about AI outputs are well-founded and when they might lead you astray.">Because AI systems are designed to match human intuitions</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Pick a task you actually do — writing an email, summarising a reading, planning a revision schedule, explaining a concept to a friend. Open any AI tool (ChatGPT, Claude, Gemini, Copilot, or another) and ask it to do that task for you. Record exactly what you asked and what it produced.


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** How did the AI's output compare to what you would have produced yourself? Was there anything it got right that surprised you? Anything it got wrong or missed that you wouldn't have? What does this tell you about where this tool fits — and doesn't fit — in your own workflow?


<box type="info">Choose something genuinely from your life, not a test prompt. The point is to see how AI handles a task where you already know what good looks like.
</box>

</panel>


<question type="mcq" header="Which of the following best describes how a music recommendation system works?
">
  <q-option reason="This describes a content-based filtering approach, which some systems use partially, but it is not how most major recommendation systems primarily work. The dominant approach is collaborative filtering — looking at what other users with similar listening histories played next — rather than analysing the songs themselves.">It analyses the musical structure of songs you like and finds similar ones</q-option>
  <q-option correct reason="Correct. This is collaborative filtering: the system doesn&#x27;t analyse what songs sound like — it notices that users who played what you played also played something else. It&#x27;s finding you in a space of similar listeners, not understanding music. This is why recommendations can be surprisingly accurate while also occasionally baffling.">It uses patterns across many users to identify what people like you tend to listen to next</q-option>
  <q-option reason="Some music services have used human-curated tagging (genre, mood, tempo) as one input, but this is not how recommendation systems primarily work at scale. Expert categorisation alone cannot produce the granular, personalised suggestions that collaborative filtering achieves across millions of users.">It asks music experts to categorise songs and matches your preferences to categories</q-option>
  <q-option reason="Random selection within a genre would produce recommendations far too broad and imprecise to be useful. Recommendation systems use statistical patterns from large user populations to make targeted predictions about what a specific listener is likely to want next — the opposite of random sampling.">It randomly selects songs from your preferred genres</q-option>
</question>

</quiz>
