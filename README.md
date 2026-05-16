# Humanizer

> Humanize AI text. Make your prose sound like a human wrote it, not a machine. A Claude Code skill that teaches the feel of real writing, no banned-word list.

While using AI day in and day out for almost everything in the last couple of years, the writing started bothering me in a way I couldn't shake. Every paragraph reads the same. Same hedged framing, same closing line about a bright future, same "on one hand, on the other hand" balance, etc... and once you notice it, you can't read AI text the same way again. It feels boring. It feels assembled. You don't feel like there is a person on the other side of the page.

I tried the humanizer skills that already exist, and honestly, they didn't fix it for me. They all work the same way: a list of banned words, a stack of before-and-after templates, and a hope that the swap-out will make the writing sound human. It doesn't. The AI just dodges the listed words and the prose still reads like an output, because nothing underneath actually changed.

So I built this one, and the approach is different. Instead of giving Claude a list of words to avoid, this skill teaches him what human writing actually feels like, deep enough that he can catch the AI-ness anywhere it shows up. Even in places nobody wrote down in a catalog. The whole thing rests on one idea: human writing trusts the reader, AI writing doesn't.


## Install

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/spuvr/humanizer.git ~/.claude/skills/humanizer
```

That's it. Claude Code picks it up automatically the next time you start a session.

For other tools that read Claude skills (Anti Gravity, OpenCode, and similar agent frameworks), drop the folder into the equivalent skills directory for that tool. The skill is just a SKILL.md file with frontmatter, no platform-specific code, so it travels.


## How to use it

The most basic use is just asking.

```
Humanize this text:
[paste your text]
```

If you want the rewrite to sound like you specifically, pass in a sample of your own writing as a voice reference.

```
Humanize this paragraph. Match the voice of this sample:
[your writing here]

