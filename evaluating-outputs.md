<frontmatter>
  title: "Evaluating AI Outputs"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Your manager asks you to use an AI tool to check a supplier&#x27;s claim about their product&#x27;s compliance with industry regulations. The AI responds with a detailed, authoritative-sounding paragraph confirming the claim is valid. What does the AI&#x27;s confident tone tell you about whether the claim is actually true?">
  <q-option reason="Confidence in tone doesn&#x27;t correlate with accuracy in language models. The model produces fluent, assertive text whether or not the underlying content is correct. Treating tone as a reliability signal is one of the most common ways AI outputs mislead users.
">A confident tone means the model is more likely to be correct</q-option>
  <q-option reason="Language models don&#x27;t retrieve information from sources at the point of generating a response — they draw on patterns learned during training. There is no citation lookup happening behind a confident-sounding answer, and no guarantee that a reliable source existed for the claim being made.
">A confident tone means the model retrieved the answer from a reliable source</q-option>
  <q-option correct reason="Correct. Models generate text by predicting what comes next, not by verifying facts. A confident tone is a feature of how the text is written, not evidence that the content has been checked. Fluency and accuracy are independent properties of a language model&#x27;s output.
">Very little — the tone reflects how the model generates text, not whether the content is true</q-option>
  <q-option reason="There is no internal verification process in a language model. The model doesn&#x27;t check its output against a database of facts before presenting it. The confident tone is generated for the same reason everything else is — because it&#x27;s the most statistically likely continuation of the text.
">A confident tone means the answer has been verified internally by the model</q-option>
</question>


<question type="text" header="How confident are you that you could spot an error in an AI-generated response in a subject you know well?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>


<question type="mcq" header="You ask an AI for a summary of recent developments in renewable energy policy. Which of the following is the most important limitation to keep in mind?
">
  <q-option reason="AI models can produce fluent text about scientific topics — in fact, this is an area where they often sound highly authoritative. The problem isn&#x27;t an inability to write about science; it&#x27;s the risk that the content sounds credible even when it&#x27;s outdated or inaccurate.
">AI models struggle to write about scientific topics</q-option>
  <q-option correct reason="Correct. Policy is a fast-moving domain where significant changes can happen in months. A model trained up to a cutoff date has no knowledge of legislation, agreements, or announcements that came after it — and won&#x27;t signal that its information is outdated unless explicitly asked.
">AI models have a training cutoff and may not know about recent developments</q-option>
  <q-option reason="AI models can and do produce analytical-sounding text about policy, not just summaries. The concern isn&#x27;t about what type of output they produce but about whether the factual basis of that output is current and accurate.
">AI models only summarise, they cannot analyse policy</q-option>
  <q-option reason="There&#x27;s no established pattern of AI models being biased against environmental topics as a category. The relevant limitation here is about time, not topic — a training cutoff affects anything that has changed recently, regardless of subject matter.
">AI models are biased against environmental topics</q-option>
</question>

</quiz>

<p>[dry run — no content generated]</p>

<panel header="Hallucination Hunt: Confident but Wrong">

**Task:** Pick any AI assistant and ask it to explain a concept from your discipline in plain language. Then ask a follow-up that pressures it for certainty (e.g., "Are you sure?"). Capture exactly what changed.

**Record your findings:**

- Tool Used
- Prompt Used
- Output
- One Surprise
- One Thing To Verify

**Reflect:** Which part of the answer sounded most confident, and what evidence would you need before trusting it in assessed work?

<box type="info" header="Offline alternative">Use the provided sample output from class, then complete the same capture and reflection fields.</box>

</panel>

<pic src="images/evaluating-outputs-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="You&#x27;re writing an essay and you ask an AI to find supporting evidence for your argument. It returns three citations that look plausible. What is the single most important next step?
">
  <q-option reason="Asking for more citations compounds the problem rather than solving it. If the model has generated plausible-sounding but non-existent references, asking for additional ones produces more of the same. Quantity of citations is not a substitute for verifying that they are real.
">Ask the AI to add more citations to strengthen the argument further</q-option>
  <q-option correct reason="Correct. AI models can generate citations that look real — plausible author names, journal titles, and article titles — but don&#x27;t exist. This is one of the most consequential failure modes in academic work. Verification means confirming the source exists and that it actually contains the claim attributed to it.
">Check that the cited sources actually exist and say what the AI claims</q-option>
  <q-option reason="Rephrasing the output in your own words is useful for other reasons, but it doesn&#x27;t address the verification problem. A fabricated citation rephrased in your own words is still a fabricated citation — and is now attributed to you rather than the AI.
