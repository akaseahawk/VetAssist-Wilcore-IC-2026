# From Idea to Live App — No Technical Skills Required to Start

> This is a test case and a how-to guide. Not a tutorial written by someone
> who read about this. A real account of what I actually did — written entirely
> in my own voice, on my phone, as it was happening.
>
> If you have an idea — technical background or not — this is for you.

---

## How this started

I built a working, deployed web application in roughly 4 hours of actual effort
spread across 2 days.

Not 4 uninterrupted hours. 4 hours of stolen minutes — entirely on my phone.

Between chores. Waiting rooms. Waiting for a Lyft. Driving (voice-to-text, relax).
Sitting at the playground in between actually playing with my kid. From the first idea
to a working POC to showing it to a veteran friend while we watched our kids run around
— all of it was on my phone. Talking, typing, reviewing, directing.

The desktop didn't come in until we were building out the presentation for the final
hackathon submission. The app itself? Phone start to finish.

He used it on my phone at the playground. On the spot. That's when I knew it was real.

This guide exists because I think a lot of people — technical and non-technical —
have ideas sitting in their heads that they assume require more than they have:
more time, more money, more skills, more help. I wanted to demonstrate what's
actually possible right now, and show exactly how I did it so you can too.

The app itself? You can find it at
**[vetassist-production.up.railway.app](https://vetassist-production.up.railway.app)**
— go see what it does. I'll let it speak for itself.

If you want to see what the team turned that POC into for the Wilcore Innovation
Challenge, the full hackathon version is at the same URL — same app, grown up a bit.
The repo is here:
**[github.com/akaseahawk/VetAssist-Wilcore-IC-2026](https://github.com/akaseahawk/VetAssist-Wilcore-IC-2026)**

Questions or want to talk through your own idea? Reach out to me directly.

---

## Before you read this as "AI did everything and it was magic" — it wasn't

I've spent roughly 3 years developing and refining a set of custom instructions that
shape how any AI works with me. Think of it as a personal operating agreement between
me and the model. Some examples of what's in it:

- **Numbered structured output** — everything the AI produces is numbered hierarchically
  (1.1, 1.2.3, etc.) so I can say "what you said at 2.3 is wrong" or "explain 4.1.2"
  and we both know exactly what we're talking about. No ambiguity, no re-reading walls
  of text to find the thing.
- **Show your work** — the AI shares what it's deciding, considers alternatives, and
  gives me a pro/con/reason before acting. I'm not just getting output, I'm getting
  its thinking.
- **Structured push-back** — it's set up to flag when it disagrees or sees a risk,
  not just comply and move on.

This is sometimes called a `CLAUDE.md` file or a system prompt — the AI community
has been writing about this pattern a lot lately because it genuinely changes how
well the collaboration goes. I've been building and tuning mine across projects for
years. The tools got dramatically better, but so did my ability to work with them.

The result blew my mind. But it didn't come from nowhere — I set it up for success.

**One honest caveat on AI reasoning:** research has shown that what an LLM says
it's doing isn't always what it's actually doing under the hood. The chain-of-thought
explanation is useful, but it's not a guaranteed window into the model's true process.
Two studies worth knowing about:

- [*Reasoning Models Don't Always Say What They Think*](https://www.anthropic.com/research/reasoning-models-dont-say-think)
  — Anthropic's own alignment science team (2025) found that model chain-of-thought
  reasoning can be unfaithful to its actual internal process.
- [*Language Models Don't Always Say What They Think: Unfaithful Explanations in
  Chain-of-Thought Prompting*](https://arxiv.org/abs/2305.04388) — Turpin et al.,
  NeurIPS 2023. CoT explanations can systematically misrepresent the true reason for
  a model's prediction — plausible but misleading.

Still useful. Just not gospel. Stay engaged, keep asking questions, don't treat the
AI's self-reported reasoning as ground truth. More on that when we get to the build.

---

## What's actually happening while you live your life

Here's the part that took me a minute to internalize. While I was doing dishes,
or pushing a kid on a swing, or waiting at the doctor's office — this is what
was actually running:

| What I was doing | What the AI was doing |
|---|---|
| Talking through my idea on my phone | Asking clarifying questions, pushing back, helping me find the holes |
| Describing a feature out loud | Writing the code, wiring it to the backend, testing it |
| Saying "that looks wrong" | Diagnosing the problem, proposing a fix, explaining why |
| Doing literally nothing | Building, deploying, verifying, documenting |
| Waiting for a Lyft | Thinking through features, talking out the next step |
| Playing with my kid | Running API tests, checking browser behavior, fixing edge cases |
| Reviewing on my phone before bed | Already done. Waiting for my feedback. |

Here's what that actually looked like on my phone — Perplexity Computer and Claude Code
working through the VetAssist sprint while I was living my life:

![Perplexity Computer working — task list sprint](assets/perplexity-working-1.png)
![Perplexity Computer working — editing code files](assets/perplexity-working-2.png)

That's the shift. You're not doing the work in the traditional sense.
You're directing it. There's a meaningful difference — and it comes with real
responsibility, which I'll get to.



You do not need to know how to code to get started.
You do not need a computer science degree.
You do not need a technical co-founder.
You do not need a free weekend.

What you need: a clear idea, the willingness to think it through, and about $20/month.

That said — and I mean this — getting something working is not the same as getting
something right. A prototype that runs is a starting point, not a finish line.
At some point, especially if real people are going to use your app and rely on it,
you want technical eyes on it. Someone who can check whether it's secure, whether
it handles edge cases, whether it scales, whether it does what you think it does
under the hood.

The good news: not having those skills is no longer a reason to never start.
Knowing when to bring them in — and being humble enough to recognize that moment —
is the important part.

This guide gets you to a real, working first version. Eyes open.

---

## The tools (and what they cost)

| Tool | What it does | Cost |
|---|---|---|
| **Perplexity Computer** | Your AI co-pilot — browses the web, writes and runs code, manages files, deploys apps. Works on desktop and mobile. | ~$20/month |
| **Claude Code** (via Anthropic API) | The heavy-lifting code builder, called automatically during the build. You don't interact with it directly — Perplexity handles that. | Pay-as-you-go — start with $20–50 in credits |
| **GitHub** | Stores your code safely in the cloud. Every change tracked. Rollback if something breaks. | Free |
| **Railway** | Hosts and runs your app live on the internet. Connects to GitHub — push code, app updates automatically. | Free tier / ~$5/month for always-on |

**Realistic total to launch something real: $20–75.**

The Anthropic API credits are the variable. Think before you build and you won't
burn through them. More on that below.

---

## Phase 1 — Think before you build

> The most important phase. And the cheapest. Do not skip it.

The most common mistake: jumping straight into building before the idea is solid.
If you're vague going in, the AI will build you something vague. It is remarkably
good at confidently building the wrong thing if you let it.

**Do this phase outside of Claude Code.** Use Perplexity Computer on your phone,
Claude.ai, ChatGPT — whatever. These conversations are cheap or free.
Claude Code burns API credits, and you don't want to spend them figuring out
what you're making.

You can do all of Phase 1 on your phone. In a waiting room. On a walk.
That's where most of VetAssist came from.

### Have a real conversation with AI about your idea

Talk it out. Voice-to-text. Screenshot your sketches. Think out loud.
Ask it to disagree with you.

Work through these — not as a form to fill out, as a conversation:

- **What problem does this solve?** Specific beats general every time.
- **Who is it for?** Name one real person. What's their actual frustration?
- **What does it do, step by step?** Walk through it out loud like you're showing someone.
- **What does it NOT do?** This one matters as much as the above.
- **What's the smallest version that proves the idea works?** That's your MVP. Build that first.
- **Does it touch anything sensitive?** Personal data, health info, financial info —
  flag it now. Doesn't stop you, just changes what you need to think about.

Push the AI on your idea:
- "What are the holes in this?"
- "What would a skeptical user say?"
- "What's the riskiest assumption I'm making?"
- "Where could this go wrong?"

### Write a one-page brief

Before you move to Phase 2, write a short summary. Informal is fine:

- What the app does (2–3 sentences)
- Who it's for
- The main flow, step by step
- What it does NOT do
- The simplest first version
- Any known risks or sensitivities

This becomes the brief you hand to the AI when building starts. The better it is,
the less back-and-forth you'll need, and the fewer credits you'll burn.

---

## Phase 2 — Set up your tools (one time)

Do these once. Never again.

**1. GitHub** — [github.com](https://github.com). Free. Sign up.
Think of it as a safe deposit box for your code with full version history.
If something breaks, you go back. If a collaborator wants to review your code, this is where they look.

**2. Perplexity Computer** — [perplexity.ai](https://perplexity.ai). Subscribe.
This is your main interface for everything, desktop and mobile.

**3. Anthropic API key** — [console.anthropic.com](https://console.anthropic.com).
Create an account, add $20–50 in credits. Keep the key private — do not share it,
do not post it anywhere. Ever.

**4. Railway** — [railway.app](https://railway.app). Sign up with your GitHub account.
When you push new code, your live app updates automatically. No manual steps.

---

## Phase 3 — Build it

Now Perplexity Computer and Claude Code work together. You direct.

### Hand over your brief

Start a conversation with Perplexity Computer. Paste your one-page brief. Say something like:

> "I want to build this app. Here's what it does, who it's for, and what the
> first version needs. I'm not a developer — I'll be directing and reviewing,
> you handle the building."

From here it will ask clarifying questions, write the code, test things, and explain
decisions. Your job: review what it shows you, flag when something's wrong, stay engaged.

While you're living your life, it's doing the work in the table above.

### Reviewing without knowing how to code

You don't need to understand every line. You need to ask:
- Does this do what I asked?
- Does it behave the way a real user would expect?
- Is there anything here I don't understand that I probably should?

If you can't get a plain-language explanation of a decision, ask it to simplify.
Complexity you don't understand is complexity you can't stand behind.

### Test it like a real user

Use the thing. Walk the full flow. Try weird inputs. Use it on your phone.
Ask "what happens if someone does X?" Report what you find. It fixes things.

### On security and sensitive data

If your app touches anything personal — names, health data, financial data,
anything you wouldn't want leaked — raise it explicitly during the build:
- "Is this stored securely?"
- "Can one user access another user's data?"
- "What happens if someone tries to abuse this?"

The AI addresses what you ask. It doesn't always volunteer every concern unprompted.
That's exactly why technical review matters later.

---

## Phase 4 — Deploy it

**Push to GitHub** — Perplexity Computer handles this entirely. You don't touch the command line.

**Connect Railway** — link your Railway project to your GitHub repo. Done once.
Every future push auto-deploys. You get a live URL you can share with anyone.

That's it. Your app is on the internet.

---

## Phase 5 — Don't stop at "it works"

Working is the beginning, not the end.

Once real people use your app — or once you're seriously thinking about that —
bring in technical perspective. Ask someone to look at it who can tell you:

- Is this actually secure?
- What breaks under unusual conditions?
- Will this hold up if more people use it than I planned for?
- Does it do what I think it does in every case that matters?

You don't hand the project over. You get a second set of eyes.

If you're at Wilcore — you work with engineers. Ask one. An hour of their time
on a quick review is worth more than you'd expect.

**Technical people reading this:** the same principle applies in reverse.
You can build faster now than ever before. But fast and correct are still different things.
Use these tools to accelerate — not to skip the thinking.

---

## When to redeploy or restart on Railway

| Situation | What to do |
|---|---|
| Pushed new code to GitHub | Nothing — auto-deploys in ~60–90 seconds |
| Changed a Railway environment variable | Auto-redeploys when you save |
| App seems frozen or stuck | Railway dashboard → Deployments → Restart |
| Browser showing old version | Hard refresh: `Cmd+Shift+R` Mac / `Ctrl+Shift+R` Windows |

---

## What this costs

| Item | Cost |
|---|---|
| Perplexity Computer | ~$20/month |
| Anthropic API credits (first build) | $20–50 one-time |
| GitHub | Free |
| Railway | Free tier / ~$5/month always-on |
| **Total to ship something real** | **~$20–75** |

---

## The mindset

You are the product owner. The AI is the engineering team.
Technical review is your quality gate.

A few things that actually helped:

- **Talk to it like a colleague.** Push back. Ask why. You'll build better things
  and learn more about what you're building in the process.
- **Iterate in small steps.** One thing working is better than five things halfway done.
- **Use your phone.** Voice-to-text, photos of sketches, screenshots of things you
  want to reference. I built the entire POC — start to finish — on my phone. Chores,
  waiting rooms, Lyft rides, the playground. The desktop only came out for the
  presentation. That's not a flex — that's the point.
- **Don't panic when things break.** They will. That's Tuesday. Tell the AI what
  happened, it fixes it.
- **Think before you burn credits.** Phase 1 is free. Use it. Clarity going in
  means less rework, less cost, better output.
- **Stay humble about what you don't know.** Running doesn't mean right.
  Safe. Secure. Correct under all conditions. Those still require judgment —
  and often, someone else's.

---

## Go build the thing

Most people stay stuck at "I wish someone would build something that..." —
assuming the gap between idea and reality is bigger than it is.

It isn't. Not anymore.

You can start today. On your phone. Between whatever is happening in your life.
You can have something real running in a weekend — or, honestly, in a few hours
of stolen time across a couple of days.

The app this guide was written around is live at
**[vetassist-production.up.railway.app](https://vetassist-production.up.railway.app)**.
Go use it. Then come build your own.

Questions, thoughts, want to talk through your idea? Reach out to me directly —
I'm happy to help you think it through.

---

*Written in my own voice, on my phone, as a deliberate test case of what's possible
right now with these tools. The entire build — from first idea to working POC — was done
on my phone. Chores, waiting rooms, Lyft rides, the playground. The desktop only
came in for the presentation. A veteran friend tested the finished product on my phone
while our kids played.*

*That's the bar. You can clear it.*