And here is the text to rewrite:
[paste your text]
```

You can drop in pretty much anything: an article draft, a LinkedIn post that came out of ChatGPT, a paragraph in a doc that feels off, an essay, a cover letter, etc... The skill takes over from there.


## What the skill actually catches

A small slice of the patterns the skill recognizes, why each one is a tell, and what a human does instead.

| What AI writes | Why it sounds AI | What a human does |
|---|---|---|
| "It's worth noting that..." | Padding to sound thorough | Cuts it. The sentence already works. |
| "fast, flexible, and reliable" | Defaults to lists of three | Uses 2, 4, or 1. Breaks the cadence. |
| "It's not just X, it's Y" | Frames everything as a profound reframe | Just says Y |
| "Experts say..." | Vague authority, no real source | Names the source or drops the claim |
| Em-dashes everywhere ("—") | The model's versatile fallback | Uses commas, periods, parentheses, or a plain hyphen ("-") |
| "stunning, vibrant, breathtaking" | Brochure copy leaking through | Describes the thing instead of selling it |
| "Great question!" | Chatbot pleasantry leaking in | Deletes it. The piece starts at sentence one. |
| "The future looks bright" | Forced positive closer | Ends on something concrete |
| "On one hand, on the other hand" | Performing balance, avoiding stake | Has an opinion, or admits real uncertainty |
| "Despite challenges, X thrives" | Wikipedia template | Drops the section if there are no real challenges |
| "In a world where..." | Reaching for grand framing | Starts with the thing itself |
| "reflecting the community's deep connection..." | Tacked-on "-ing" tail for fake depth | Ends the sentence at the real fact |

The full catalog is in [SKILL.md](SKILL.md), along with everything underneath about rhythm, flow, voice, specificity, and what human writing actually feels like.


## Before and after, so you can feel the gap

Three paragraphs pulled straight from the benchmark, each written about the same topic with the same factual references. The only thing that changed was whether the humanizer skill was loaded.

**Why we yawn, without the humanizer skill:**

> Yawning is one of the most common human behaviors, and yet scientists still cannot fully explain why we do it. The old idea that yawning boosts oxygen intake has largely been disproved by research. The leading current theory is that yawning helps regulate the temperature of the brain by drawing in cooler air and increasing blood flow to the head. Yawning is also contagious in humans and in some animals such as dogs and chimpanzees, and that contagion appears to be linked to empathy. Most of us start yawning before we are even born, since ultrasounds have captured fetuses yawning in the womb, and unusually frequent yawning can sometimes point to sleep disorders, heart problems, or certain neurological conditions.

**Why we yawn, with the humanizer skill:**

> Yawning is one of those things everyone does and nobody can quite explain. The oxygen theory, the one your gym teacher told you, has mostly fallen apart under testing. The current best guess is temperature regulation, that pulling cool air in and bumping blood flow helps cool the brain a little. The contagious part is stranger. It catches in humans, in dogs, in chimps, and the people who catch it most readily tend to score higher on empathy measures. Fetuses yawn in the womb, caught on ultrasound months before they breathe air. And if you find yourself yawning constantly for no reason, that can point at a sleep disorder, a heart issue, something neurological worth asking about.

Same facts. The first reports them in textbook order. The second hooks you with "everyone does and nobody can quite explain," then plants you in a memory ("the one your gym teacher told you") and overturns it. You actually read the whole thing.

Another one, on the fall of the Berlin Wall.

**Without the humanizer skill:**

> The Berlin Wall stood from 1961 to 1989, dividing East and West Berlin after East Germany built it to stop its citizens from fleeing westward. On the evening of November 9, 1989, an East German official named Günter Schabowski mistakenly told a press conference that travel restrictions would be lifted immediately. Hearing the news, East Berliners flocked to the border crossings, and the overwhelmed guards eventually gave up and opened the gates. Crowds from both sides climbed onto the wall together, celebrating and chipping off pieces as souvenirs. The collapse of the wall set off a rapid unravelling of communist governments across Eastern Europe and led to the reunification of Germany on October 3, 1990.

**With the humanizer skill:**

> The wall went up in 1961 to keep East Germans from walking west, and it came down on the evening of November 9, 1989, because a man read a note wrong. Günter Schabowski, an East German official, was handed new travel rules at a press conference, didn't quite understand them, and when a reporter asked when they took effect he said "immediately." East Berliners heard him on the news and walked to the checkpoints. The guards had no orders, no script, and eventually no choice; they opened the gates. People climbed on top of the concrete with hammers and chisels, working off pieces while strangers from both sides drank together in the cold. Within a year the other communist governments in the region had folded, and Germany was one country again on October 3, 1990.

The baseline gives you "mistakenly told a press conference" and "chipping off pieces as souvenirs." The humanizer version gives you "because a man read a note wrong" and "strangers from both sides drank together in the cold." Same facts, completely different relationship to the reader.

One more, this time something technical. How vinyl records work.

**Without the humanizer skill:**

> A vinyl record stores sound as a single continuous spiral groove cut into the surface of the disc, with tiny side-to-side and up-and-down wiggles that mirror the shape of the original sound waves. When the record spins, a stylus rests in the groove and vibrates with those wiggles, and a cartridge converts the motion into an electrical signal using either a coil-and-magnet system or a piezoelectric element. That signal is then amplified and sent to the speakers. Albums typically play at 33⅓ RPM, singles at 45 RPM, and older shellac records at 78 RPM. Because the groove represents the sound wave continuously rather than as a series of discrete samples, vinyl is considered an analog format, in contrast to CDs and other digital audio.

**With the humanizer skill:**

> A record is a single spiral groove cut into the disc, and the wiggles in that groove, side to side and up and down, are the sound wave itself, drawn in plastic. The stylus drops in and shakes as the record turns. A cartridge picks up that shaking with a magnet and a coil, or with a piezo crystal, turns it into a tiny electrical signal, and the amp takes it from there. 33 and a third for an album, 45 for a single, 78 for the old shellac stuff your grandparents had. The whole thing is analog, which means the wave is right there as one continuous shape, not the stairstep of samples a CD uses.

The baseline spends three full sentences on the physical groove and never lets you see it. The humanizer version says "the sound wave itself, drawn in plastic" and the whole mental model lands in one line.


## The benchmark, because I didn't want to just claim it works

I didn't want to just say this skill is good, I wanted to actually test it. So I ran two separate benchmarks with three agents each. Two agents wrote without the humanizer skill loaded (baselines), and a third agent wrote with the skill loaded. All three agents got identical topics and identical factual references. The only thing that changed was the skill.

Round 1 covered the invention of paper, how airplane wings generate lift, why we yawn, and the fall of the Berlin Wall. Round 2 covered the history of pizza, how vinyl records work, why flamingos are pink, and the Great Pyramid of Giza.

In both rounds, the two baseline agents converged hard. They produced almost the same paragraph for each topic, using the same hedged framing and the same neutral closers. The convergence itself is the tell. It is what AI prose looks like when you sample it twice.

The humanizer agent broke pattern on every single topic. It opened in concrete moments ("Pizza didn't start as anything special," "The wall went up in 1961 to keep East Germans from walking west"). It reached for specific images the baselines never grabbed for ("the sound wave itself, drawn in plastic," "the only one you can still walk up to"). It varied rhythm. It had a voice.

Full output is in [BENCHMARK.md](BENCHMARK.md) for round one and [BENCHMARK-2.md](BENCHMARK-2.md) for round two. 24 paragraphs side by side. Judge for yourself.


## What reading AI feels like versus what reading human writing feels like

Reading AI text feels like reading the same person paraphrasing themselves over and over. The cadence is even, the framing is balanced, the closer is positive in a way that doesn't commit to anything, etc... You read it and you understand it, but nothing in it touches you. It doesn't feel like there is anyone on the other side. It is technically writing, but it does not feel like communication.

Reading human writing feels different in a way that is hard to put into words until you sit with it. There is a person there. They have an opinion. They are a little annoyed, or a little amused, or genuinely uncertain about something, and you can feel it. They reach for specific images and concrete numbers because those are the things they actually know. They leave space in the prose for you to land in your own head. They trust you. You read all the way through, from the first sentence to the last, because each sentence is doing work and pulling you forward instead of restating what came before.

This skill is built to give you back that second kind of reading experience, even when the writer happens to be an AI.


## Why I built this

Honestly, after years of using AI for everything, I just wanted to be able to read what it gives me without zoning out. I wanted to chat with an AI and feel like I'm chatting with a friend, where I actually want to read the whole message from the first sentence to the last, not skim it because it feels generic. That feeling, the feeling that there is somebody on the other end of the words, is what most AI text is missing, and it is what this skill is built to put back.

It is not finished. AI writing is a moving target, and new tells show up as the models change. The pattern catalog inside SKILL.md is a starter, not a closed set. If you find a pattern the skill doesn't catch, open an issue or a pull request, and we will add it. The catalog grows over time. The underlying principle (trust the reader) doesn't change.


## How this skill was written

The skill itself follows the philosophy it teaches. No banned-word list. No find-and-replace templates. No checklist energy. Examples are used as direction, not as a cage. If reading SKILL.md feels like it is hand-holding you, that is a bug, and the file needs another pass.


## Sponsor

If this skill saves you time or just makes reading AI text a little less painful, you can sponsor me on GitHub here: [github.com/sponsors/spuvr](https://github.com/sponsors/spuvr). Completely optional, no pressure, but always appreciated.


## License

MIT. Use it however you want, modify it, fork it, ship it inside your own projects, etc... Credit is appreciated but not required.


## Tags

humanize ai text, ai writing humanizer, claude code skill, anthropic skill, remove ai tells, ai writing patterns, make ai sound human, chatgpt humanizer, llm writing style, prose editing, ai content editor, ai text rewriter, humanize chatgpt, natural writing, writing assistant
