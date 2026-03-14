<frontmatter>
  title: "Under the Hood"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Imagine a large language model was a band member. Which role fits best?
">
  <q-option reason="Rhythm is predictable, but LLMs are not about timing — they predict the next word using probability, not a beat.">The drummer who keeps perfect rhythm</q-option>
  <q-option correct reason="Close. LLMs riff plausible language on the fly without consulting a script, similar to an improvising guitarist who knows many patterns but never repeats exactly the same solo.">The guitarist who riffs without a script</q-option>
  <q-option reason="Conductors have full scores and plan every gesture. LLMs have no score or plan; they react to each input token sequentially.">The conductor who reads every note ahead of time</q-option>
  <q-option reason="This sounds repetitive, but LLMs actually produce ever-shifting text instead of looping a fixed chorus — every reply is newly generated.">The singer who keeps shouting the same chorus</q-option>
</question>


<question type="mcq" header="Quick warm-up: if you had to compare a large language model to one of these, which feels closest right now?
">
  <q-option reason="This is a common instinct, because AI answers can feel like polished search results. But a language model is not searching the web by default and stitching together sources. That mistaken comparison is exactly what this unit is about to unsettle.">A search engine in a very expensive coat</q-option>
  <q-option correct reason="Closest. A language model is not literally improvising, but this metaphor gets at something important: it produces plausible next bits of language in real time, without checking whether the performance is true. It is a useful starting picture, even though the mechanics are more technical than that.">An improv performer who is extremely good with words</q-option>
  <q-option reason="This makes the system sound far more reliable than it is. Calculators are built to return correct outputs from defined inputs. Language models are built to produce plausible text, which is why they can sound certain while being wrong.">A calculator for facts</q-option>
  <q-option reason="This is one of the most dangerous comparisons. Human expertise is grounded in memory, judgment, and experience. A language model has none of those in the human sense, even when its tone sounds authoritative.">A human expert who just types unusually fast</q-option>
</question>


<question type="mcq" header="What do you think happens when you type a message to an AI like ChatGPT and hit send?
">
  <q-option reason="This is a reasonable starting point — many people assume language models work like a very sophisticated search engine. The unit will show why this model is mistaken: there is no live search happening, no retrieval of external documents, and no &#x27;assembly&#x27; in the way you might imagine.">The AI searches the internet for the most relevant information and assembles an answer</q-option>
  <q-option reason="This is a reasonable starting point — imagining a database of facts is intuitive. But language models don&#x27;t work this way: there is no structured database of facts to look up, and the model has no mechanism for verifying whether what it produces is factually correct.">The AI retrieves the correct answer from a stored database of facts</q-option>
  <q-option reason="This is a reasonable starting point — and it&#x27;s the closest of the four options to what actually happens. After reading the unit, come back to this and notice how the full explanation makes this description feel both more accurate and more surprising than it first appeared.">The AI generates a response by predicting, word by word, what text is likely to follow your message</q-option>
  <q-option reason="This is a reasonable starting point — imagining a logical reasoning process is a natural assumption. But language models have no separate reasoning engine and do not work through problems logically in the way a human or a rule-based system might. The unit will explain what is actually happening instead.">The AI connects to a reasoning engine that works out the logical answer to your question</q-option>
</question>


<question type="text" header="How confident are you that you could explain, to a friend, why an AI language model sometimes states false things as if they were definitely true?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>


<question type="mcq" header="An AI language model produces a response that sounds authoritative and well-structured, but contains a factual error. What does this most likely tell you?
">
  <q-option reason="A factual error in an otherwise fluent response is not a sign of malfunction — it is the model working exactly as designed. The model was optimised to produce plausible-sounding text, not to verify claims. Confident errors are an expected output, not an exception to be patched.">The model is malfunctioning and needs to be updated</q-option>
  <q-option correct reason="Correct. The model was optimised for fluency, not accuracy. It has no internal fact-checker and no mechanism for expressing genuine uncertainty when it lacks knowledge. Producing confident-sounding text — even when that text is wrong — is the model working as designed. This is the most important single thing to understand about using these tools safely.">The model is doing exactly what it was built to do — producing plausible-sounding text</q-option>
  <q-option reason="Language models do not have a reliable mechanism for detecting the limits of their knowledge. When a model reaches a topic it &#x27;knows&#x27; less about, it does not flag uncertainty — it continues producing fluent, confident-sounding text. The absence of a warning is not evidence of accuracy.">The model detected that this topic was outside its knowledge and flagged it</q-option>
  <q-option reason="Cleaner training data can reduce some error types, but it does not fix the underlying issue. The model has no truth-checking mechanism — even with perfect training data, it would still produce confident-sounding text about things it effectively does not &#x27;know&#x27;. The problem is architectural, not just a data quality issue.">The error came from the training data and would have been fixed if the data were cleaner</q-option>
