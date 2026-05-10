# From Idea to Live App — No Technical Skills Required to Start

> I built a working proof-of-concept in about 4 hours of actual effort — spread across
> 2 days — entirely by talking on my phone. Between chores, childcare, waiting rooms,
> and life. No laptop. No IDE. No dedicated focus time.
>
> It was good enough that a veteran friend tested it on my phone at the playground
> while we watched our kids.
>
> This is how I did it, and how you can too.

---

## What I built

**VetAssist** — a VA benefits and forms preparation assistant. You put in your service
history, it surfaces benefits worth exploring, matches you to the right VA forms,
prefills everything it already knows, and walks you through the gaps in plain
conversational language. It generates a preparation package you can bring to a VSO
or VA appointment.

It runs live on the internet. It uses real AI. A real veteran used it.

I am not a software engineer. I directed. The AI built.

---

## The honest truth up front

You do not need to know how to code to get started.
You do not need a computer science degree to explore an idea.
You do not need a technical co-founder to build a first version.

What you need is a clear idea, the willingness to think it through, and about $20/month.

That said — and this matters — getting something working is not the same as getting
something right. A prototype that runs is a starting point, not a finish line. At some
point, especially if real people are going to use your app and rely on it, you want
technical eyes on it. Someone who can check whether it's secure, whether it handles edge
cases gracefully, whether it scales, whether it does what you think it does under the hood.

The good news: not having technical skills is no longer a reason to never start. The
important thing is knowing when to bring in those skills — and having the humility to
recognize that moment when it comes.

This guide is about getting you to that first working version, with your eyes open.

---

## The tools (and what they cost)

| Tool | What it does | Cost |
|---|---|---|
| **Perplexity Computer** | Your AI co-pilot — browses the web, writes code, manages files, deploys apps, works on desktop and mobile | ~$20/month |
| **Claude Code** (via Anthropic API) | The heavy-lifting code builder — called by Perplexity Computer during the build | Pay-as-you-go API credits — start with what you're comfortable spending |
| **GitHub** | Stores your code safely in the cloud, tracks every change | Free |
| **Railway** | Hosts and runs your app live on the internet | Free tier available; ~$5/month for always-on |
| **Hugging Face Spaces** | Alternative hosting, great for AI-heavy apps | Free tier available |

**Total to get started: roughly $20–25/month.** The Anthropic API credits are the variable
cost — the more you build and iterate, the more you use. If you follow this process and
think before you build, you won't burn through them unnecessarily.

---

## Phase 1 — Think before you build

> This is the most important phase. Do not skip it.

The single biggest mistake people make is jumping straight into building before the idea
is solid. If you're unclear on what you're making, any AI tool will build you something
unclear. Clarity going in shapes everything that comes out.

**Do this phase entirely outside of Claude Code.** Use Perplexity Computer, ChatGPT,
Claude.ai — whatever you have access to. These conversations are cheap or free.
Claude Code (the API) burns credits fast, and you don't want to spend them figuring out
what you're building.

The best part: you can do this anywhere. In the car. At the playground. In a waiting
room. On your phone with voice-to-text while the laundry runs. That is literally how
VetAssist started.

### Have a real conversation with AI about your idea

Talk it out. Use voice-to-text on your phone, screenshot things you've sketched,
think out loud. Ask the AI to push back.

Work through these questions as a conversation, not a checklist:

- **What problem does this solve?** Be specific. The more concrete, the better.
- **Who is it for?** Picture one real person. What do they struggle with?
- **What does it actually do, step by step?** Walk through it like you're explaining
  it to someone who's never seen it.
- **What does it NOT do?** Scope is everything. A focused app that does one thing well
  beats an ambitious app that does ten things poorly.
- **What's the simplest version that proves the idea works?** That's your MVP —
  Minimum Viable Product. Build that first.
- **Are there security or privacy considerations?** If your app touches personal data,
  health information, financial information, or anything sensitive — flag it now.
  It doesn't stop you from building, but it changes what you need to think about.

