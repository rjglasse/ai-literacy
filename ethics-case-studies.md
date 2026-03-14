<frontmatter>
  title: "AI in Practice: Ethics and Real Cases"
</frontmatter>

## Warmup

<quiz>

<question type="mcq" header="Before reading anything — if an AI hiring tool rejects more applications from women than from men with similar qualifications, who is most responsible?
">
  <q-option reason="This is a reasonable starting point — the AI did produce the outcome. But an AI system has no intentions, values, or moral agency of its own. Locating responsibility solely in the AI lets every human actor involved off the hook.
">The AI — it made the decision</q-option>
  <q-option reason="This is a reasonable starting point — the deploying organisation made a choice to use this tool and is accountable for its effects. But responsibility doesn&#x27;t end there: the engineers, the data providers, and the regulatory environment all played a role too.
">The company that deployed it — they chose to use it</q-option>
  <q-option reason="This is a reasonable starting point — design decisions shape outcomes, and the people who made them bear some responsibility. But the engineers may not have chosen the training data, the deployment context, or the decision to use the system without audit.
">The engineers who built it — they designed the system</q-option>
  <q-option reason="This is a reasonable starting point — and of the four options, it comes closest to the analysis the unit develops. Ethical responsibility in AI systems is genuinely distributed across multiple actors, none of whom bears full responsibility alone.
">All of the above, in different ways and to different degrees</q-option>
</question>


<question type="text" header="How confident are you that you could explain what &quot;algorithmic bias&quot; means to someone who hasn&#x27;t studied AI or data science?
" answer="Rate yourself from 1 (Not at all confident) to 5 (Very confident).">
  <div slot="hint">Rate from 1 (Not at all confident) to 5 (Very confident).</div>
</question>


<question type="mcq" header="You are affected by an AI decision — for example, a credit-scoring system denies your application. Which of the following is most likely to be true?
">
  <q-option reason="This is rarely the case. Most AI-assisted decisions come with little or no explanation of which inputs drove the outcome. Even where explanation is legally required, what is provided is often a generic summary rather than a meaningful breakdown of the model&#x27;s reasoning.
">You will be told which factors the AI weighted most heavily</q-option>
  <q-option reason="In some regulated sectors — consumer credit in the EU, for example — a right to human review exists on paper. In practice, it is inconsistently implemented, rarely exercised, and often results in a human reviewing rather than overriding the AI&#x27;s output.
">You can request a human review of the decision</q-option>
  <q-option correct reason="Correct. Many AI-assisted decisions are not disclosed as such. A rejection letter may simply cite policy reasons, with no indication that an automated system produced or heavily influenced the outcome. This opacity is one of the central ethical problems the unit examines.
">You may not even know an AI system was involved</q-option>
  <q-option reason="Human review of every AI-assisted decision would defeat most of the efficiency gains organisations seek from automation. In practice, human oversight is often reserved for edge cases, appeals, or high-value decisions — not every output the system produces.
">The AI&#x27;s decision will have been checked by a human before reaching you</q-option>
</question>

</quiz>

<p>[dry run — no content generated]</p>

<box type="tip" header="#### Reflection :fas-lightbulb:">

Choose one stakeholder affected by an AI decision in this unit. What harm is easiest to miss if you only evaluate technical performance?

</box>

<pic src="images/ethics-case-studies-hero.webp" alt="Hero image" width="100%"></pic>

## Knowledge Check

<quiz>

<question type="mcq" header="What is the most precise way to describe &quot;bias&quot; in an AI system?
">
  <q-option reason="Intentional discriminatory programming does exist, but it is not what &quot;algorithmic bias&quot; typically refers to. This framing focuses on individual bad intent, which misses the more common and harder-to-fix case: systems that produce biased outcomes without anyone intending them.
