# Benchmark

I spawned two Claude agents in parallel, in two separate tmux windows. One had the humanizer skill loaded (it read `SKILL.md` before writing), the other didn't. Both got the exact same four subjects, the exact same factual references, and the exact same instructions about length and format.

Each agent wrote its output directly into its own file in this folder. I didn't write, paste, or edit anything in `baseline.md` or `humanizer.md`. The agents did.


## The four subjects

1. The history of chocolate
2. How GPS works
3. Why cats purr
4. The Wright Brothers' first flight


## Quick contrast, opener by opener

A scan of the first sentence each agent wrote for each subject. Same facts available to both, very different starting move.

| Subject | Baseline opener (no skill) | Humanizer opener (with skill) |
|---|---|---|
| Chocolate | "Chocolate has a rich and fascinating history that spans thousands of years." | "For most of its life, chocolate wasn't sweet." |
| GPS | "GPS, or the Global Positioning System, relies on a network of more than 30 satellites orbiting Earth..." | "There are about thirty satellites circling the planet at 20,200 km, each one shouting its position and the time, over and over. Your phone listens." |
| Cats purring | "Cats produce their distinctive purring sound by rapidly twitching the muscles in their larynx..." | "A cat's purr isn't coming from the chest the way people think." |
| Wright Brothers | "The Wright Brothers' first powered flight took place on December 17, 1903, at Kitty Hawk, North Carolina, marking a pivotal moment in human history." | "Twelve seconds and 120 feet, into the wind off the dunes at Kitty Hawk." |


## Full comparison, paragraph by paragraph

| Subject | Baseline (no skill) | Humanizer (with skill) |
|---|---|---|
| **The history of chocolate** | Chocolate has a rich and fascinating history that spans thousands of years. The cacao tree, Theobroma cacao, is native to Central and South America, where the Olmecs were likely the first to process cacao beans around 1500 BC. The Mayans and Aztecs later embraced cacao, drinking it as a bitter, frothy beverage and even using the beans as a form of currency. Chocolate made its way to Europe in the 16th century through Spanish conquistadors, where sugar was added to counter its natural bitterness and transform it into a sweet treat. The 19th century brought further innovation with the introduction of solid chocolate bars, and in 1875, Daniel Peter invented milk chocolate in Switzerland, paving the way for the modern confection we enjoy today. | For most of its life, chocolate wasn't sweet. The Olmecs were grinding cacao around 1500 BC, and by the time the Mayans and Aztecs had their hands on it, it was a thick bitter drink they'd whip into foam and pass around at ceremonies. The beans doubled as currency. Spanish conquistadors carried it back across the Atlantic in the 1500s, and someone there had the obvious idea of adding sugar. The bar you eat now is even younger than that. Daniel Peter mixed milk into it in Switzerland in 1875, and that's basically the version that won. |
| **How GPS works** | GPS, or the Global Positioning System, relies on a network of more than 30 satellites orbiting Earth at an altitude of around 20,200 kilometers. Each satellite continuously broadcasts its position and the precise time, and a GPS receiver on the ground listens to signals from at least four satellites simultaneously. By measuring how long each signal takes to arrive, the receiver calculates its distance to each satellite and uses a process called trilateration to pinpoint its location in three-dimensional space. Originally developed by the US military in the 1970s, GPS was opened to civilian use in the 1980s and made fully accurate for civilians in 2000, becoming an essential part of modern navigation. | There are about thirty satellites circling the planet at 20,200 km, each one shouting its position and the time, over and over. Your phone listens. It catches signals from at least four of them, works out how long each one took to arrive, and from those four distances it figures out where you're standing in three dimensions. The military built the system in the 1970s and opened it up to civilians a decade later. The signal was still deliberately fuzzy for outsiders until 2000; before then your handheld GPS was off by about a hundred meters because the Pentagon didn't want anyone else's missiles to be accurate. |
| **Why cats purr** | Cats produce their distinctive purring sound by rapidly twitching the muscles in their larynx around 25 to 30 times per second, with the vibration occurring during both inhalation and exhalation, which is why the sound is continuous. While many people associate purring with contentment, cats also purr when they are injured, sick, or giving birth, suggesting it serves multiple purposes. Interestingly, the frequencies in purring, around 25 to 50 Hz, overlap with frequencies known to promote bone healing and tissue regeneration. Domestic cats and many wild cats such as cheetahs and bobcats can purr, but the big cats that roar, like lions and tigers, generally cannot. Kittens begin purring within a few days of birth, and mother cats use it to help their blind newborns locate them. | A cat's purr isn't coming from the chest the way people think. It's the muscles around the larynx twitching about 25 to 30 times a second, on the inhale and the exhale, which is why the sound never stops to take a breath. And it isn't only a happy noise. Cats purr when they're hurt or in labor too. The frequencies sit in the 25 to 50 Hz range, the same band researchers have linked to bone healing, which is suggestive even if nobody's nailed it down. Kittens are born blind and start purring within days, mostly so their mother can find them by the buzzing. |
| **The Wright Brothers' first flight** | The Wright Brothers' first powered flight took place on December 17, 1903, at Kitty Hawk, North Carolina, marking a pivotal moment in human history. Wilbur and Orville Wright, bicycle shop owners from Dayton, Ohio, designed and built the Wright Flyer themselves, a biplane equipped with a 40 horsepower engine of their own design. The first flight, with Orville at the controls, lasted just 12 seconds and covered 120 feet, but they made four flights that day, with the longest reaching 59 seconds and 852 feet, piloted by Wilbur. Despite the magnitude of their achievement, news did not spread widely at first, and many people remained skeptical until the brothers gave public demonstrations in 1908. | Twelve seconds and 120 feet, into the wind off the dunes at Kitty Hawk. That was the first one, December 17, 1903, with Orville at the controls and his brother running alongside. They were bicycle mechanics from Dayton who'd built their own engine because nobody made one light enough. They flew four times that day. Wilbur took the longest, 59 seconds and 852 feet, before the wind picked the Flyer up and broke it on the sand. The story barely traveled at first; most papers didn't believe them until they started flying in public five years later. |


## The references both agents received

The agents had access to nothing more than what is listed below for each subject. The humanizer agent didn't have extra facts, it just made different choices with the same facts.

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


## Raw files

- [baseline.md](baseline.md) — exactly what the no-skill agent wrote, no edits
- [humanizer.md](humanizer.md) — exactly what the with-skill agent wrote, no edits
