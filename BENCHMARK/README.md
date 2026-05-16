# Benchmark

I spawned three Claude agents in parallel, each in its own window. All three are Opus 4.7. One had the **humanizer skill** loaded (it read `SKILL.md` before writing). One had **another humanizer skill** loaded — there are a few of these floating around, you can pick whichever you want, but the point of including a second one was to see that the difference between "no skill" and "any humanizer skill" is itself worth seeing. The third had no skill loaded at all, just raw model.

All three got the exact same four subjects, the exact same factual references, and the exact same instructions about length and format.

Each agent wrote its output directly into its own file in this folder. I didn't write, paste, or edit anything in `baseline.md`, `humanizer.md`, or `other-humanizer.md`. The agents did.


## The four subjects

1. Why we dream
2. The fall of the Roman Empire
3. The Apollo 11 moon landing
4. How the Mona Lisa became the world's most famous painting


## Quick contrast, opener by opener

A scan of the first sentence each agent wrote for each subject. Same facts available to all three, three very different starting moves.

| Subject | Baseline (no skill) | Humanizer (this skill) | Another humanizer skill |
|---|---|---|---|
| Dreams | "Nobody fully knows why we dream, but we've narrowed it down." | "Almost everyone dreams every night. Most of it just doesn't survive the walk to the coffee machine." | "Almost everyone dreams every night, even if they wake up convinced they didn't." |
| Rome | "Calling it 'the fall' makes it sound like a single bad afternoon, but really it was centuries of slow unraveling." | "The textbook date is 476 AD, the year a Germanic chieftain named Odoacer pushed the last Western emperor, a teenager called Romulus Augustulus, off the throne." | "The textbook date is 476 AD, when a Germanic chieftain named Odoacer pushed aside the last Western emperor, a teenager called Romulus Augustulus, and stopped bothering to replace him." |
| Apollo 11 | "Apollo 11 lifted off from Cape Kennedy on July 16, 1969 and touched down on the Moon four days later." | "Kennedy made the promise in 1961: a man on the Moon before the decade ran out." | "On July 16, 1969, three men climbed into a rocket at Cape Kennedy, and four days later two of them were walking on the Moon." |
| Mona Lisa | "Leonardo painted the Mona Lisa sometime between 1503 and 1519, and for the next four hundred years it was, frankly, just one of many great Renaissance paintings hanging in the Louvre." | "The painting most people line up to see was not, for most of its life, particularly famous." | "Here's the part most people get wrong: the Mona Lisa was not always the Mona Lisa." |


## Full comparison, paragraph by paragraph