">The AI has been deliberately programmed to favour certain groups</q-option>
  <q-option correct reason="Correct. This is the mechanism behind most algorithmic bias. When historical data encodes patterns of discrimination — in who was hired, who received loans, who was arrested — a model trained on that data learns to reproduce those patterns, regardless of anyone&#x27;s intentions. Fixing it requires examining the data and system design, not just auditing the engineers.
">The AI has learned patterns from training data that reflect and reproduce existing inequalities</q-option>
  <q-option reason="Random errors distributed unevenly might look like bias, but they are not the same thing. Algorithmic bias is typically systematic rather than random — the model consistently underperforms or discriminates against particular groups because of what it learned from the training data.
">The AI makes random errors that happen to affect some groups more than others</q-option>
  <q-option reason="The personal beliefs of individual engineers are rarely the primary cause of algorithmic bias. Even a team with entirely egalitarian intentions can produce a biased system if the training data reflects historical inequalities. The source is usually the data, not the developers&#x27; worldview.
">The AI was trained by people who held personal prejudices</q-option>
</question>


<question type="mcq" header="What is the difference between a technical failure and an ethical failure in an AI deployment?
">
  <q-option reason="This conflates two separate distinctions. A technical failure is about whether the system does what it was designed to do; an ethical failure is about whether it should have been designed or deployed that way. Neither category requires bad intentions — a system can fail technically by accident and fail ethically despite good intentions.
">Technical failures are caused by bugs; ethical failures are caused by bad intentions</q-option>
  <q-option reason="This collapses an important distinction. A system that correctly classifies applications according to its training data is technically working; if that classification produces discriminatory outcomes, the problem is not in the code — it is in the design, data, or deployment decision. Reducing ethical questions to technical ones makes them harder to identify and address.
">There is no meaningful difference — all AI failures are technical in origin</q-option>
  <q-option correct reason="Correct. This is one of the unit&#x27;s central distinctions. Technical success and ethical success are independent: a system can function perfectly according to its specification and still produce harmful, unjust, or discriminatory outcomes. Identifying ethical failures requires asking different questions — not whether the system did what it was told, but whether it should have been built and deployed as it was.
">A system can work exactly as designed and still cause serious harm — the harm is an ethical failure, not a technical one</q-option>
  <q-option reason="Foreseeability can affect how we assign blame, but it does not determine whether a harm is an ethical failure. Many serious harms from AI systems were difficult to anticipate in advance — but that does not mean no one bears responsibility for them, or that the deployment decision was therefore ethical.
">Ethical failures only matter if the harm was foreseeable at the time of deployment</q-option>
</question>


<question type="mcq" header="What makes an AI deployment &quot;high-stakes&quot;?
">
  <q-option reason="This measures stakes from the organisation&#x27;s perspective, not the affected person&#x27;s. A system that is cheap to fix from a business standpoint can still cause serious, lasting harm to individuals — wrongful denial of welfare, housing, or bail, for example. Stakes should be measured by harm to people, not cost to the deployer.
">The AI is operating in a domain where errors are expensive to fix for the organisation</q-option>
  <q-option correct reason="Correct. High stakes are defined by the severity of consequences for the people affected. A system used by very few people but making decisions about medical treatment, criminal sentencing, or child welfare is high-stakes. This framing determines how much scrutiny, human oversight, and accountability the deployment should require.
">The AI makes decisions or recommendations that significantly affect people&#x27;s lives, opportunities, or rights</q-option>
  <q-option reason="Processing sensitive data is a privacy and security concern, and it often correlates with high stakes — but it is not the defining feature. A system could handle vast amounts of personal data while making only low-consequence decisions. Conversely, a system making life-altering recommendations may process relatively little data per case.
">The AI processes large amounts of sensitive personal data</q-option>
  <q-option reason="Scale of use is relevant to aggregate harm, but not to the per-person stakes of a given decision. A system used by millions to make trivial recommendations is not high-stakes in the relevant sense. A system used by a handful of courts to recommend prison sentences is — even though far fewer people interact with it.
">The AI is used by a large number of people</q-option>
</question>


