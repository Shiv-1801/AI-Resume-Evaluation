# I used three AIs to optimize my resume. They can't agree on what "good" even means.

### And if you can't see which AI is screening you, optimizing for one of them is a coin flip

---

I finally gave in and decided to use AI to "optimize" my resume for every future application.

Not wanting to take any chances, I built my resume from the ground up on three different models to maximize the "optimization." Claude, ChatGPT, and Gemini, free versions of all three.

Then I ran a small test.

Once all three versions were built, I made a fresh account on each platform (so none of them carried any prior context about me), uploaded all three resumes to all three, and gave every model the same prompt:

> "Of these 3 resumes, which would you choose for a Market Intelligence Analyst role?"

Every model picked its own.

Claude picked the Claude resume. Its reason: it "opens with the strongest MI credential first."

ChatGPT picked the ChatGPT resume. Its reason: it "reads like someone who actually does Market Intelligence."

Gemini picked the Gemini resume. Its reason: it "aggressively curates the candidate's experience."

(Screenshots and full transcripts are in the repo linked at the bottom, if you want to check I'm not making this up.)

## The problem

Each model is pattern-matching to its own output style and calling that quality.

That is not stylistic variation. That is a different definition of "good."

Claude thinks a strong resume leads with evidence. ChatGPT thinks it should read like someone already native to the role. Gemini thinks it should ruthlessly cut anything off-target. Three models, three theories, and each one graded the other two against its own theory and found them wanting.

## Why this actually matters

Here is the part that turned this from a curiosity into something I would tell other applicants.

ATS vendors don't disclose which foundation model powers their screening layer. Some use proprietary ranking systems. Some use fine-tuned LLMs. Some still run older NLP pipelines that predate this entire generation of models. When you hit "apply," you have no way of knowing which one is reading you.

So if you optimize your resume for ChatGPT's preferences, and the company you are applying to runs an ATS built on a different model with a different theory of "good"... you may have optimized for the wrong target entirely.

Using AI to beat an AI-powered ATS assumes you know which AI you are beating. Most of the time, you don't.

That is the whole trap. The optimization feels rigorous, and it does produce a cleaner resume. But the confidence it gives you is borrowed from a judge who may not even be in the room.

## The part that's actually useful

It wasn't all a wash.

Claude and ChatGPT, with no access to each other's answers, both said the best resume would be a hybrid. And they converged on nearly the same recipe.

Both said: take Claude's opening sentence, build ChatGPT's experience architecture around it, and apply Gemini's curation logic, drop the social media metrics and strip the marketing noise.

Two models that had just disagreed about the winner quietly agreed on the fix. When that happens, the agreement is worth more than either verdict was.

## One caution about trusting even that

The agreement isn't gospel either.

Both Claude and ChatGPT flagged one number in Gemini's resume, "8,800+ job postings," as a round-number credibility risk. Both told me to cut it.

They were wrong. That number is real. It is my first scrape of 4,949 postings plus a later one I called the August Update, roughly 3,897 more, and both are sitting in my public project repo. The profile I gave the models only mentioned the first number, so two reviewers saw a big round figure they couldn't verify and told me to drop my most complete, most honest stat.

That one stuck with me. A reviewer without your receipts will flag your best real number. Context you leave out of the document becomes a liability, even when you are right. And two AIs agreeing on something doesn't make it true. It just makes it worth checking.

## Where this leaves us

None of this is really the models' fault. It is the black box.

The candidate can't see which AI is judging them, so they optimize blind. The hiring team gets a flood of resumes shaped by whichever chatbot each applicant happened to trust. Neither side actually knows what the other is optimizing for.

Lack of transparency in the hiring process creates friction for everyone in it, the candidate and the hiring team both. I don't have a clean fix for it. But I would rather apply knowing I am guessing than apply thinking a chatbot handed me a sure thing.

---

*The full experiment is public if you want to check my work: every prompt, all three resumes, all three model transcripts, and the LinkedIn profile I started from. [github.com/Shiv-1801/AI-Resume-Evaluation](https://github.com/Shiv-1801/AI-Resume-Evaluation)*
