https://youtu.be/Ve-akpov78Q?si=HDg6UPXTqBDGafC2

### Summary

Large enterprises' codebases are extremely hard to manage because they are huge, interdependent, and often highly varied.  They already grow like weeds, but in the near future, they will grow even faster, thanks to AI-enabled development.  New tools need to be developed to allow the enterprises' staff who work on cross-cutting concerns, to manage that more abstract complexity better.

At a narrow scope, tools like _link not tracked_ have shown how AI can aid developers in quickly adding features, but what about when you need something more like a bulldozer, for huge tasks like changing your logging platform, enterprise-wide, across a thousand repos?  For _link not tracked_ in _link not tracked_

This video explores one solution to that problem, a product called _link not tracked_, and goes into the technical details about how it uses massively concurrent forking agentic workflows to solve the problem.  I found the section at 14:00 about the use of _link not tracked_ to do fast, exploratory _link not tracked_ (which feels a little like _link not tracked_) to be particularly intriguing.

### Details

[[agent]] _link not tracked_ [[codified agentic workflow]]

At 1:57 _link not tracked_ the product, _link not tracked_, is aimed at _link not tracked_ instead of _link not tracked_.  Basically, it is targeted at top developers to be a very large-scale code bulldozer (vs. helping those who are less familiar with coding be able to make things they would not have been able to).  X Kinda funny because _link not tracked_ but that's essentially what you'll get with these super-high-leverage system-wide tools.
...
_link not tracked_

At 3:20 once more developers start using AI (and the AI becomes more powerful, too) there's gonna be way more code, and we're gonna need tools for managing just tons of code. Rather than single lines, you're gonna be making huge changes across many files. X  _link not tracked_ _link not tracked_ _link not tracked_

At 8:00 when searching to replace the logging for a whole enterprise across thousands of repos, they use their own special SQL that does both static analysis in concert with using LLMs . X Roughly makes me think of _link not tracked_ techniques more generally.

At 10:50 the idea that IDEs are already giving us superhuman tools with _link not tracked_, _link not tracked_, etc, and that we need to ensure that we give our LLMs the same tools X _link not tracked_

At 12:50 the iteration time for checking a potential solution is comprised on coming up with a code change in the LLM, then checking the compilation.  In big enterprises, the build time for _link not tracked_ can be multi-minute, which actually dwarfs the LLM time and kills the iteration time.  You need to make sure that you are using the same language server tools that you would as a person using the IDE... where they do incremental change detection and you get feedback almost immediately instead of relying on your CLI tools that are part of CI (since they are so slow).
...
_link not tracked_
...
What you want is _link not tracked_ for your _link not tracked_

At 14:00 he talks about the problem of [[compounding error]]s and how you can get in a bad state that you can't recover from. The solve is to use _link not tracked_ to be able to snapshot the memory of a process at a known good state and then try 10 hypothetical changes, then you rely on things like _link not tracked_s, etc. to determine which ones are the best and you establish a _link not tracked_ to decide what should become the new base to fork from x _link not tracked_ _link not tracked_
...
This also reminds be of _link not tracked_ approaches to reasoning using the _link not tracked_ methods.  Basically _link not tracked_ _link not tracked_ then winnowing things down by _link not tracked_.  The difference here is that these seem to be short-term hypotheses and _link not tracked_ with the aim of getting to some _new_ _link not tracked_  _link not tracked_, then _link not tracked_ off of that to go further.  That feels a little like _link not tracked_.  This is all to avoid the [[compounding error]] (AKA [[error accumulation]]), which is particularly important because of [[dim - reliability -- low]] and a lack of revisiting _link not tracked_.  LLMs doing _link not tracked_ _link not tracked_ tend to have _link not tracked_ and _link not tracked_, which causes the errors to get worse over time.

At 15:50 he talks about how it can get really expensive to do so many forks to your code and edit the whole file in each of the forks because _link not tracked_ are more expensive than input tokens. Because it's auto regressive. Also the output limits are not growing as fast as the context windows, which have become very large.

At 17:00 he describes the challenges with applying changes. Full file works well, but is very expensive, LLMs are not very good at generating _link not tracked_s with good line numbers, etc. so they invented a loose search and replace. X _link not tracked_

---

[[dim - scale -- high]]