I have been mostly a silent participant of the Haskell community for more than 10 years. I made [contributions](https://github.com/haskell/cabal/pull/3670) to [Haskell's Cabal package manager](https://www.haskell.org/cabal/) when I needed for a private project and read the most significant papers and books, from "[A History of Haskell: Being Lazy with Class](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/history.pdf)" to "[Parallel and Concurrent Programming in Haskell](https://simonmar.github.io/pages/pcph.html)"

- https://github.com/fmaste/Helenium
  - I built my first Haskell tool used in production at the end of 2011.
    Tired of having to test before and after every release at work, I built my own domain specific language embedded in Haskell (EDSL) to avoid doing manual testing.
    I also build a [web console](https://github.com/fmaste/HeleniumConsole) for the team to create, edit and run the tests with just a a web browser while providing a nice output of the whole run (screeshots, debug, assertions, warnings, etc).
- https://github.com/fmaste/Mafia
  - Here I made public a 2016 tool I created that was also a research project on GHC [internals](https://github.com/fmaste/Mafia/blob/master/docs/Executable.md).
    I was having problems with Cabal at that time so I built my own alternative with reproducible builds.
- https://github.com/haskell/cabal/pull/3670
  - My contribution to Haskell's Cabal that got merged. I needed to package projects with [auto generated modules](https://cabal.readthedocs.io/en/3.4/cabal-package.html#autogenerated-modules-and-includes) and it was not working as expected.
- https://github.com/fmaste/Haskell
  - Still a work-in-progress. Building a little summary of everything I have read and know about Haskell and Theoretical Computer Science.
    For example, [notes](https://github.com/fmaste/Haskell/blob/master/doc/EDSL.md) and [source code](https://github.com/fmaste/Haskell/blob/master/src/EDSL.hs) about different ways of building an EDSL in Haskell.
- https://github.com/fmaste/jsMVC
  - The web console mentioned above was built with a JavaScript MVC framework I created.
- https://github.com/fmaste/hansible
  - A little tool to generate a Graphviz DOT description file from Ansible hosts.

I’m a [Scrum Alliance Certified Scrum Developer](https://www.scrumalliance.org/get-certified/developer-track/certified-scrum-developer). I’ve worked remotely for a US based company or with the South African team of another one. I have worked with Java projects with all the Hibernate/Struts frameworks using all the object oriented patterns you can imagine or with a big PHP spaghetti codebase.

The best way to evolve the code or understand legacy code is refactoring it, making small steps until it gets easier to understand and fix errors.
When extracting, renaming, refactoring in general I follow the steps detailed in [Martin Fowler's book Refactoring](https://refactoring.com/). Although it's mostly object oriented the methodology can still be applied to functional programming (The downside of trying to do small / atomic commits is that you have to remember to [merge squash](https://git-scm.com/docs/git-merge#Documentation/git-merge.txt---squash) to keep the log uncluttered.).

Linkedin: https://www.linkedin.com/in/fmaste/