<question type="mcq" header="The unit presents real cases where AI caused harm. Which of the following best describes how those cases are typically resolved?
">
  <q-option reason="AI harm cases rarely produce a clear villain. Because responsibility is distributed across many actors — engineers, product teams, deploying organisations, regulators — it is usually possible for each to argue that someone else bears the primary blame. This diffusion is itself part of what makes the problem hard.
">Clear villains are identified and held accountable</q-option>
  <q-option reason="Harmful AI systems are sometimes modified or taken down, but often only after prolonged campaigning, litigation, or regulatory action — and sometimes not even then. Organisations have financial and reputational incentives to dispute that harm occurred or to make minimal adjustments rather than shutting a system down entirely.
">The AI systems are shut down once the harm is identified</q-option>
  <q-option correct reason="Correct. This is a deliberate and unsettling observation. AI ethics cases tend to unfold over years rather than weeks, involve disputed evidence about who caused what, and are addressed by legal and regulatory frameworks that were not designed for them. Understanding this is not meant to produce cynicism, but to replace an unrealistic &quot;scandal and fix&quot; model with a more accurate picture of how these situations actually resolve.
">Responsibility is contested, harm persists for years, and resolution is slow and incomplete</q-option>
  <q-option reason="This assumes that harm from AI systems is primarily technical in origin and can therefore be addressed by patching code. But if the harm arises from design choices, data, or the decision to deploy at all, there may be no technical fix available — and even when there is, organisational and legal processes typically move far more slowly than software updates.
">Technical fixes are deployed within weeks and normal service continues</q-option>
</question>


<panel header="LLM Excursion" type="seamless">

**Task:** Choose a topic where framing matters — a political issue, a social question, or a controversial decision in your field. Write two prompts that ask the same factual question but frame it differently. For example: "What are the benefits of [policy]?" versus "What are the risks of [policy]?" Send both prompts to the same AI tool and record both responses.


**Capture:**

- tool_used
- prompt_used
- output
- one_surprise
- one_thing_to_verify

**Reflect:** How did the framing of your question shape the AI's response? Did it present different facts, or the same facts with different emphasis? If you had only asked one version, what perspective would you have missed? What does this tell you about the role of the questioner — not just the AI — in shaping outputs?


<box type="info">Try to make the two prompts genuinely different in framing while asking about the same underlying topic. The more clearly you can see the difference in output, the more the exercise reveals.
</box>

</panel>


<question type="mcq" header="Two people look at the same AI deployment and reach different conclusions about whether it is ethical. What should you conclude?
">
  <q-option reason="It is possible that one person has the facts wrong — but that is not what this scenario assumes. If both people share the same factual understanding and still reach different conclusions, the disagreement is about values, not facts. Assuming someone must have misunderstood the facts is a way of avoiding the harder question of which values to prioritise.
">One of them has misunderstood the facts</q-option>
  <q-option reason="The existence of disagreement does not mean there are no better or worse answers to ethical questions. Some positions are better reasoned, more consistent, and more attentive to evidence than others. Disagreement among thoughtful people is a reason to think carefully, not to give up on ethical reasoning altogether.
">Ethical questions about AI have no meaningful answers</q-option>
  <q-option correct reason="Correct. Ethical disagreements often persist even when both parties share the same factual picture, because they are prioritising different values — privacy versus safety, efficiency versus accountability, individual rights versus collective benefit. Recognising this changes how you engage: rather than trying to show the other person is wrong, you can ask what values they are prioritising and why.
">They may be applying different values or weighing the same harms and benefits differently — both positions can be held in good faith</q-option>
  <q-option reason="Ethical disagreement about technology is no different in kind from ethical disagreement in medicine, law, or public policy — domains where we accept that careful ethical reasoning is both possible and necessary. The existence of hard cases and genuine disagreement is an argument for better ethical thinking, not for abandoning it.
">The disagreement proves that ethics cannot be applied to technology</q-option>
</question>

</quiz>
