# Benchmark

I spawned two Claude agents in parallel, in two separate tmux windows. One had the humanizer skill loaded (it read `/Humanizer-Skill/SKILL.md` before writing), the other didn't. Both got the exact same four subjects, the exact same factual references, and the exact same instructions about length and format.

Each agent wrote its output directly into its own file in this folder. I didn't write, paste, or edit anything in `baseline.md` or `humanizer.md`. The agents did.

Compare them side by side and decide for yourself whether the skill is doing real work or not.


## The four subjects

1. The history of chocolate
2. How GPS works
3. Why cats purr
4. The Wright Brothers' first flight


## The references both agents received

### Subject 1: the history of chocolate

- The cacao tree (Theobroma cacao) is native to Central and South America
- The Olmecs, around 1500 BC, were likely the first to process cacao beans
- The Mayans and Aztecs drank it as a bitter, frothy beverage and used cacao beans as currency
- Chocolate reached Europe in the 16th century through Spanish conquistadors
- Sugar was added in Europe to counter the bitterness, which turned it into a sweet treat
- Solid chocolate bars came in the 19th century, and milk chocolate was invented in 1875 by Daniel Peter in Switzerland


### Subject 2: how GPS works

- A network of about 30+ satellites orbits Earth at around 20,200 km altitude
- Each satellite continuously broadcasts its position and the precise time
- A GPS receiver listens to signals from at least 4 satellites at once
- By measuring how long each signal took to arrive, the receiver calculates its distance to each satellite
- With distances to 4 satellites it can pinpoint its location in 3D space (trilateration)
- Originally developed by the US military in the 1970s, opened to civilian use in the 1980s, and made fully accurate for civilians in 2000


### Subject 3: why cats purr

- Cats produce purring by rapidly twitching the muscles in their larynx, about 25 to 30 times per second
- The vibration happens during both inhalation and exhalation, which is why the sound is continuous
- Purring is not just a sign of contentment; cats also purr when they are injured, sick, or giving birth
- The frequencies in purring (around 25 to 50 Hz) overlap with frequencies known to promote bone healing and tissue regeneration
- Domestic cats and many wild cats (cheetahs, bobcats, etc.) purr, but the big cats that roar (lions, tigers) generally do not
- Kittens start purring within a few days of birth, and mother cats purr to help blind newborns find them


### Subject 4: the Wright Brothers' first flight

- The flight took place on December 17, 1903, at Kitty Hawk, North Carolina
- Wilbur and Orville Wright were bicycle shop owners from Dayton, Ohio
- The Wright Flyer was a biplane with a 40 horsepower engine they designed and built themselves
- The first flight, with Orville at the controls, lasted 12 seconds and covered 120 feet
- They made four flights that day; the longest was 59 seconds and 852 feet, flown by Wilbur
- News didn't spread widely at first, and many people doubted the claims until public demonstrations in 1908


## Files

- [baseline.md](baseline.md) — agent without the humanizer skill
- [humanizer.md](humanizer.md) — agent with the humanizer skill