</question>

</quiz>

<h1>Under the Hood</h1>

<p>Before you read this page, you'll see a few questions appear. Don't skip them. The point isn't to get them right — it's to make you think before you're told what to think.</p>

<h2>What actually happened during training</h2>

<p>A large language model is built by training software on an enormous volume of text — web pages, books, forums, code, articles, conversations — far more than any person could read in a lifetime. That text was not curated for accuracy; it was assembled at scale, so the system learned from good arguments and confident misinformation alike.</p>

<p>Through billions of iterative adjustments, the system was trained to do one thing well: <strong>predict which word (or token) is most likely to follow a given sequence of text</strong>.</p>

<p>That is the entire training objective. The model is not a database of verified facts, not a reasoning engine, not a knowledge store. It is a large set of learned statistical patterns derived from text.</p>

<h2>Tokens, not words</h2>

<p>The model technically operates on <strong>tokens</strong> — subword units roughly the size of a syllable or short word — but the key point is the same either way: it is doing pattern matching. When you ask a question, it generates text that statistically resembles a plausible response, based on everything it was trained on. It is not retrieving a stored answer or working through a logical chain of reasoning.</p>

<p>The output often looks deliberate and well-informed because competent-sounding prose appeared frequently in the training data — not because the system possesses the competence it appears to demonstrate.</p>

<h2>Why it sounds so confident</h2>

<p>The model was optimised for <em>plausibility</em>, not accuracy. These are different objectives.</p>

<p>The system has no internal mechanism for verifying its claims against reality. When it produces a fabricated citation, an invented date, or a confident but incorrect assertion, it does so with the same fluency it applies to well-evidenced statements. The field calls these errors <strong>hallucinations</strong>, though the term is more dramatic than the cause: the model simply follows a probable linguistic trajectory that happens to diverge from the truth.</p>

<p>This is not a malfunction. It is the system working as designed.</p>

<h2>What the model doesn't have</h2>

<p>Your knowledge is grounded in continuous lived experience — you know things because you have a body, memory, and a history of interacting with a world that provides real feedback. The model has none of this. It has no persistent memory across conversations, no sensory experience, and no way to check whether what it says is true.</p>

<p>What it does have is an uncanny ability to produce text that resembles expertise. That resemblance can be genuinely useful — and consistently misleads users who mistake fluency for reliability.</p>

<h2>Why this matters</h2>

<p>Plausibility is not correctness. Fluency is not accuracy. The appropriate response to a well-written LLM output is not trust — it is <strong>engaged scepticism</strong>: knowing which errors are likely, developing habits of verification for consequential claims, and treating generated text as a starting point rather than a conclusion.</p>

<hr />

<p><em>Reflection prompt (not graded): Think about the last time you used an AI tool. With what you now know about how it works, is there anything you'd do differently? Write a sentence or two — for yourself, not for anyone else.</em></p>


<box type="tip" header="#### Reflection :fas-lightbulb:">

Where in this unit did you most clearly see the shift from hand-written rules to learning from data, and why does that shift matter in practice?

</box>

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
  <iframe src="https://www.youtube-nocookie.com/embed/jWQFCTLq7a8" title="Introduction video" style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;" allowfullscreen></iframe>
</div>

<pic src="images/under-the-hood-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="What was the core task that a large language model was trained to do?
">
  <q-option reason="Answering questions correctly was never the explicit training objective. The model learned to answer questions as an emergent capability — because question-and-answer text appeared in the training data and predicting plausible responses to questions was part of learning to predict text generally. Accuracy was not the target; plausibility was.">Answer questions correctly</q-option>
  <q-option reason="Summarisation is something large language models can do, but it is not the core training task — it is an emergent capability. The model was not trained to summarise; it learned to produce text that resembles summaries because such text appeared in training data alongside longer source material.">Summarise large amounts of text</q-option>
  <q-option correct reason="Correct. Next-token prediction is the core training objective. Everything else the model appears to do — answering questions, explaining concepts, writing code, translating languages — emerges from doing this one task extremely well across an enormous volume of training text. The model was never explicitly taught to &#x27;know&#x27; facts; it learned to produce text that resembles plausible responses.">Predict what word (or token) is likely to come next in a piece of text</q-option>
  <q-option reason="There is no stored knowledge base and no matching process. Language models do not retrieve answers from a structured store of information — they generate text by predicting likely continuations. This is why they can produce fluent, confident-sounding answers about things that are entirely wrong: there is no database of correct answers to retrieve from.">Match questions to the best-fitting answers in a stored knowledge base</q-option>