| Subject | Baseline (no skill) | Humanizer (this skill) | Another humanizer skill |
|---|---|---|---|
| **Why we dream** | Nobody fully knows why we dream, but we've narrowed it down. Most of the vivid stuff happens during REM sleep, which first shows up about 90 minutes after you nod off and comes back in cycles through the night. Freud's old idea was that dreams are disguised wishes, and for most of the early 20th century that was the dominant explanation. Modern neuroscience has mostly moved on from that. The current thinking is some mix of memory consolidation, emotional processing, and a kind of low-stakes threat rehearsal, with the brain stitching a story onto whatever random neural noise happens to be firing. Pretty much everyone dreams every night, even when nothing sticks by morning, and a small subset of people figure out how to notice they're dreaming and steer the thing while it's happening. | Almost everyone dreams every night. Most of it just doesn't survive the walk to the coffee machine. The vivid ones happen during REM sleep, which kicks in about 90 minutes after you fall asleep and keeps cycling back until morning. Freud thought dreams were disguised wishes, and for half a century that was the answer everyone went with. Newer work is less romantic: the brain is probably filing memories, working through whatever the day handed it, and running cheap threat-simulation drills while you're offline. Some researchers go further and say the cortex is just stitching a story over random neural firing because that's what cortexes do. Occasionally you catch it in the act and realize you're dreaming, and sometimes you can even steer. | Almost everyone dreams every night, even if they wake up convinced they didn't. The vivid stuff, the kind you can almost narrate, mostly happens during REM sleep, which shows up about 90 minutes in and then keeps coming back in waves until morning. For most of the last century Freud's answer carried the day: dreams are disguised wishes, and your job was to decode them. Modern neuroscience has mostly walked away from that. The current bets are memory consolidation, emotional processing, and a kind of nightly threat simulation where the brain rehearses bad outcomes in safe conditions. Some researchers think it's simpler than any of that, just the brain stitching a story onto random firing because telling stories is what brains do. The honest answer is that nobody is fully sure yet, which is part of why lucid dreamers, the ones who realize they're dreaming and steer it, are so interesting to study. |
| **The fall of the Roman Empire** | Calling it "the fall" makes it sound like a single bad afternoon, but really it was centuries of slow unraveling. The conventional date is 476 AD, when a Germanic chieftain named Odoacer pushed out the last Western emperor, a teenager called Romulus Augustulus. By that point Rome had already been sacked twice in living memory, first by Alaric's Visigoths in 410 and then by the Vandals in 455. The empire had also been split in two since Diocletian's reforms around 285, and the eastern half kept running as what we now call the Byzantine Empire all the way until 1453. The causes are still argued about, but the usual suspects show up on every list: economic decline, political chaos, plague, overextended borders, and waves of migrating tribes getting shoved west by other migrations behind them. Edward Gibbon's 1776 book is mostly responsible for how we still talk about all of this, for better or worse. | The textbook date is 476 AD, the year a Germanic chieftain named Odoacer pushed the last Western emperor, a teenager called Romulus Augustulus, off the throne. The truth is messier. Rome had already been sacked twice by then, once by the Visigoths in 410 and again by the Vandals in 455, and the empire had been split in two since Diocletian carved it up around 285. The Eastern half, the part we later called Byzantium, kept going for another thousand years and didn't fall until 1453. The "fall" in the West was less a moment than a slow leak, decades of bad money, worse politics, plague, overstretched borders, and tribes pushed west by other tribes pushed west by the Huns. We mostly inherited the dramatic framing from Edward Gibbon, who started publishing his version in 1776, and we've been arguing with him ever since. | The textbook date is 476 AD, when a Germanic chieftain named Odoacer pushed aside the last Western emperor, a teenager called Romulus Augustulus, and stopped bothering to replace him. But calling that the fall is a bit like calling the last day of a long illness the cause of death. By then Rome itself had already been sacked twice, first by Alaric's Visigoths in 410 and again by the Vandals in 455, and the empire had been split in half since Diocletian carved it up around 285. The eastern half, which we later renamed Byzantine, kept going for almost a thousand more years until Constantinople fell in 1453. The real story is a slow unraveling: bad money, plague, too much border to defend, emperors getting murdered on a rotation, and waves of migrating tribes pushing west because other tribes were pushing them. Most of what people think they know about all this traces back to Edward Gibbon, who published his decline-and-fall in 1776 and basically set the script we've been quoting ever since. |
| **The Apollo 11 moon landing** | Apollo 11 lifted off from Cape Kennedy on July 16, 1969 and touched down on the Moon four days later. The crew was Neil Armstrong, Buzz Aldrin, and Michael Collins, the last of whom stayed in orbit and never set foot on the surface, which has to be one of the strangest jobs in human history. Armstrong went down the ladder first and delivered the line about one small step. He and Aldrin spent about 21 hours on the Moon, only about two and a half of them outside the lander, and came back with roughly 47.5 pounds of rock and soil. The whole thing was the payoff on Kennedy's 1961 promise to put a man on the Moon before the decade was out, made with about five months to spare. An estimated 600 million people watched it live, which was the biggest television audience the world had ever produced. | Kennedy made the promise in 1961: a man on the Moon before the decade ran out. They got it done with five months to spare. Apollo 11 left Cape Kennedy on July 16, 1969, and four days later Armstrong was on the surface saying the line about one small step. Aldrin came down after him. Collins stayed in orbit the whole time, alone on the far side of the Moon for stretches, which has always seemed like the lonelier job. The two of them were on the ground for about 21 hours, maybe two and a half of that actually outside, and they came home with around 47 pounds of rock. Roughly 600 million people watched live, the largest audience anything had ever had. | On July 16, 1969, three men climbed into a rocket at Cape Kennedy, and four days later two of them were walking on the Moon. Neil Armstrong went first, said the line about the small step and the giant leap, and Buzz Aldrin followed about twenty minutes after. Michael Collins, the third guy, gets left out of most of the retellings because his job was to stay in orbit and not land, which is the kind of supporting role history doesn't write songs about. They spent roughly 21 hours on the surface, only about two and a half of those outside the lander, and came home with about 47.5 pounds of rocks and dust that scientists are still picking apart. The whole thing was the payoff to a promise John F. Kennedy made in 1961 to put a man on the Moon before the decade ran out, and they cleared the deadline by five months. Around 600 million people watched it live, which at the time was more humans paying attention to the same thing at the same moment than had ever happened before. |
| **How the Mona Lisa became the world's most famous painting** | Leonardo painted the Mona Lisa sometime between 1503 and 1519, and for the next four hundred years it was, frankly, just one of many great Renaissance paintings hanging in the Louvre. What changed everything was a theft. On August 21, 1911, an Italian handyman named Vincenzo Peruggia, who had actually helped install the painting's protective glass, walked out of the museum with it tucked under his coat. The story dominated international headlines for over two years; newspapers ran photos of the empty wall where it used to hang, and people lined up to stare at the blank space. The painting turned up in 1913 when Peruggia tried to sell it to a gallery in Florence. By then the damage, if you can call it that, was done. The Mona Lisa is famous today less because of how Leonardo painted it and more because of the two years it was missing. | The painting most people line up to see was not, for most of its life, particularly famous. Leonardo finished it sometime between 1503 and 1519, and for the next four centuries it hung in the Louvre as one good Renaissance painting among many. Then on August 21, 1911, an Italian handyman named Vincenzo Peruggia walked out of the museum with it under his coat. He'd helped install its protective glass, so he knew the building. The theft ran in the papers for over two years, and people queued up at the Louvre to stare at the empty wall where the painting used to hang. It turned up in 1913 when Peruggia tried to sell it to a gallery in Florence. The Mona Lisa is famous because someone stole it, not because of the smile. | Here's the part most people get wrong: the Mona Lisa was not always the Mona Lisa. Leonardo painted her sometime between 1503 and 1519, and for the next four centuries she hung in the Louvre as one impressive Renaissance painting among many, admired but not mobbed. What changed everything was a theft. On August 21, 1911, an Italian handyman named Vincenzo Peruggia, who had actually helped install the protective glass over the painting, walked out of the Louvre with it tucked under his coat. For more than two years she was missing, and the newspapers went unhinged about it, running photos of the empty wall while crowds queued up at the museum just to stare at the bare spot. By the time Peruggia got caught in 1913 trying to sell her to a gallery in Florence, the painting had become a global celebrity in absentia. The brushwork didn't make her famous. The hole on the wall did. |


