# Federico Mastellone

Systems Engineer specialized in Performance, Tracing & Reproducible Infrastructure

## Summary

I am a systems engineer specialized in performance benchmarking of distributed systems and the infrastructure needed to do it reproducibly: fleet provisioning, node operations, deterministic builds, orchestration, and metrics pipelines. I have worked on Linux for more than 20 years, and it has been my only environment for over a decade, from bare-metal point-of-sale terminals to multi-region cloud fleets. That includes hardware-level work: serial-protocol drivers I designed and implemented for fuel dispensers and fiscal printers, directly from the wire-level protocol specifications. My core tools are Nix, Bash, HashiCorp Nomad, AWS, and PostgreSQL, with a decade of Haskell behind them.

## Performance & Tracing

I build and operate the benchmarking infrastructure for [cardano-node](https://github.com/IntersectMBO/cardano-node), the software powering the Cardano blockchain. Every cardano-node release is validated on this infrastructure before shipping.

- **Performance reports**: metrics analyzed down to the millisecond, published with each evaluation. Examples: [memory / execution budget evaluation (10.2, 2025)](https://updates.cardano.intersectmbo.org/reports/2025-03-execbudget-memory-10.2/) ([PDF](https://updates.cardano.intersectmbo.org/assets/files/execbudget-10.2-mem_scaling-ae344917bf4358c013821b4a7449f283.pdf)), [release performance evaluation (10.1.1, 2024)](https://updates.cardano.intersectmbo.org/reports/2024-10-performance-10.1.1/) ([PDF](https://updates.cardano.intersectmbo.org/assets/files/release-10.1.1.voting-01ee31495edecaf8c36b79c94247919a.pdf)).
- **Fleet provisioning and node operations**: reproducible benchmarking clusters of 52 AWS machines across three regions, administered directly over SSH and automated with Nix, Bash, and HashiCorp Nomad (extended with a custom plugin). Main PRs: [#6544](https://github.com/IntersectMBO/cardano-node/pull/6544), [#6611](https://github.com/IntersectMBO/cardano-node/pull/6611), [#4760](https://github.com/IntersectMBO/cardano-node/pull/4760), [#4852](https://github.com/IntersectMBO/cardano-node/pull/4852), [#5037](https://github.com/IntersectMBO/cardano-node/pull/5037), [#5068](https://github.com/IntersectMBO/cardano-node/pull/5068), [#5129](https://github.com/IntersectMBO/cardano-node/pull/5129).
- **Low-level performance engineering**: OS-level tuning such as disk-cache behavior for on-disk benchmarks, and analysis of Haskell runtime memory usage and garbage-collector behavior.

## Nix Build Engineering

I keep large Nix codebases simple, fast, and dependency-light. On cardano-node, a repository with roughly 520 CI jobs, I restructured the Nix code behind the Hydra CI pipeline for optimized cache hits ([#6105](https://github.com/IntersectMBO/cardano-node/pull/6105)): Hydra evaluation time dropped from multiple hours to under 12 minutes, and post-evaluation job processing from over 40 minutes to about 8. This was the final step of a sustained simplification effort ([#5957](https://github.com/IntersectMBO/cardano-node/pull/5957), [#5983](https://github.com/IntersectMBO/cardano-node/pull/5983)), not a one-off.

Feedback from the CI infrastructure maintainer after #6105:

> "Big improvement from what I've seen already! [...] it looks like there is a solid ~30 minute improvement on the post-eval minimum build time also. Awesome!"

## Haskell

I have been an active member of the Haskell community for more than 10 years, with a [merged contribution](https://github.com/haskell/cabal/pull/3670) to [Cabal](https://www.haskell.org/cabal/), Haskell's package manager.

## Projects

- [fmaste.github.io/Haskell](https://fmaste.github.io/Haskell/): Notes on Haskell and theoretical computer science, including [type checking and inference](https://fmaste.github.io/Haskell/doc/TypeCheckingAndInference.html), [evaluation strategies](https://fmaste.github.io/Haskell/doc/EvaluationStrategies.html), and [EDSL design](https://fmaste.github.io/Haskell/doc/EDSL) ([source](https://github.com/fmaste/Haskell/blob/master/src/EDSL.hs)).
- [Helenium](https://github.com/fmaste/Helenium): A Haskell EDSL for automated browser testing, in production since 2011, with a [web console](https://github.com/fmaste/HeleniumConsole) for creating, editing, and running tests with rich output (screenshots, debug logs, assertions, warnings).
- [Mafia](https://github.com/fmaste/Mafia): A Cabal alternative with Nix-style reproducible builds, including [research notes on GHC internals](https://github.com/fmaste/Mafia/blob/master/docs/Executable.md) (2016).

## How I Work

Simplicity first: minimal dependencies and no over-engineering, as the dependency removal and pipeline simplification above show in practice. Testing as a requirement, not an option: unit tests plus property-based testing with [QuickCheck](https://hackage.haskell.org/package/QuickCheck) and [Hedgehog](https://hackage.haskell.org/package/hedgehog), wired into CI. Code evolves through small, reviewable refactoring steps, with [git-bisect](https://git-scm.com/docs/git-bisect) as the safety net.

## External

LinkedIn: https://www.linkedin.com/in/fmaste/

## Education

B.S. in Computer Science Engineering, [ITBA](https://www.itba.edu.ar/)
