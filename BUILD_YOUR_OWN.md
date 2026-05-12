# From Idea to Live App — No Technical Skills Required, Technically
*Technical skills give you a head start. Non-technical skills give you a different one. We'll get to both.*

> A real account of what I actually did — written in my own voice, on my phone, as it was happening.
>
> This is a guide about building software, written by someone who does not write software for a living — and who had real gaps that showed. We'll get to those too.
>
> If you have an idea — technical background or not — this is for you.

---

## Quick navigation

**Key:** &nbsp; ⚡ Technical advantage &nbsp;|&nbsp; 💡 Non-technical advantage &nbsp;|&nbsp; ✳️ No unfair advantage here

---

🕐 [How this started](#-how-this-started) — ✳️ The story. Start here.

🪞 [Who I am, and why that matters](#-who-i-am-and-why-that-matters) — 💡 Why this worked, and why it can work for you.

⚙️ [Before you read this as "AI did everything"](#%EF%B8%8F-before-you-read-this-as-ai-did-everything--it-wasnt) — ✳️ Why you should stay skeptical. Both of you.

👁️ [What's actually happening while you live your life](#%EF%B8%8F-whats-actually-happening-while-you-live-your-life) — ✳️ The real division of labor.

✅ [The honest truth up front](#-the-honest-truth-up-front) — 💡 What you actually need. And the zero-sum myth.

🛠️ [The tools and what they cost](#%EF%B8%8F-the-tools-and-what-they-cost) — ✳️ Four tools. Under $75.

📋 [Phase 1 — Think before you build](#-phase-1--think-before-you-build) — ✳️ The cheapest and most important phase.

🔧 [Phase 2 — Set up your tools](#-phase-2--set-up-your-tools-one-time) — One time. Done.

🏗️ [Phase 3 — Build it](#%EF%B8%8F-phase-3--build-it) — ⚡ Directing vs. executing. Working closely with the model is how you stay ahead.

🚀 [Phase 4 — Deploy it](#-phase-4--deploy-it) — Get it live.

🤝 [Phase 5 — Don't stop at "it works"](#-phase-5--dont-stop-at-it-works) — ✳️ Collaboration story + who to bring in and when.

🧠 [The mindset](#-the-mindset) — ✳️ Applies to everyone. Both sides get called out.

🏁 [Go build the thing](#-go-build-the-thing)

📚 [Research & receipts](#-research--receipts) — Verify them yourself. That's the point.

---

## 🕐 How this started

Time is the one resource you can never get back.

I built a working, deployed web application in roughly 4 hours of actual effort spread across 2 days.

Not 4 uninterrupted hours. 4 hours of stolen minutes — entirely on my phone.

Between chores. Waiting rooms. The Lyft was late. Sitting at the playground between actually playing with my kid. A minute here, a few minutes there. Responsibly watching a child at a playground is not a perfect time to build software. It turned out to be plenty of time.

From first idea to working POC to showing it to a veteran friend while we watched our kids run around — all on my phone. Talking, typing, reviewing, directing.

He used it on my phone at the playground. On the spot. That's when I knew it was real.

There is no perfect time. You say something, wait for things to happen, review when a moment opens up. The moments were real. The product was real.

This guide exists because I think a lot of people — technical and not — have ideas sitting in their heads that they assume require more than they have. I wanted to show what's actually possible right now, and exactly how I did it.

The app: **[vetassist-production.up.railway.app](https://vetassist-production.up.railway.app)** — go see what it does.

The hackathon repo: **[github.com/akaseahawk/VetAssist-Wilcore-IC-2026](https://github.com/akaseahawk/VetAssist-Wilcore-IC-2026)**

Questions or want to talk through your own idea? Reach out directly.

---

## 🪞 Who I am, and why that matters

Anyone with an idea can do this. My background shaped how fast I moved. It also came with gaps. Both matter.

I'm an AI solution architect, AI engineer, data engineer, and data scientist. I have a biomedical engineering degree and a background in engineering management. I am not a software developer, not a DevOps engineer, not a UI/UX professional, not a contracts expert, not an end user of what I was building. I don't build production web applications for a living — I write code, but there's a difference.

I had real gaps. I can't eyeball a security vulnerability the way a trained engineer can. I don't have the instincts that come from years of shipping software. I'm not the veteran trying to navigate a broken system. Those gaps were real, and they showed.

What filled them: AI compensated for a lot of what I couldn't do alone — not perfectly, but well enough to ship something real. Then the right people came in and took it further. That's the actual story. Phase 5 covers it.

What I did bring: I think in systems. I can spec a problem, identify failure modes, manage toward an outcome, and notice when the AI is confidently heading somewhere wrong. Working with this generation of AI is, fundamentally, engineering management. I've been developing that skill for about 3 years, and it shows in the output.

*(Software developers reading this: you have every advantage I have, plus the ability to read the code and know if it's actually right. You should be doing this in half the time. I'm not sure why you aren't.)*

---

## ⚙️ Before you read this as "AI did everything" — it wasn't

Three years of refining custom instructions that shape how any AI works with me — a personal operating agreement between me and the model, sometimes called a `CLAUDE.md` file or system prompt.[^9] Mine does three things:

- **Numbered structured output** — everything is numbered hierarchically so I can say "2.3 is wrong" and we both know exactly what we're talking about. Small thing. Not a small thing.
- **Show your work** — the AI shares what it's deciding and why, before acting. I'm getting its reasoning, not just output — which I can agree with, correct, or redirect.
- **Structured push-back** — it flags disagreement and risk instead of just complying. An AI that only agrees with you is a faster way to be wrong.[^6]

The tools got dramatically better over those 3 years. So did my ability to work with them.

**On trusting AI reasoning:** research shows that what an LLM says it's doing isn't always what it's actually doing.[^1][^2][^3] The chain-of-thought is useful — not a guaranteed window into the model's actual process. Trust, but verify. What to verify: does the output do what you asked, does it behave correctly for a real user, and does anything feel off even if you can't articulate why. That instinct matters. Act on it.

This applies to everyone — technical readers included. Knowing how to read code doesn't make the model's stated reasoning accurate.

---

## 👁️ What's actually happening while you live your life

While I was doing dishes, pushing a kid on a swing, waiting for a Lyft — this is what was running:

| What I was doing | What the AI was doing |
|---|---|
| Talking through my idea | Asking clarifying questions, pushing back, finding holes |
| Describing a feature | Writing code, wiring it to the backend, testing it |
| Saying "that looks wrong" | Diagnosing, proposing a fix, explaining why |
| Doing literally nothing | Building, deploying, verifying, documenting |
| Waiting for a Lyft | Working through system architecture |
| Playing with my kid | Running API tests, checking browser behavior, fixing edge cases |
| Reviewing on my phone before bed | Already done. Waiting for my feedback. |

What that actually looked like on my phone:

![Perplexity Computer working — task list sprint](assets/perplexity-working-1.png)
![Perplexity Computer working — editing code files](assets/perplexity-working-2.png)

You're not doing the work in the traditional sense. You're directing it. There's a meaningful difference — and real responsibility that comes with it.

---

## ✅ The honest truth up front

You do not need to write code to get started.
You do not need a CS degree to ship something real.[^8]
You do not need a free weekend.

What you need: a clear idea, the willingness to think it through, and about $20/month.

**On non-technical advantages:** knowing the problem from the inside, seeing clearly what real users actually need, and not getting distracted by what's technically interesting — those are genuine advantages. Research consistently shows non-technical people face real barriers to building, often assuming they can't start at all.[^8] That assumption is wrong, and it's expensive. The people who get the most out of AI-assisted building aren't always the most technical — they're the ones who know what they're building and why.

**On technical advantages:** systems thinking, the ability to read the AI's output critically, and knowing when something is technically correct but practically wrong — those matter too. Technical people can move faster, catch more errors, and ask better questions of the model.

**Neither is complete without the other. This is not zero-sum.**

The common framing is that AI takes the output or humans do. That's the wrong model. Used well, it's 2+2=8. The human brings judgment, domain knowledge, and the ability to say "this is wrong for this user." The AI brings speed, breadth, and the ability to hold an entire codebase in memory while you're at the playground. The combination produces something neither could alone. That's the actual story of VetAssist — and it's the point of this guide.

Getting something working is not the same as getting something right. A prototype is a starting point. When real people depend on it, you want the right eyes on it. More on that in Phase 5.

---

## 🛠️ The tools (and what they cost)

| Tool | What it does | Cost |
|---|---|---|
| **Perplexity Computer** | AI co-pilot — browses the web, writes and runs code, manages files, deploys apps. Desktop and mobile. | ~$20/month |
| **Claude Code** (via Anthropic API) | Heavy-lifting code builder. Perplexity calls it automatically. | Pay-as-you-go — start with $20–50 |
| **GitHub** | Stores your code. Every change tracked. If something breaks, you go back. | Free |
| **Railway** | Hosts your app live. Connects to GitHub — push code, app updates. | Free tier / ~$5/month always-on |

**Realistic total to launch: $20–75.** The Anthropic credits are the variable — Phase 1 exists to keep that number down.

---

## 📋 Phase 1 — Think before you build

> The most important phase. Also the cheapest.

The most common mistake: building before the idea is solid. The AI will confidently build the wrong thing if you let it.[^6]

*(Technical people: this applies more to you, not less. You can move fast enough to get very far in the wrong direction before noticing.)*

**Do this phase outside Claude Code.** Perplexity Computer, Claude.ai, ChatGPT — free or close to it. Save the API credits for building.

You can do all of Phase 1 on your phone. Waiting room. Walk. That's where most of VetAssist came from.

### Have a real conversation with AI about your idea

Talk it out. Voice-to-text. Ask it to push back. Cover these:

- **What problem does this solve?** Specific beats general.
- **Who is it for?** Name one real person. What's their actual frustration?
- **What does it do, step by step?** Walk through it like you're showing someone.
- **What does it NOT do?** As important as the above.
- **What's the smallest version that proves the idea works?** Build that first.
- **Does it touch anything sensitive?** Flag it now.

Push it: *"What are the holes in this? What would a skeptical user say? What's the riskiest assumption?"*

### Write a one-page brief

Before Phase 2:

- What it does (2–3 sentences)
- Who it's for
- The main flow
- What it does NOT do
- The simplest first version
- Any known risks

This is what you hand the AI when building starts. The better it is, the less rework, the fewer credits burned.

---

## 🔧 Phase 2 — Set up your tools (one time)

**1. GitHub** — [github.com](https://github.com). Free. Sign up.

**2. Perplexity Computer** — [perplexity.ai](https://perplexity.ai). Subscribe.

**3. Anthropic API key** — [console.anthropic.com](https://console.anthropic.com). Add $20–50 in credits. Keep the key private. Do not share it or post it anywhere.

**4. Railway** — [railway.app](https://railway.app). Sign up with your GitHub account.

---

## 🏗️ Phase 3 — Build it

Perplexity Computer and Claude Code work together. You direct.

### Hand over your brief

Paste your one-page brief into Perplexity Computer:

> *"I want to build this app. Here's what it does, who it's for, and what the first version needs. I'll be directing and reviewing — you handle the building."*

It asks questions, writes code, tests things, explains decisions. Your job: review, flag what's wrong, stay engaged.

### Reviewing the work

- Does this do what I asked?
- Does it behave the way a real user would expect?
- Is there anything I don't understand that I probably should?

If you can't get a plain-language explanation, ask for one. Complexity you can't explain is complexity you can't stand behind.

*(Technical readers: you get to read the code and know if it's actually correct. Use that.)*

### Test it like a real user

Walk the full flow. Try weird inputs. Use it on your phone. Ask "what happens if someone does X?" Report what you find. It fixes things.

### On security and sensitive data

If your app touches anything personal, raise it explicitly:
- "Is this stored securely?"
- "Can one user access another user's data?"
- "What happens if someone tries to abuse this?"

The AI addresses what you ask. It doesn't always volunteer what you don't.[^7] You need to be the paranoid one.

---

## 🚀 Phase 4 — Deploy it

**Push to GitHub** — Perplexity Computer handles this.

**Connect Railway** — link to your GitHub repo, done once. Every future push auto-deploys. You get a live URL.

### When things don't look right

| Situation | What to do |
|---|---|
| Pushed new code | Nothing — auto-deploys in ~60–90 seconds |
| Changed a Railway env variable | Auto-redeploys when you save |
| App frozen or stuck | Railway dashboard > Deployments > Restart |
| Browser showing old version | Hard refresh: `Cmd+Shift+R` / `Ctrl+Shift+R` |

---

## 🤝 Phase 5 — Don't stop at "it works"

Working is the beginning.

The MVP worked. A real veteran used it and it held up. Still rough — functional, not polished. Then the right people came in, not at the beginning to help me start, but after there was something worth building on. That's the sequence.

- **Matt** — full accessibility overhaul, P0 through P2. VA Design System alignment: progress bars, alerts, buttons, card/list semantics, VA web components and fonts. Cognitive accessibility, responsive layout, 200% zoom, static assets, scan/camera capture, document upload refinement. Edited the demo videos.
- **Regan and Tyson** — both veterans — used it as actual end users. They knew what the experience should feel like and where it fell short. No technical review substitutes for that. Regan also produced the demo videos.
- **Andrew** — reviewed contract viability. Whether this could go somewhere in a government context. Mattered.
- **Selia** — reviewed the presentation. Fresh eyes on whether it landed.
- **Amy** — accessibility consult before the overhaul started. Right framing early meant less rework.

**[vetassist-production.up.railway.app](https://vetassist-production.up.railway.app)** — that's what collaboration does to an MVP.

You don't need a team to start. You need something for them to work with.

### What to look for when you bring people in

| Who | What to ask |
|---|---|
| **Technical reviewer** | Is this secure? What breaks under load? Does it do what I think in every case? |
| **Domain expert** | Does this actually solve the problem? Where does it fall short for a real user? |
| **Fresh eyes** | Does this make sense? What's confusing? |

---

## 🧠 The mindset

The AI is the engineering team. You are the product owner.

- **Talk to it like a colleague.** Push back. Ask why. You'll build better things and understand what you built.
- **Iterate in small steps.** One thing working beats five things halfway done.
- **Don't panic when things break.** They will. Tell the AI what happened. It fixes things.
- **Stay humble about what you don't know.** Running doesn't mean right, secure, or correct under all conditions.
- **Think before you build.** Phase 1 is free. *(Technical people: especially you.)*
- **If you have technical skills — use them.** Read the code. That knowledge doesn't become less valuable because the AI did the typing. *(Non-technical readers: this is why Phase 5 matters.)*

---

## 🏁 Go build the thing

Most people stay stuck at "I wish someone would build something that..." — assuming the gap between idea and reality requires more than they have.

It doesn't. Not anymore.

You can start today. On your phone. Between whatever is happening in your life.

Time is the one resource you can never get back. The question isn't whether you have enough — it's what you do with the pieces you actually have.

**[vetassist-production.up.railway.app](https://vetassist-production.up.railway.app)** — go use it. Then come build your own.

Questions or want to talk through your idea? Reach out directly.

---

*Written on my phone, as a deliberate test case of what's possible right now. The entire build — from first idea to working POC — was done on my phone. Chores, waiting rooms, Lyft rides, the playground. The desktop only came out for the presentation, which is a slide deck and not a web application and therefore doesn't count.*

*A veteran friend tested the finished product on my phone while our kids played.*

*That's the bar. You can clear it.*

---

## 📚 Research & receipts

I've spent three years following this space. I'm reasonably confident in these citations. I have not verified every one with the rigor I'd apply professionally — partly because I built this guide the same way I built the app: in stolen minutes, on my phone, between life.

Which means this is a perfect opportunity to practice what this guide preaches: don't trust the AI's work without checking it. I did my part. Now it's your turn.

*(The irony of citing research about AI overconfidence in its own reasoning, in a document partially produced by AI, is not lost on me.)*

Check the quality and applicability yourself. That's not a disclaimer — it's the point.

---

**On AI reasoning — what's actually happening under the hood**

**[1]** Turpin et al., NeurIPS 2023 — *Language Models Don't Always Say What They Think*
https://arxiv.org/abs/2305.04388
CoT explanations can systematically misrepresent the true reason for a model's prediction. Plausible, but not necessarily what drove the answer.

**[2]** Anthropic Alignment Science, April 2025 — *Reasoning Models Don't Always Say What They Think*
https://www.anthropic.com/research/reasoning-models-dont-say-think
Claude 3.7 Sonnet mentioned a contextual hint in its chain-of-thought only 25% of the time. In reward-hacking scenarios, models admitted to the behavior less than 2% of the time.

**[3]** Lanham et al., Anthropic, 2023 — *Measuring Faithfulness in Chain-of-Thought Reasoning*
https://arxiv.org/abs/2307.13702
Intervening on the reasoning chain changes model predictions in ways that show the stated reasoning isn't always load-bearing. Same conclusion, separate study.

---

**On AI capability velocity**

**[4]** Wijk et al., 2024 — *RE-Bench: Evaluating Frontier AI R&D Capabilities Against Human Experts*
https://arxiv.org/abs/2411.15114
AI agents scored 4x higher than human experts on structured ML engineering tasks at a 2-hour budget, generating and testing solutions over 10x faster. ML research engineering specifically — not general app development. The velocity gap is real. Extrapolate accordingly.

---

**On AI-assisted development — productivity, risks, and human judgment**

**[5]** Schmidt et al., 2024 — *Significant Productivity Gains through Programming with Large Language Models*
https://dl.acm.org/doi/pdf/10.1145/3661145
Productivity gains are real. The human's ability to evaluate and redirect output remains the variable.

**[6]** Zhou et al., 2026 — *Cognitive Biases in LLM-Assisted Software Development*
https://www.semanticscholar.org/paper/8592f852439d6b03788ef8ac0c1ddeaef738e4e7
48.8% of programmer actions in LLM-assisted development were biased; LLM interactions drove 56.4% of those. Automation bias and over-reliance are the dominant failure modes. The study behind "the AI will confidently build the wrong thing" and "an AI that only agrees with you is a faster way to be wrong."

**[7]** Haque et al., 2025 — *Hallucinations and Security Risks in AI-Assisted Software Development*
https://ieeexplore.ieee.org/document/11202778/
Security vulnerabilities, hallucinations, and code quality issues in LLM-generated code. The study behind "the AI is not paranoid enough."

---

**On non-technical users building with LLMs**

**[8]** Calò & De Russis — *Leveraging Large Language Models for End-User Website Generation*
https://link.springer.com/10.1007/978-3-031-34433-6_4
End users generating functional websites with no programming background. The research basis for "you don't need a CS degree."

---

**On system prompts and custom instructions**

**[9]** Zhang et al., 2024 — *SPRIG: Improving Large Language Model Performance by System Prompt Optimization*
https://arxiv.org/abs/2410.14826
Optimized system prompts improve performance and generalize across model families, parameter sizes, and languages. Three years of custom instructions is not a quirk — it's documented.