</question>


<question type="mcq" header="The page describes LLM errors as a &quot;feature of the architecture, not a bug to be patched.&quot; What does this mean?
">
  <q-option reason="Hallucinations are not intentional features — they are an undesired but structurally inevitable consequence of how the model works. Developers actively try to reduce them through fine-tuning and RLHF, but they cannot be designed away because the underlying architecture has no truth-checking mechanism.">Hallucinations are intentional — developers added them to make the model seem more human</q-option>
  <q-option correct reason="Correct. Because the model is optimised for plausibility and has no mechanism for verifying claims against reality, confident-sounding errors are an inherent possibility — not an accident waiting to be cleaned up. Better training and fine-tuning can reduce certain error types, but they cannot eliminate the underlying vulnerability while the architecture remains the same.">The errors come from a structural property of how the model works, not from a flaw that could simply be fixed</q-option>
  <q-option reason="Better training data does reduce some errors, but it does not solve the structural problem. Even with perfect training data, a model that predicts plausible next tokens has no way to verify whether its outputs are true. The absence of a truth-checking mechanism is the architectural issue, not the quality of the data.">The model was trained on wrong information and would be error-free with better data</q-option>
  <q-option reason="Newer models do produce fewer errors on many benchmarks, but hallucination has not been eliminated in any deployed model. The claim that errors are being &#x27;eliminated&#x27; misunderstands the source of the problem: it is structural, not a matter of model version. Treating newer models as error-free is one of the more dangerous misconceptions about AI reliability.">Errors only happen in early versions of models and are being eliminated in newer releases</q-option>
</question>


<question type="mcq" header="Which of the following best describes the difference between how you know something and how an LLM &quot;knows&quot; something?
">
  <q-option correct reason="Correct. Your knowledge is grounded in continuous lived experience — a body, a sense of time, relationships, the ability to verify things against the world. The model has none of that. It has patterns extracted from text. When it produces a statement that sounds like knowledge, it is producing text that resembles how knowledge is expressed — not retrieving a fact it has genuinely verified or understood.">You know things through experience and memory; an LLM has learned patterns in text with no experience behind them</q-option>
  <q-option reason="Processing more text does not produce more precise knowledge — it produces a more extensive pattern-matching capability. The model has no mechanism for checking whether what it produces is true, regardless of how much text it was trained on. Volume of training data does not translate into reliability of output.">You know things imperfectly; an LLM knows things precisely because it has processed more information than you</q-option>
  <q-option reason="This comparison collapses a critical distinction. Human memory is grounded in experience, embodiment, and the ability to test beliefs against reality. LLM &#x27;knowledge&#x27; is statistical patterns in text, with no grounding in experience and no ability to verify claims. Treating them as similar leads to over-trusting model outputs.">There is no meaningful difference — both you and the LLM store and retrieve facts in a similar way</q-option>
  <q-option reason="Standard large language models do not access live data — they have a training cutoff and no ability to retrieve current information unless specifically connected to external tools. This option also misses the deeper point: even if a model could access live data, the distinction being drawn is about the nature of knowledge, not about currency of information.">The LLM knows more recent information because it can access live data</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Open any AI tool and ask it: "Explain, in plain language, how you generate your responses. What happens between receiving my message and producing your reply?" Record the explanation it gives you, word for word.


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** Compare the AI's self-explanation to what you learned in Unit 2. Did it describe next-token prediction? Did it mention anything about not having a fact-checking mechanism? Where did its explanation oversimplify, and where — if anywhere — did it add something useful that the unit didn't cover?


<box type="info">This is a generate-then-critique exercise. The AI&#x27;s explanation of itself is not necessarily accurate — evaluating it against what you&#x27;ve learned is the point.
</box>

</panel>


<question type="text" header="Now that you&#x27;ve read the unit — how confident are you that you could explain, to a friend, why an AI language model sometimes states false things as if they were definitely true?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>

</quiz>