">Rephrase the AI&#x27;s response in your own words before submitting</q-option>
  <q-option reason="A different AI model will not reliably catch citation fabrication from another model. AI tools tend to produce similar outputs when given similar inputs, and none of them perform independent source verification. The only check that matters here is looking up the sources yourself.
">Run the response through a different AI to get a second opinion</q-option>
</question>


<question type="mcq" header="A classmate says: &quot;I don&#x27;t really need to check AI outputs in my subject area because I&#x27;d notice if something was wrong.&quot; What is the main flaw in this reasoning?
">
  <q-option reason="Domain familiarity does help with some errors, but it also creates confidence that can make you stop looking. The specific failure mode with AI is plausible-sounding errors that fit existing expectations — those are precisely the ones domain familiarity is least likely to catch automatically.
">It&#x27;s correct — familiarity with a subject makes errors easier to spot</q-option>
  <q-option correct reason="Correct. The dangerous errors aren&#x27;t the ones that look wrong — those get caught. The ones that slip through are the ones that fit the shape of what you expect to see. Domain knowledge helps, but it also creates the confidence to stop looking. The verification habit matters most precisely when something seems fine.
">It assumes errors will be obvious, but plausible-sounding errors are the hardest to catch</q-option>
  <q-option reason="Training data quality is relevant to some failure modes, but it doesn&#x27;t determine whether an individual output contains errors. Models trained on high-quality data still hallucinate and make factual errors. The underlying issue is structural, not a matter of which data was used.
">It&#x27;s only a problem if the AI was trained on low-quality data</q-option>
  <q-option reason="Even in stable subjects, AI can produce confident errors about well-established facts. The training cutoff issue is more severe in fast-moving fields, but hallucination and factual error are not limited to topics that have changed recently. Stable subject matter doesn&#x27;t make AI outputs self-verifying.
">It&#x27;s correct as long as the subject isn&#x27;t changing rapidly</q-option>
</question>


<question type="mcq" header="You&#x27;ve asked an AI to help with a task in a subject you know nothing about. The output looks thorough and well-structured, but you have no way to judge whether it&#x27;s accurate. What is the most appropriate response?
">
  <q-option reason="Structure and thoroughness are properties of the writing, not of the underlying accuracy. A model can produce a well-organised, detailed response on a topic where it has no reliable information. Appearance of quality is not the same as quality of content.
">Trust it — a thorough, well-structured response is a good sign</q-option>
  <q-option reason="Discarding the output entirely is overcorrecting. AI can provide useful starting points even in unfamiliar domains — the problem is not that the output is worthless, but that you can&#x27;t evaluate it yourself. The right response involves using it carefully, not rejecting it entirely.
">Discard it — AI outputs in unfamiliar domains are never reliable</q-option>
  <q-option correct reason="Correct. Knowing that you can&#x27;t judge an output is itself a form of calibration — and it&#x27;s the honest position. The right move is to be explicit about that uncertainty and bring in someone or something that can actually evaluate what matters. This is good epistemic practice regardless of whether AI is involved.
">Acknowledge your uncertainty, and find a way to get the output verified by someone who can judge it</q-option>
  <q-option reason="Asking the same AI to confirm its own output doesn&#x27;t constitute verification — it typically agrees with itself. The model has no independent check it can run on what it just produced. Self-confirmation from an AI is not evidence of accuracy.
">Ask the AI to confirm that the output is accurate</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Find an AI tool you have access to — ChatGPT, Claude, Gemini, Copilot, or any other. Ask it to explain what a hallucination is in the context of AI language models, in plain language for someone who hasn't studied AI before. Record exactly what it says.


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** Compare what the AI told you to what you read in Units 2 and 4. Did it get the key ideas right? Did it introduce any oversimplifications that might mislead a reader? What would you change about the explanation it gave?


<box type="info">Any tool works — variation across the cohort is useful. If you can, try the same prompt on two different tools and note what differs.
</box>

</panel>


<panel header="LLM Excursion" type="seamless">

**Task:** Ask an AI tool to give you five specific factual claims about a topic you know well — your field of study, a hobby you're expert in, or a subject you've recently researched thoroughly. Record all five claims, then systematically check each one. For each claim, note: is it accurate, partially accurate, or wrong? How confident did the AI sound?


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** How many of the five claims were fully accurate? Did the AI's confidence level vary between accurate and inaccurate claims, or was the tone consistent regardless? What would have happened if you had accepted all five claims without checking — in a domain you didn't already know well?