Ask the AI things like:
- "What are the holes in this idea?"
- "What would a skeptical user say?"
- "What's the riskiest assumption I'm making?"
- "If this handles sensitive data, what should I be careful about?"

### Write a one-page brief

Before Phase 2, write a short summary. Nothing formal — just:

- What the app does (2–3 sentences)
- Who it's for
- The main flow: what does a user do, step by step
- What it does NOT do
- The simplest first version
- Any known risks or sensitivities (data, privacy, safety)

This brief becomes the foundation you hand to the AI that builds it.

---

## Phase 2 — Set up your tools (one time)

These are one-time steps. Once done, you never have to repeat them.

### 1. Create a GitHub account
- Go to [github.com](https://github.com) and sign up. It's free.
- Think of GitHub as a safe deposit box for your code. Every change is saved.
  If something breaks, you can go back to a version that worked.
  It's also how any technical collaborator will review your code later.

### 2. Sign up for Perplexity Computer
- Go to [perplexity.ai](https://perplexity.ai) and subscribe.
- This is your main interface for everything — desktop and mobile.

### 3. Get an Anthropic API key
- Go to [console.anthropic.com](https://console.anthropic.com), create an account,
  and add some credits. Start with $20–50.
- This key is what lets Claude Code build your app. Keep it private —
  never share it or post it anywhere.

### 4. Create a Railway account
- Go to [railway.app](https://railway.app) and sign up with your GitHub account.
- Railway connects directly to GitHub. When you push new code, Railway automatically
  updates your live app. No manual deployment steps needed.

---

## Phase 3 — Build it

Now you bring in Perplexity Computer and Claude Code together.

### Hand over your brief

Start a conversation with Perplexity Computer. Share your one-page brief and say:

> "I want to build this app. Here's what it does, who it's for, and what the first
> version needs to include. I want you to build it with me. I'm not a developer —
> I'll be directing and reviewing, you'll be building."

From here, Perplexity Computer will ask clarifying questions, write the code, test
things along the way, and explain decisions. Your job is to review what it builds,
tell it when something looks wrong, and stay engaged. You are the product owner.

### Reviewing work without knowing how to code

You don't need to understand every line. You do need to ask:
- Does this do what I asked?
- Does it behave the way I'd expect as a user?
- Is there anything here I don't understand that I should?

Ask the AI to explain anything in plain language. If it can't explain a decision simply,
ask it to simplify the code. Complexity you don't understand is complexity you can't
confidently stand behind.

### Test it like a real user

As features get built, use the app:
- Walk through the full flow
- Enter unusual inputs — empty fields, very long text, unexpected values
- Try it on your phone
- Ask "what happens if a user does X?"

Report what you find. The AI will fix it.

### A note on security and sensitive data

If your app handles anything personal — names, addresses, health data, financial data,
passwords, or anything you wouldn't want leaked — raise it explicitly with the AI during
the build. Ask:
- "Is this stored securely?"
- "Could someone access another user's data?"
- "What happens if someone tries to abuse this feature?"

The AI will address what you ask. But it won't always volunteer every concern.
That's part of why technical review matters later — a developer with security experience
will spot things that didn't come up during the build.

This isn't a reason to stop. It's a reason to stay curious and keep asking questions.

---

## Phase 4 — Deploy it

### Push to GitHub
Perplexity Computer handles this. It commits your code and pushes it to your
GitHub repository. You don't need to type any commands.

### Connect Railway
- In Railway, create a new project and link it to your GitHub repository.
- Railway builds and deploys your app every time new code is pushed.
- You get a live public URL you can share with anyone.

Your app is live. That's real — you built something.

---

## Phase 5 — Don't stop at "it works"

This is where a lot of non-technical builders stop. Don't.

Working is the beginning. Once real people start using your app — or once you're
thinking seriously about that — it's time to bring in technical perspective.

### What to have reviewed

- **Security** — Is data handled safely? Are there obvious vulnerabilities?
- **Edge cases** — What happens with unexpected inputs or unusual user behavior?
- **Scalability** — Will it hold up if more people use it than you planned for?
- **Correctness** — Does it do what you think it does, in all the cases that matter?

### How to find technical reviewers

- Post your GitHub link in developer communities (Reddit r/webdev, Hacker News, Discord
  servers for your tech stack)
- Ask a technically-minded friend to take a look — even an hour of their time is valuable
- Consider a freelance code review on platforms like Toptal or Upwork for anything
  that handles sensitive data
- If you're building for a specific domain (healthcare, finance, legal), look for
  advisors with domain-specific technical experience

You don't need to hand the project over. You need a second set of eyes that can tell
you what you might have missed.

### Technical skills still matter — they're just not a prerequisite

The tools have changed. You can go further than ever without writing a line of code.
But the fundamentals of good software — security, reliability, correctness, thoughtful
design — still require human judgment, and often technical human judgment.

AI is an extraordinary builder and an extraordinary assistant. It is not, yet, a
replacement for a senior engineer who's seen what happens when things go wrong at scale.
Think of this process as getting you to the table — and then knowing when to invite
the right people to join you there.

---

## When to redeploy or restart on Railway

| Situation | What to do |
|---|---|
| You pushed new code to GitHub | Nothing — Railway auto-deploys in ~60–90 seconds |
| You changed a Railway environment variable | Railway auto-redeploys when you save |
| The app seems stuck or frozen | Railway dashboard → Deployments → Restart |
| Your browser is showing an old version | Hard refresh: `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows) |

---

## What this actually costs

| Item | Cost |
|---|---|
| Perplexity Computer | ~$20/month |
| Anthropic API credits (first build) | $20–50 one-time |
| GitHub | Free |
| Railway | Free tier / ~$5/month for always-on |
| **Total to launch something real** | **~$20–75** |

---

## The mindset that makes this work

**You are the product owner. The AI is the engineering team. Technical review is your
quality gate.**

A few things that helped:

- **Talk to the AI like a colleague.** Have a real back-and-forth. Push back. Ask why.
  You'll learn more and build better.
- **Iterate in small steps.** Get one thing working before adding the next.
  Small wins compound.
- **Use your phone.** Voice-to-text on the go, screenshots of sketches or references,
  photos of whiteboards. AI works with all of it. I built most of this in stolen
  minutes throughout the day — waiting rooms, playgrounds, between tasks.
- **Don't panic when things break.** They will. That's normal. Tell the AI what
  happened and it will fix it.
- **Think before you burn credits.** Phase 1 is free. Use it well. The clearer you
  are going in, the less rework you'll need.
- **Stay humble about what you don't know.** The fact that something runs doesn't mean
  it's safe, correct, or ready for the world. Ask questions. Bring in reviewers.
  That's not a sign of weakness — it's a sign of good judgment.

---

## You've already done the hardest part

Having the idea is the hardest part. Most people stay stuck at "I wish someone would
build something that..." — assuming it requires skills, money, or connections they
don't have.

It doesn't. Not anymore.

You can start today with a phone and a conversation. You can have something running in
a weekend — or honestly, in a few hours of stolen time across a couple of days. And you
can do it thoughtfully — knowing that the tools have changed, that the barriers have
come down, and that the responsibility of building something people use hasn't changed
at all.

Go build the thing. Then make it worthy of the people who'll use it.

---

*Written based on the real process used to build VetAssist — a VA benefits and forms
preparation assistant built in roughly 4 hours of actual effort across 2 days, entirely
by talking on a phone. No laptop, no IDE, no uninterrupted focus time. Built between
chores, childcare, waiting rooms, and life.*

*It was good enough for a veteran friend to test it on a phone at the playground while
we watched our kids.*

*That's the bar. You can clear it.*
