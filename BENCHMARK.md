# Benchmark

Three agents, four topics, identical factual references. Two agents wrote without the humanizer skill (Baseline A and Baseline B). The third agent was told to read SKILL.md and write from inside it, and was explicitly told not to invoke any other writing skill that might exist in its environment. The only variable was the skill.

The four topics: the invention of paper, how airplane wings generate lift, why we yawn, and the fall of the Berlin Wall. Each paragraph was asked for in 3-6 lines.

What follows is the raw output, untouched.


## Topic 1: the invention of paper

### Baseline A

Paper was invented in China around 105 AD, with tradition crediting the court official Cai Lun for refining the process. Before paper, Chinese scribes wrote on silk, which was expensive, or on bamboo strips, which were heavy and awkward to handle. The new method involved soaking plant fibers such as bark, hemp, and rags into a pulp, then pressing the mixture into thin sheets and letting them dry. The technique spread west slowly, reaching the Islamic world after the Battle of Talas in 751 AD, when captured Chinese papermakers passed on their knowledge. From there it travelled to Europe through Spain in the 12th century, and over the following centuries it replaced parchment because it was much cheaper to produce.

### Baseline B

Paper was invented in China around 105 AD, traditionally credited to a court official named Cai Lun. Before paper, writing was done on silk, which was expensive, or on bamboo strips, which were heavy and awkward to store. The new material was made by soaking plant fibers such as bark, hemp, and rags into a pulp, then pressing the mixture into thin sheets and letting them dry. The technique spread westward slowly, reaching the Islamic world after the Battle of Talas in 751 AD, when captured Chinese papermakers passed on their craft. From there it travelled into Europe through Spain in the 12th century, and over the following centuries it replaced parchment because it was far cheaper to produce.

### Humanizer

Paper started in China around 105 AD, credited to Cai Lun, a court official who got tired of writing on silk (too expensive) and bamboo strips (too heavy to carry across a room, let alone a province). The method was almost embarrassingly simple once you saw it. Soak bark, hemp, and old rags until the fibers let go of each other, press the slurry thin, dry it flat. The technique drifted west the way useful things do, slowly. It reached the Islamic world after the Battle of Talas in 751, when captured Chinese papermakers traded the recipe for their lives, and only landed in Europe through Spain in the 12th century, where it spent the next few hundred years quietly putting parchment out of business on price alone.


## Topic 2: how airplane wings generate lift

### Baseline A

An airplane wing is shaped so that air moves faster over its curved upper surface than along its flatter underside. According to Bernoulli's principle, the faster-moving air on top has lower pressure than the slower air below, and that pressure difference pushes the wing upward. The angle of attack also matters: tilting the wing upward into the airflow redirects air downward, and by Newton's third law the wing is pushed up in response. Lift only appears when the wing is moving forward through the air, which is why aircraft need a runway to gather speed before takeoff. If the angle of attack becomes too steep, airflow separates from the upper surface, lift collapses, and the wing stalls.

### Baseline B

An airplane wing is shaped with a curved upper surface and a flatter lower one, so air moves faster over the top than along the bottom. According to Bernoulli's principle, that faster-moving air exerts less pressure than the slower air below, and the pressure difference pushes the wing upward. The angle of the wing against the oncoming air, known as the angle of attack, also matters: tilting the wing up redirects air downward, and by Newton's third law the wing is pushed up in response. Because all of this depends on air flowing over the wing, the plane needs forward motion, which is why a runway is required for takeoff. If the angle of attack becomes too steep, the airflow separates from the wing's surface, lift collapses, and the plane stalls.

### Humanizer

A wing is curved more on top than on the bottom, so the air running over it has further to go and moves faster than the air underneath. Faster air pushes less, by Bernoulli, so the pressure below is higher than the pressure above, and the wing gets shoved upward. The angle of the wing matters too. Tilt it up and you redirect a column of air downward, and Newton hands you the reaction for free. None of this works standing still, which is why a runway exists. Push the tilt past what the airflow can hug and the air separates from the surface, lift dies, and the plane stalls.


## Topic 3: why we yawn

### Baseline A

Yawning is one of the most common human behaviors, and yet scientists still cannot fully explain why we do it. The old idea that yawning boosts oxygen intake has largely been disproved by research. The leading current theory is that yawning helps regulate the temperature of the brain by drawing in cooler air and increasing blood flow to the head. Yawning is also contagious in humans and in some animals such as dogs and chimpanzees, and that contagion appears to be linked to empathy. Most of us start yawning before we are even born, since ultrasounds have captured fetuses yawning in the womb, and unusually frequent yawning can sometimes point to sleep disorders, heart problems, or certain neurological conditions.