<box type="info">Choose a topic where you can genuinely verify the claims. The exercise only works if you can tell the difference between accurate and fabricated.
</box>

</panel>


<question type="mcq" header="Which of the following best describes the relationship between AI generation and human judgement?
">
  <q-option reason="Generation and judgement are not symmetric capabilities in current AI systems. A model can produce a plausible output without being able to evaluate whether that output is accurate, appropriate, or fit for purpose. Treating them as interchangeable removes the human check that makes AI use safer.
">AI can generate and judge equally well — the two are interchangeable</q-option>
  <q-option reason="Avoiding AI generation entirely is an overcorrection. The appropriate response to error risk is verification and judgement, not avoidance. AI generation can be genuinely useful as a starting point — the skill is in evaluating what it produces, not in refusing to use it.
">Humans should avoid using AI for generation because errors are too common</q-option>
  <q-option correct reason="Correct. Getting a draft on the page, exploring options, and summarising large amounts of text are areas where AI adds real value. Evaluating whether that output is accurate, appropriate, and fit for purpose is still something humans do better. That gap between generation and judgement is where AI literacy lives.
">AI is well-suited to generating a first draft; humans are still better at judging whether it&#x27;s good</q-option>
  <q-option reason="This is a claim about a future state that doesn&#x27;t reflect current evidence. Even as AI improves at generation tasks, the ability to evaluate outputs — for accuracy, appropriateness, and context — remains a human capability. There&#x27;s no established trajectory showing that judgement will be automated away alongside generation.
">Human judgement will become unnecessary as AI improves</q-option>
</question>


<question type="mcq" header="In 2023, a lawyer in New York used ChatGPT to help prepare a legal brief and submitted it to court. The filing contained multiple case citations that looked perfectly real — complete with case names, volume numbers, and page references. When the judge checked, the citations turned out to be entirely fabricated by the AI. The lawyer was sanctioned by the court. This is directly relevant to your studies. Imagine you ask an AI tool to find three scholarly references supporting the Thaumic Resonance Theory of Octarine Decay, and it gives you three confident-looking citations with authors, journal names, dates, and page numbers. What should you assume?
">
  <q-option reason="This is exactly the trap the New York lawyer fell into. AI systems generate text that looks structurally correct — proper formatting, plausible author names, real-sounding journal titles — but the details can be completely invented. Specificity is not the same as accuracy. HEX at least has the decency to produce an Out Of Cheese Error when it runs out of reliable information. Large language models do not.
">The citations are probably real because the AI included specific details like page numbers and dates</q-option>
  <q-option correct reason="Correct. This is the verification reflex in action. AI language models generate plausible-looking text by predicting likely word sequences, not by looking things up in a library catalogue. They will invent citations with the same confidence they use to produce real ones. The Librarian would be appalled — and you do not want to appall the Librarian. Always check that a cited work actually exists before you rely on it.
">Every single citation must be independently verified before use, because AI tools routinely fabricate references that look authentic</q-option>
  <q-option reason="AI outputs are not consistent in this way. One citation in a list might happen to correspond to a real paper while the others are entirely fabricated, or all three might be invented, or all three might be real. Each output is generated independently in terms of its relationship to reality. You must check every single one. Think of it this way — if you found three unfamiliar mushrooms in the Shades, you would not taste one and assume the rest were safe based on surviving the first.
">You only need to check one of the three — if one is real, the others probably are too</q-option>
  <q-option reason="The fabrication of references is not limited to any particular field. It has been extensively documented across law, medicine, the sciences, history, and the humanities. The underlying mechanism is the same regardless of subject matter — the AI is generating text that fits the pattern of a citation, not retrieving actual records. Whether you are writing about tort law or thaumaturgical field theory, the risk is identical.
">This only happens with legal citations — academic references from AI tools are generally reliable</q-option>
</question>


<question type="mcq" header="Most first-year students assume that AI tools are least reliable for creative or subjective tasks and most reliable for straightforward factual or mathematical tasks. In reality, as of 2025-2026, AI systems have a well-documented and perhaps surprising limitation in one of these areas. Which of the following describes a real, current failure mode that challenges common assumptions about what AI tools are good at?
">
  <q-option correct reason="Correct. This surprises many people because counting letters feels like exactly the kind of simple, objective task a computer should handle perfectly. But large language models process text as tokens — chunks of characters — not as individual letters. When asked how many times the letter &quot;r&quot; appears in &quot;strawberry,&quot; models have famously and repeatedly answered &quot;2&quot; instead of the correct answer, 3. They also make errors in multi-step arithmetic, especially with larger numbers. This is because they are generating probable-looking answers, not actually computing. It is a fundamental architectural limitation, not a bug that will be patched next week. Even HEX can count to three, provided it has enough cheese.
