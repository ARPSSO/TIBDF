
<br />
<div align="center">
  <h3 align="center">Trusted In-Browser Data Forwarding (TIBDF) Proof</h3>

  <p align="center">
    The proof for in-browser data forwarding trustworthiness in ARPSSO.
    <br />
    <a href="https://arpsso.hejunlin.cn"><strong>View ARPSSO Demo »</strong></a>
  </p>
</div>

We use the the Tamarin Prover to formally verify the TIBDF's Trustworthiness. The Tamarin Prover is
an powerful automated tool for verifying security protocols within the symbolic cryptographic framework. For more about Tamarin Prover, please visist https://tamarin-prover.com.

This repository contains the theories, and the `proofs/` subdirectory contains the proven models, which can be loaded into Tamarin to reproduce the proofs we obtained.

## Getting Started
Run in interactive mode:
```
tamarin-prover interactive .
```
Then visit `http://127.0.0.1:3001`.



## Benchmarks
We obtained the proofs using Tamarin version 1.8.0.

The proofs were computed automatically on a Mac Studio wiht Apple M1 Max, 10-core CPU, 32-core GPU, 64 GB of RAM, running macOS 14.1.2.

The computation took about 1 hour and 30 minutes. Output:

```
/* All wellformedness checks were successful. */

/*
Generated from:
Tamarin version 1.8.0
Maude version 2.7.1
Git revision: UNKNOWN, branch: UNKNOWN
Compiled at: 2023-09-01 12:12:18.719033 UTC
*/

end

==============================================================================
summary of summaries:

analyzed: TIBDF.spthy

  processing time: 5348.63s
  
  executable (exists-trace): verified (11 steps)
  secrecy (all-traces): verified (4083 steps)

==============================================================================
tamarin-prover -Dtimethis TIBDF.spthy --prove -v  21630.29s user 810.77s system 419% cpu 1:29:08.97 total
```
