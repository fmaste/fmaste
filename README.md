# Federico Mastellone

## Education

B.S. in Computer Science Engineering, [ITBA](https://www.itba.edu.ar/)

## Summary

I’m a [Scrum Alliance Certified Scrum Developer](https://www.scrumalliance.org/get-certified/developer-track/certified-scrum-developer) and I have been following agile practices for many years, on-site or remotely with companies from different regions. I have worked in Java projects with the usual Hibernate/Struts frameworks and used all the object oriented patterns you can imagine, mostly when trying to make sense of big spaghetti PHP codebases.

## Haskell

But mostly, I have been a silent participant of the Haskell community for more than 10 years. I made [contributions](https://github.com/haskell/cabal/pull/3670) to [Haskell's Cabal package manager](https://www.haskell.org/cabal/) when I needed for a private project and read the most significant papers and books, from "[A History of Haskell: Being Lazy with Class](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/history.pdf)" to "[Parallel and Concurrent Programming in Haskell](https://simonmar.github.io/pages/pcph.html)"

- https://fmaste.github.io/Haskell/
  - Still a work-in-progress. Building a little summary of everything I have read and know about Haskell and Theoretical Computer Science.
    For example:
    - [Type Checking and Type Inference in Action](https://fmaste.github.io/Haskell/doc/TypeCheckingAndInference.html)
    - [Evaluation Strategies - Lazy vs. Non-Strict](https://fmaste.github.io/Haskell/doc/EvaluationStrategies.html)
    - [Notes](https://fmaste.github.io/Haskell/doc/EDSL) and [source code](https://github.com/fmaste/Haskell/blob/master/src/EDSL.hs) about different ways of building an EDSL in Haskell.
- https://github.com/fmaste/Helenium
  - I built my first Haskell tool used in production at the end of 2011.
    Tired of having to test before and after every release at work, I built my own domain specific language embedded in Haskell (EDSL) to avoid doing manual testing.
    I also build a [web console](https://github.com/fmaste/HeleniumConsole) for the team to create, edit and run the tests with just a a web browser while providing a nice output of the whole run (screeshots, debug, assertions, warnings, etc).
- https://github.com/fmaste/Mafia
  - Here I made public a 2016 tool I created that was also a research project on GHC [internals](https://github.com/fmaste/Mafia/blob/master/docs/Executable.md).
    I was having problems with Cabal at that time so I built my own alternative with Nix style reproducible builds.
- https://github.com/haskell/cabal/pull/3670
  - My contribution to Haskell's Cabal that got merged. I needed to package projects with [auto generated modules](https://cabal.readthedocs.io/en/3.4/cabal-package.html#autogenerated-modules-and-includes) and it was not working as expected.
- https://github.com/fmaste/jsMVC
  - The web console mentioned above was built with a JavaScript MVC framework I created.
- https://github.com/fmaste/hansible
  - A little tool to generate a Graphviz DOT description file from Ansible hosts.

## Principles

> “Premature optimization is the root of all evil”
> 
> Donald Knuth.

Always keep it simple and don’t overbuild.

If you're going to break something you better break it early, committing and merging often is a good practice and when an error is found it's complemented very well with [git-bisect](https://git-scm.com/docs/git-bisect).

But to find errors you need proper testing, ***"Program testing can be used to show the presence of bugs, but never to show their absence!"***. So in addition to defining the base cases by induction with [HUnit](https://hackage.haskell.org/package/HUnit), I use [QuickCheck](https://hackage.haskell.org/package/QuickCheck) and [Hedgehog](https://hackage.haskell.org/package/hedgehog), that coupled [GitHub Actions](https://github.com/features/actions) are your best friends. Evolving code without testing is dangerous!

The best way to evolve the code or understand legacy code is refactoring it, making small steps until it gets easier to understand and fix errors.
When extracting, renaming, refactoring in general I follow the steps detailed in [Martin Fowler's book Refactoring](https://refactoring.com/). Although it's mostly object oriented the methodology can still be applied to functional programming (The downside of doing small / atomic commits is that you have to remember to [merge squash](https://git-scm.com/docs/git-merge#Documentation/git-merge.txt---squash) to keep the log uncluttered).

Having code that looks nice and everybody can understand is important. Style guidelines can vary from company to company (and generate a lot of [bikeshedding](https://en.wikipedia.org/wiki/Law_of_triviality)) but I always try to be as standard as possible and use as few dependencies as possible.

## External

Linkedin: https://www.linkedin.com/in/fmaste/