">Large language models frequently make errors in basic arithmetic and counting tasks, such as counting the number of times a specific letter appears in a word</q-option>
  <q-option reason="This is not accurate. Modern AI language models can generate text in many languages, including Morporkian, Klatchian, and hundreds of Roundworld languages. They tend to perform best in English due to training data imbalances, but multilingual capability is well established. The real surprise limitations lie elsewhere.
">AI tools cannot generate text in languages other than English</q-option>
  <q-option reason="If only this were true. One of the most important things to understand about current AI systems is that they do not reliably know what they do not know. They will often answer confidently even when the answer is wrong or entirely made up. This is the opposite of refusing to answer — and it is exactly why the verification reflex matters so much. A good wizard knows the limits of their knowledge. Current AI tools frequently do not.
">AI tools always refuse to answer questions about topics they are uncertain about</q-option>
  <q-option reason="While AI image generation has improved significantly, as of 2025-2026 these tools still produce errors with hands (extra fingers, impossible joint angles) and with text in images (misspellings, garbled letters) with noticeable frequency. The improvements are real but the problems are not solved. However, this limitation is fairly well known and would not surprise most students — the question asks about an unexpected failure mode.
">AI image generators have now overcome all problems with generating human hands and text in images</q-option>
</question>


<question type="mcq" header="You are a first-year student writing an essay on the historical impact of the Mage Wars on trade routes across the Sto Plains. You have used an AI tool to help draft a section, and it has produced a confident, well-written paragraph claiming that &quot;the Siege of Pseudopolis in AM 1289 resulted in a forty-year closure of the Ankh-Sto trade corridor, reducing commerce by an estimated 73%, according to Frumkin&#x27;s Economic History of the Plains (Unseen University Press, AM 1902).&quot; The paragraph reads beautifully. You have never heard of Frumkin or this specific claim. What is the best approach?
">
  <q-option correct reason="Correct. This is the full verification approach, and it is what the situation requires. You need to check multiple things independently. First, does this source actually exist? (Check the catalogue. Bring a banana.) Second, if it does exist, does it actually say what the AI claims it says? AI tools sometimes cite real sources but misrepresent their contents. Third, are the specific factual claims — the date, the duration, the statistic — accurate? A plausible paragraph can contain a real source, a misquoted claim, and an invented statistic all at once. Each element needs separate verification.
">Check whether Frumkin&#x27;s book exists in the Library catalogue, verify the specific claim about the 73% figure and forty-year closure in the actual source if it exists, and check the date and details of the Siege independently</q-option>
  <q-option reason="This is the approach that gets people into trouble. Sounding authoritative is exactly what AI language models are designed to do. The specificity of the citation — publisher name, date, precise percentage — makes it feel more trustworthy, but as we saw in the case of the fabricated legal citations (q04-d01), AI tools generate specific-sounding details with the same ease whether those details are real or invented. A confident tone is not evidence. A page number is not proof. Your essay marker will check, even if you do not.
">The paragraph sounds authoritative and includes a specific source with a publisher, so it is probably fine to include as written</q-option>
  <q-option reason="This does not work. When asked to verify its own outputs, an AI tool will often simply confirm what it already said, because the same text-generation process that produced the original claim will produce a confident-sounding confirmation of it. It is like asking a compulsive storyteller whether the story they just told you is true — they will say yes with great conviction. Verification must happen outside the system that generated the claim. Go to the Library. Use an independent source. Ask a lecturer. Do not ask the tool to mark its own homework.
">Ask the same AI tool whether its own citation is accurate — if it confirms the source, you can trust it</q-option>
  <q-option reason="This is tempting but dangerous. If you cannot verify the specific claims, you also cannot verify the general claim that they were supposed to support. The Siege of Pseudopolis might have happened at a different date, lasted a different duration, or had entirely different economic consequences — or the AI might have conflated multiple events, or invented the entire scenario from plausible fragments. Removing the details while keeping the conclusion is like removing the foundations while keeping the building. If you cannot verify the claim, do not include it. Find what the actual sources say and build your argument from there.
">Remove the specific percentage and source reference but keep the general claim, since the broad historical point is likely correct even if the details are wrong</q-option>
</question>

</quiz>
