# humanizer comparison

three agents rewrote the same four AI-style paragraphs. one agent had no humanizer skill loaded (just told to rewrite). the other two each had a different humanizer skill loaded. same input to all three, side by side here.

| agent | skill |
|---|---|
| **@plain** | none. just told to rewrite. |
| **@humanizer** | `humanizer` (the skill in this repo) |
| **@other** | `humanizer-other` (the alternative humanizer skill) |

---

## 1. polymorphism

**original:**

> Polymorphism is a fundamental concept in object-oriented programming that allows objects of different classes to be treated as instances of a common superclass. It enables a single interface to represent different underlying forms, which significantly enhances code flexibility and reusability. By leveraging polymorphism, developers can write more generic and maintainable code that adapts seamlessly to various data types and behaviors.

| @plain | @humanizer | @other |
|---|---|---|
| Polymorphism lets you treat objects from different classes as if they were the same type, usually through a shared parent class or interface. The same method call can do different things depending on the actual object behind it. That's useful because you can write code against the general type and let each subclass handle the specifics, instead of branching on every possible case yourself. | Polymorphism is the trick where you call the same method on different objects and each one does its own thing. Same name, different bodies. Ask a Dog and a Cat to .speak() and one barks, one meows, and your calling code never has to know which animal it's holding. That's the whole point. Write against the shape of the interface, not the specifics, and you stop rewriting the caller every time you add a new kind of thing. | Polymorphism lets you treat objects of different classes through a shared interface. Think a `Shape` base class with `Circle` and `Square` subclasses: call `.area()` on any of them and the right version runs, without the caller knowing which is which. The win is that code using the interface doesn't care about the concrete types, so adding a new shape later doesn't force you to go rewrite everything that touched the old ones. |

---

## 2. exceptions

**original:**

> Exceptions are a critical mechanism in modern programming languages that enable developers to handle unexpected runtime errors in a structured and graceful manner. By utilizing try-catch blocks, programmers can separate the normal flow of execution from error-handling logic, which leads to cleaner and more readable code. Furthermore, exceptions play a vital role in maintaining application stability and providing meaningful feedback to users when something goes wrong.

| @plain | @humanizer | @other |
|---|---|---|
| Exceptions are how most languages deal with runtime errors. Instead of checking a return code after every call, you wrap the risky code in a try block and put the recovery logic in a catch. The normal path stays readable, and the error path is somewhere you can actually find. If nothing handles the exception, it bubbles up until something does, or the program dies, which is usually better than silently continuing with bad state. | Exceptions are how a function says "I can't deal with this, somebody upstairs handle it." Something blows up three calls deep, you throw, and the error skips back up the stack until something is willing to catch it. The try-catch split is what makes the code readable. The happy path stays where you can actually see it, the recovery sits off to the side, and you stop having to thread an error code through every function in between. | Exceptions let you pull error handling out of the main flow of your code. Instead of every function returning some `(result, error)` thing the caller has to check, you throw when something goes wrong and a `catch` further up the stack deals with it. The catch (pun intended) is that control flow gets less obvious, exceptions travel further than you'd expect, and a lot of "graceful handling" in the wild is really just a `catch (Exception e) {}` that quietly eats the bug. They're useful. They're also easy to misuse. |

---

## 3. bees

**original:**

> Bees have played an essential role in human civilization for thousands of years, with evidence of honey collection dating back to ancient Egypt and even earlier prehistoric times. These remarkable insects have been revered across countless cultures, often associated with industriousness, community, and divine wisdom. Throughout history, beekeeping has evolved from simple log hives into a sophisticated practice that supports both agricultural pollination and commercial honey production. Today, bees continue to be a critical component of global ecosystems, and their decline has become a pressing environmental concern that demands urgent attention.

| @plain | @humanizer | @other |
|---|---|---|
| People have been keeping bees, or at least raiding their nests, for a very long time. There are Egyptian wall paintings showing honey harvests, and rock art from well before that. Beekeeping itself has gone from hollowed-out logs to wooden frame hives you can inspect without destroying the colony, and it now feeds into a lot more than just honey, most of it is pollination contracts for orchards and farms. The worrying part is that colonies have been collapsing or weakening for years now, from a mix of pesticides, mites, and habitat loss, and nobody's quite landed on a single fix. | People have been robbing bees for at least 8,000 years. There's a cave painting in Spain of someone halfway up a cliff with one hand in a hive and the other clutching a basket, which tells you roughly how badly we wanted the honey. The Egyptians kept bees in clay tubes and buried jars of honey in their tombs that came out edible 3,000 years later. From there the hives got fancier and the production scaled up, and now California's almond crop physically cannot happen without trucks hauling billions of bees in every February. Which is also why colony collapse stopped being a hobbyist worry and started being an agriculture one. | People have been raiding bee colonies for honey since at least 7000 BC, judging by cave paintings in Spain that show some poor soul climbing a cliff with a basket while bees swarm their head. The Egyptians kept hives in clay cylinders and floated them up and down the Nile to chase the bloom. Modern beekeeping mostly uses the stackable wooden frame Lorenzo Langstroth came up with in 1851, which has barely changed since. The reason any of this matters now, beyond honey, is pollination. Almonds basically can't happen without trucked-in commercial hives, and a lot of the other stuff you eat is in a similar boat. So when people talk about colony collapse, the worry isn't really "are bees going extinct" so much as "can the people growing your food keep affording to rent them." |

---

## 4. the printing press

**original:**

> The invention of the printing press by Johannes Gutenberg in the mid-fifteenth century stands as one of the most transformative moments in human history, fundamentally reshaping how knowledge was preserved, shared, and disseminated. Prior to this revolutionary development, books were laboriously copied by hand, making them prohibitively expensive and accessible only to the wealthy elite and religious institutions. Gutenberg's movable type technology democratized literacy and learning across Europe, paving the way for the Renaissance, the Reformation, and the eventual rise of modern scientific thought. The ripple effects of this single innovation continue to influence our world today, as it laid the very foundation for the information age in which we now live.

| @plain | @humanizer | @other |
|---|---|---|
| Before Gutenberg, books were copied by hand, one at a time, mostly by monks. That made them slow to produce and expensive enough that only churches, universities, and rich people really owned them. Gutenberg's press, around the 1450s, used movable metal type you could rearrange for each page, so once you'd set a page you could print hundreds of copies in the time it used to take to copy one. Within a few decades there were presses all over Europe, and the cost of a book dropped dramatically. That's a big part of why the Reformation spread the way it did, and why scientific ideas could actually circulate instead of sitting in a single library somewhere. | Before Gutenberg, copying out a Bible took a monk close to a year, which made books the kind of thing you owned if you were a cathedral or a king. He worked out the trick of casting individual letters in metal in the 1450s, and within fifty years European presses had printed somewhere around twenty million books. That math alone changes everything downstream. Luther nails his 95 theses to a church door in 1517 and they're circulating across Germany inside two weeks, which has no path to existence in the world before. Gutenberg himself, for what it's worth, got sued by his investor and lost the shop. | Before Gutenberg, books in Europe were copied by hand, usually by monks, and a single Bible could take years. They cost roughly what a small farm cost. His real innovation around 1450 wasn't the press (wine and olive presses already existed) but the movable metal type: tiny reusable letters you could rearrange into any page, cast cheap from a hand mold. A print shop with a few workers could now do in a week what a scriptorium needed a year for. Within fifty years there were something like 20 million printed books floating around Europe. Once that's true, a lot of other things start being possible. Luther's pamphlets reach the kind of audience that would've been unthinkable a century earlier. Scientific results actually circulate. And the idea that regular people might read at all stops being weird. |