### Baseline B

Yawning is one of the most common things humans do, and yet scientists still cannot say with certainty why we do it. The older idea that yawning boosts oxygen intake has largely been disproved by research. The current leading theory is that yawning helps regulate the temperature of the brain by pulling in cooler air and increasing blood flow to the head. It is also contagious in humans and in some animals such as dogs and chimpanzees, and that contagion appears to be linked to empathy. People begin yawning before they are even born, with ultrasounds showing fetuses yawning in the womb, and unusually frequent yawning can sometimes point to medical issues such as sleep disorders, heart problems, or certain neurological conditions.

### Humanizer

Yawning is one of those things everyone does and nobody can quite explain. The oxygen theory, the one your gym teacher told you, has mostly fallen apart under testing. The current best guess is temperature regulation, that pulling cool air in and bumping blood flow helps cool the brain a little. The contagious part is stranger. It catches in humans, in dogs, in chimps, and the people who catch it most readily tend to score higher on empathy measures. Fetuses yawn in the womb, caught on ultrasound months before they breathe air. And if you find yourself yawning constantly for no reason, that can point at a sleep disorder, a heart issue, something neurological worth asking about.


## Topic 4: the fall of the Berlin Wall

### Baseline A

The Berlin Wall stood from 1961 to 1989, dividing East and West Berlin after East Germany built it to stop its citizens from fleeing to the West. On the evening of November 9, 1989, East German official Günter Schabowski mistakenly announced at a press conference that travel restrictions would be lifted immediately. East Berliners rushed to the border crossings, and the overwhelmed guards eventually gave up trying to hold them back and opened the gates. Crowds from both sides climbed on top of the wall to celebrate together, chipping off pieces as souvenirs. The fall of the wall helped trigger the rapid collapse of communist governments across Eastern Europe and led to the reunification of Germany on October 3, 1990.

### Baseline B

The Berlin Wall stood from 1961 to 1989, dividing East and West Berlin after East Germany built it to stop its citizens from fleeing westward. On the evening of November 9, 1989, an East German official named Günter Schabowski mistakenly told a press conference that travel restrictions would be lifted immediately. Hearing the news, East Berliners flocked to the border crossings, and the overwhelmed guards eventually gave up and opened the gates. Crowds from both sides climbed onto the wall together, celebrating and chipping off pieces as souvenirs. The collapse of the wall set off a rapid unravelling of communist governments across Eastern Europe and led to the reunification of Germany on October 3, 1990.

### Humanizer

The wall went up in 1961 to keep East Germans from walking west, and it came down on the evening of November 9, 1989, because a man read a note wrong. Günter Schabowski, an East German official, was handed new travel rules at a press conference, didn't quite understand them, and when a reporter asked when they took effect he said "immediately." East Berliners heard him on the news and walked to the checkpoints. The guards had no orders, no script, and eventually no choice; they opened the gates. People climbed on top of the concrete with hammers and chisels, working off pieces while strangers from both sides drank together in the cold. Within a year the other communist governments in the region had folded, and Germany was one country again on October 3, 1990.


## What stands out

The two baselines converged again. They cover the same facts in the same order with almost interchangeable phrasing ("the technique spread west slowly," "an airplane wing is shaped so that," "yawning is one of the most common"). Neither baseline reaches outside the supplied references or makes a choice that surprises the reader.

The humanizer paragraphs make choices in every one.

Paper: "tired of writing on silk (too expensive) and bamboo strips (too heavy to carry across a room, let alone a province)" gives you the human reason for the invention in one stroke. "Captured Chinese papermakers traded the recipe for their lives" carries the same fact the baselines reported neutrally, but with the actual stakes attached. "Quietly putting parchment out of business on price alone" closes with a working metaphor instead of an abstract summary.

Airplane wings: "Newton hands you the reaction for free" and "None of this works standing still, which is why a runway exists" are two ways of saying what the baselines said, except they sound like a person who actually understands the physics rather than a textbook reciting it.

Yawn: "The oxygen theory, the one your gym teacher told you, has mostly fallen apart under testing" is a single line that does what a paragraph of formal prose can't. It plants the reader in a memory and overturns it.

Berlin Wall: "because a man read a note wrong" is the entire story in one clause. The baselines wrote three sentences to say the same thing, and somehow with less weight.

Same facts. Same references. The humanizer agent kept reaching for the version that sounds like somebody telling you about it, and the baselines kept landing on the version that sounds like somebody reporting it.
