# General Grant Proposal

* **Project Name: Name** *Glow*: Simple, Secure DApp DSL
* **Team Name: Name** [Mutual Knowledge Systems, Inc.](https://mukn.io)
* **Payment Address:** (BTC) bc1qma9gmt7njg0pjftv3grpgj7l052j0d2f6a4zxh

## Project Overview :page_facing_up:

### Overview

We propose to port our programming language Glow to the Polkadot platform. This three-month, $30,000 project will benefit Polkadot in the long run by bringing DApp users and developers to it. In the short run, the project will also benefit Polkadot by allowing its users to have a cross-platform language that generates matching smart contract and client/server code for financial interactions. In the long run, formal verification will drastically reduce the risks, and layer2-aware code generation will help safely scale transactions and reduce fees, thus making Polkadot a competitive blockchain for any smart contract-based business. The proposed port would be a proof of concept of the Glow language. Further work would be required to robustly support the entire feature set of Polkadot.



#### Relevance to Polkadot

This project will benefit Polkadot and Substrate in the long run
by bringing DApp users and developers to it.
In the short run, the project will also benefit Polkadot
by allowing its users to have a cross-platform language that generates
matching smart contract and client/server code for financial interactions.
In the long run, formal verification will drastically reduce the risks,
and layer2-aware code generation will help safely scale transactions
and reduce fees,
thus making PolkaDot a competitive blockchain for any smart contract-based business.

The proposed port would be a proof of concept of the *Glow* language.
Further work would be required to robustly support the entire feature set of Substrate.

### Project Details

#### The *Glow* Language: Safer, Cheaper DApps

[*Glow*](https://glow-lang.org) is a domain-specific (programming) language for Decentralized Applications (DApps).
Compared to competing DApp languages, *Glow* provides much higher-level abstractions,
that make DApp development not only drastically simpler,
but also portable and amenable to formal verification.
With *Glow*, DApps will be much cheaper and faster to develop and to use,
but also, importantly, to audit and to trust—and thus safer in the end.

The *Glow* compiler automatically enriches a DApp with details like
intermediate transactions, timeouts, and collaterals.
It can emit code in “direct style” as typically followed by humans writing DApps today, but also for “generalized state channels” that allow for scalable private contracts.
The *Glow* compiler then generates not just a “smart contract” for a DApp,
but also matching client and server code.

Last but not least, *Glow* generates a logical model that notably uses
Game Semantics to allow formal verification of security properties of the DApp
in the adversarial environment of permissionless blockchains.
The model is checked using the theorem prover, Z3, as a prerequisite to accepting to run the DApp.
Entire classes of bugs thus disappear when using the *Glow* language,
that today cost millions of dollars in development
and/or operating losses to companies deploying DApps.

#### Relevance to Substrate & Polkadot

Substrate has a good lower-level language for smart contracts, *Ink!*;
but it is missing a good higher-level language:

A language at a high-enough level
one that can generate at the same time matching contract, client/server code, and formal model,
from the same specification;

One that will make it hard or impossible
to write bugs due to missing or reversed authorization checks without being caught;


DApps are interactions between multiple mutually distrusting parties,
who exchange digital assets based on algorithmically verifiable rules
enforced by blockchain smart contracts.

*Ink!* is a great language for contracts at the relatively low-level.

Current languages There is no current language

This project will also spearhead the ability for Polkadot to host DApps written in languages other than its native Rust+Substrate. Since this feat has not been achieved before, we anticipate that this ability may require changes to the platform and to its documentation, that won’t be discovered until the attempt is completed. This will help the Polkadot ecosystem evolve toward effective feature parity or superiority compared to its rival Ethereum, on the dimensions that matter to DApp development.

With respect to Substrate, existing consensus mechanisms include proof-of-authority (Aura), proof-of-stake (Babe), and proof-of-work (Kulupu). We would like to extend this with two more constructions: proof-of-space (Spartan) and (in a later grant) proof-of-storage (Subspace). Both of these are instances of a more general class of proof-of-capacity protocols, which seek to replace "one-CPU-one-vote" with "one-disk-one-vote". Upon completion, this grant would serve to further demonstrate the flexibility of Substrate and FRAME for any abstract blockchain. Other teams seeking to implement slot-based PoC blockchains would also be able to re-use the core crates to reduce development time.  Note that any proof-of-replication implies an underlying proof-of-space. We therefore intend to begin with the much simpler task of implementing Subspace as a pure proof-of-space consensus protocol (Spartan) before extending it into a full proof-of-storage (or replication) protocol envisioned in our whitepaper. 

#### Team Motivation

We are committed to empowering humans to build secure DApps, using our simple to understand and use domain specific language.

Our values include open-source technologies, synergies, and interdisciplinary knowledge.

Our team’s expertise includes game theory, computer science and economics.


#### *Glow* So Far

The first version of *Glow* was released in February 2021, and can work on
either the Ethereum Virtual Machine (EVM), or Cardano's Plutus ecosystem.
Documentation for *Glow* is available at https://glow-lang.org/docs/

[Mutual Knowledge Systems, Inc.](https://mukn.io), a.k.a. MuKn (pronounced “Moon”)
has been developing *Glow* for a year and a half,
based on a prototype previously developed by one of its co-founders.
We are committed to ever growing the language and its ecosystem.

Development for *Glow* is currently funded for the next few months. Our current Docker image is based on Nix, and we have a new one in progress based on Guix.

Upcoming features include a user-friendly web-browser [UI](https://www.youtube.com/watch?v=0ltm6RmyDnM), a [MOOC](https://gitlab.com/mukn/glow-mooc)and several new types of smart contracts.



### Ecosystem Fit

Product Fit for Substrate:

Substrate provides a great platform to build the necessary lower-level layers of blockchain infrastructure: cryptography, gossip, consensus, scaling, elementary accounting, token economics, isolated virtual machine evaluation, etc. With Glow, we are focusing on higher-level layers of functionality: interactions between distrusting human participants, contract-level resource-preservation, automating the use of escrows, collaterals, timeouts, game theory, atomic transactions, etc.

We believe there is a great complementarity between our approaches, and that together we can build a complete product that is robust underneath, while providing users with a language embodying the concepts that matter to them: resources being managed and traded between multiple participants. The combination would provide enhanced security and usability compared to the alternatives.

We intend to port it to the Polkadot ecosystem targeting Polkadot’s language to generate Substrate scripts and Rust client code.


### Background on Glow / Relevance to Polkadot

Glow is a Domain-Specific Language (DSL) to develop secure Decentralized Applications (DApps) on the blockchain. Unlike existing languages, Glow covers much more than a DApp’s “smart contract”: the Glow compiler also generates crucially matching client code, and a logical model of your DApp so you can prove it correct. Formal methods are not an afterthought in Glow, they are built into the language and its implementation. Furthermore, Glow’s logic is designed to deal with the inherently adversarial aspect of DApps, that existing formal tools blatantly overlook. Underlying Glow is an architecture that in the future will make it possible to prove correctness of Glow itself, and can later grow into a complete DApp Operating System. Mutual Knowledge Systems, Inc. is developing Glow as an Open Source platform, with an ambitious Business Model to become the go-to company for all blockchain developments.

*Glow* on Polkadot

While the *Glow* language is portable across blockchains,
the *Glow* compiler needs to be adapted to Polkadot.
We intend to port it to the Polkadot ecosystem targeting Polkadot’s language to generate Substrate scripts and Rust client code. Our initial port will take two months and support the elementary subset of features of our language, and will enable testing of simple DApps end-to-end on Polkadot. This project will open the Polkadot ecosystem to all the applications that in the future can be written portably in *Glow*.

Deliverable: Upon completion of the project, we will deliver a working demo of DApps written in *Glow*, running on Substrate, with documentation and a nix recipe to deterministically reproduce the demo.
Our compiler and runtime are published under the Apache 2.0 license. All work we do to support Polkadot support will be included under the same license

## Team :busts_in_silhouette:

### Team Members

* **François-René Rideau:** Team leader, Co-Founder, Chief Executive Officer
* **Alexander Smart:** Co-Founder, Chief Operating Officer
* **Gauthier Lamothe:** Co-Founder, Chief Communications Officer
* **Alexander Plotnick:** Developer
* **Drew Crampsie:** Senior Developer
* **Alexander Knauth:** Junior developer
* **Emeka Nwanko:** Developer


### Contact

* **Contact Name:** François-René Rideau
* **Contact Email:** fare@mukn.io
* [**Glow Website**](https://glow-lang.org)
* [**Mutual Knowledge Systems Website**](https://mukn.io)

### Legal Structure

* **Registered Address:** Mutual Knowledge Systems, Inc. is a Delaware C corporation with its main office at 12 Aldwin Road, Boston, MA 02131, USA.
We are three co-founders, and are looking to raise money,
but without too much haste for we are currently cashflow positive.

* **Registered Legal Entity:**  We at Mutual Knowledge Systems, Inc. envision a world where everyone uses blockchains for commercial and financial transactions. In this world, simple auditable DApps maximize how much users can trust the system while minimizing how much they need to trust other users. And our *Glow* language helps make DApps orders of magnitude simpler and more auditable.

### Team's experience

* **François-René Rideau** (team leader): Co-Founder
François-René has been making programming languages and distributed systems usable for 25 years. Alumnus of the École Normale Supérieure, Former Senior Engineer at ITA Software, he also worked at Google and Bridgewater Associates. While working in the industry, he notably maintained and rewrote ASDF, the build system at the heart of the Common Lisp open source community; he also kept publishing academic papers and speaking at programming language conferences. Early in his career, he even proved in Coq the correctness of a (centralized) payment protocol. Eventually, his interests in economics and software security converged with his experience in open source software and formal methods and he started working on Layer 2 solutions for the Blockchain. Since January 2018, he has made plenty of mistakes as co-founder of startups, and learned the hard way to become his own CEO.

* **Alexander Smart**: Co-Founder
Co-Founder, has always thought fast, but learned to think deep and sharp at UChicago. After studying law at Pepperdine, he spent nearly fifteen years guiding executives and decision makers through litigation, in matters ranging from shoplifting and speeding tickets to multi-forum international investment bank disputes. His practice honed his ability to quickly assimilate and master new information, and deliver that information clearly at any level of sophistication. Tiring of courthouses, he found his skills were readily applicable and desperately needed in the blockchain space. 

* **Gauthier Lamothe**: Co-Founder
Gauthier has been a seasoned coach, psychotherapist and instructor in communication and management. He doubled his career as a media expert (film and software producer, then e-marketing manager).
He participated in a few blockchain projects, for entities such as the Free Republic of Liberland, and worked on decentralized justice systems, tokenization of governance, and of course crypto-currencies.
His work in the MuKn ecosystem is to take care of every aspect related to communications and human issues, both within the company and with customers and partners, for awareness of human-related safety risks are often dramatically underestimated in the blockchain space. 

* **Alexander Plotnick:** Developer
A Ph.D in computer science from Brandeis University, Alex is an experienced and versatile programmer. He has worked on natural language processing systems, machine learning, embedded systems, and programming language design & implementation.
His skills include natural language processing, machine learning and neural networks, knowledge representation and automated inference, and many programming languages such as (Rust, JavaScript, Java, Ruby, Python, Tcl, Perl, Prolog, C, Forth, Lisp, Fortran, Assembly)

* **Drew Crampsie:** Developer
Drew is an independent system developer with over 20 years of experience in designing, implementing and maintaining Internet based applications and servers with a focus on "bleeding edge" Web Apps. Drew is a seasoned user in non-mainstream and mainstream techs and languages (Scheme, Common Lisp, SQL, Javascript, C...).

* **Emeka Nwanko:** Developer
2005 Alumnus from Nnamdi Azikiwe University. Worked for several companies as a Field Engineer or Operations Manager, such as Schlumberger Nigeria or Northern Oilfield. Also worked for Satajanus Nigeria Limited as a software developer in the field of Blockchain industry, both in C# and F#, but also in Rust and Solidity. Also a teacher. 

* **Alexander Knauth:** Junior Developer
Alex has already co-authored two notable papers and contributed to the Racket ecosystem. His previous work on combining types and macros is directly relevant to building our compiler.

* **Noel Kwan:** Intern Developer
Sophomore at the National University of Singapore, Noel already holds significant experience in Haskell, Javascript, and Rust. He also has a strong understanding of AWS systems, NixOS and even full-stack web development. He already developed a DSL, a chat-server application, and worked on several projects as a software engineering intern previously.


### Advisors and Partners

* **Nada Amin**:  namin.seas.harvard.edu 
* [**Rick Dudley**](https://www.linkedin.com/in/afdudley/)
* [**Dominik Franek**](http://dominikfranek.com/)


### Team Code Repos

* [Glow](https://gitlab.com/mukn/glow)
* [François-René Rideau](https://github.com/fare)
* [Alexander Plotnick](https://github.com/plotnick)
* [Alexander Knauth](https://github.com/AlexKnauth)
* [Ian Denhart](https://gitlab.com/users/isd)
* [Noel Kwan](https://github.com/kwannoel)


### Team LinkedIn Profiles

* [François-René Rideau](https://www.linkedin.com/in/fahree)
* [Alexander Smart](https://www.linkedin.com/in/alexandersmart)
* [Gauthier Lamothe](https://www.linkedin.com/in/gauthier-lamothe/)

## Development Status :open_book:

Development for *Glow* is currently funded for the next few months.
Upcoming features include a user-friendly web-browser [UI](https://www.youtube.com/watch?v=0ltm6RmyDnM), and several other types of smart contracts.  We are also currently developing a [MOOC](https://gitlab.com/mukn/glow-mooc)


## Development Roadmap :nut_and_bolt:


### Overview

* **Total Estimated Duration:** 3 months
* **Full-time equivalent (FTE):** 1.5
* **Total Costs:** $30,000 USD

### Milestone 1 — Bridge *Glow* and Substrate

* **Estimated Duration:** 1.5 
* **FTE:** 1.5
* **Costs:** $15,000 USD

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 1 | Onboarding | Having a developer get familiar with the relevant parts of both *Glow* and Substrate |
| 2 | Experimentation | Having the developer run lots of small manual tests to determine how exactly to match the concepts of *Glow* and Substrate together. |
| 3 | Substrate module for *Glow* runtime support | We will create a Substrate module (in Rust) that will interface with the *Glow* runtime (in Scheme) such that *Glow* can interface with Substrate chains, send transactions, create contracts, send messages to contracts, watch messages received by contracts, and marshal data between Substrate and *Glow*. |
| 4 | Slack | Handle unforeseen difficulties in the above |

### Milestone 2 — *Glow* Language Backend Targeting Substrate

* **Estimated Duration:** 1 month
* **FTE:** 1.5
* **Costs:** $15,000 USD

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an article/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)|
| 1 | *Glow* backend into Substrate smart contracts | We will create passes for the *Glow* compiler and support in the *Glow* runtime so that existing *Glow* programs can be compiled on a Substrate chain. |
| 2 | Test environment | We will provide a deterministic build using Nix or GUIX, from which a docker image can be generated that can reliably run tests for CI/CD in gitlab |
| 3 | Documentation | We will update the documentation of *Glow* with explanations on how to deploy our DApps on a relevant test or production Substrate chains. |
| 4 | Slack | Handle unforeseen difficulties in the above |

## Future Plans

We will publish progress reports on our Blog on https://mukn.io,
including a variant of our [tutorial](https://glow-lang.org/docs/Glow_Tutorial.html) especially targeting using Polkadot test and production networks. 

We are also currently developing a [MOOC](https://gitlab.com/mukn/glow-mooc).


## Additional Information :heavy_plus_sign:


### Bibliography

Our domain specific language, *Glow*,
was designed by our Co-Founder François-René Rideau,
formerly a researcher in Programming Language Semantics and Distributed Systems.

An extensive bibliography about the design and implementation of *Glow*,
Including related present and past works by its authors, is available
[on our wiki](https://gitlab.com/mukn/glow/-/wikis/Bibliography/Glow).

### [Some Simple DApps in *Glow*](https://gitlab.com/mukn/glow/-/tree/master/dapps)


### Appendix B: [Comparison between the same contract in *Ink!* vs. *Glow*(https://gitlab.com/mukn/glow/-/wikis/Competition/Ink!)