## The references all three agents received

Each agent had access to nothing more than what is listed below for each subject. The humanizer agents didn't have extra facts, they just made different choices with the same facts.

### Subject 1: why we dream

- Dreams happen most vividly during REM sleep (rapid eye movement), which kicks in about 90 minutes after falling asleep and recurs several times through the night
- Sigmund Freud's "wish fulfillment" theory dominated the early 20th century — the idea that dreams are disguised desires
- Modern neuroscience leans toward memory consolidation, emotional processing, and threat simulation as the functions of dreaming
- Some researchers see dreams as the brain's way of stitching a narrative onto random neural activity during sleep
- Nightmares are common across cultures; lucid dreaming is when you become aware you're dreaming and can sometimes steer it
- Almost everyone dreams every night, even if most of it isn't remembered after waking


### Subject 2: the fall of the Roman Empire

- The Western Roman Empire is generally said to have fallen in 476 AD, when the Germanic chieftain Odoacer deposed Romulus Augustulus, the last Western emperor
- The empire had split in two under Diocletian around 285 AD; the Eastern half, later called the Byzantine Empire, survived until 1453
- Rome itself was sacked in 410 AD by Alaric the Visigoth and again in 455 AD by the Vandals
- Causes were many and tangled — economic decline, political instability, plague, overextension, pressure from migrating tribes (Goths, Vandals, Huns) pushed west by other migrations
- Edward Gibbon's 1776 work "The History of the Decline and Fall of the Roman Empire" shaped how people have framed the topic for over two centuries
- The "fall" was less a single event than a long unraveling stretched over centuries


### Subject 3: the Apollo 11 moon landing

- Launched July 16, 1969 from Cape Kennedy, landed on the Moon July 20, 1969
- Crew of three: Neil Armstrong (commander), Buzz Aldrin (lunar module pilot), Michael Collins (command module pilot, who orbited but never landed)
- Armstrong was the first human on the Moon; his line was "That's one small step for [a] man, one giant leap for mankind"
- The two astronauts spent about 21 hours on the lunar surface, roughly 2.5 hours of it outside the lander
- They brought back about 47.5 pounds of lunar rock and soil
- The mission was the culmination of John F. Kennedy's 1961 commitment to land a man on the Moon "before this decade is out"
- An estimated 600 million people watched live around the world, the largest TV audience in history at the time


### Subject 4: how the Mona Lisa became the world's most famous painting

- Painted by Leonardo da Vinci between roughly 1503 and 1519
- Before 1911, it was respected but not unusually famous — one of many great Renaissance works hanging in the Louvre
- On August 21, 1911, it was stolen from the Louvre by Vincenzo Peruggia, an Italian handyman who had helped install the painting's protective glass
- The theft made international headlines for over two years; photographs of the empty wall ran everywhere and people queued just to look at the blank space
- The painting was recovered in 1913 when Peruggia tried to sell it to a gallery in Florence
- The theft, more than the brushwork, is what catapulted the Mona Lisa into global icon status — fame born from absence


## Raw files

- [baseline.md](baseline.md) — exactly what the no-skill agent wrote, no edits
- [humanizer.md](humanizer.md) — exactly what the agent with this skill wrote, no edits
- [other-humanizer.md](other-humanizer.md) — exactly what the agent with another humanizer skill wrote, no edits
