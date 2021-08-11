# General Grant Proposal

* **Project Name: Name** *Glow*: Simple, Secure DApp DSL
* **Team Name: Name** [Mutual Knowledge Systems, Inc.](https://mukn.io)
* **Payment Address:** (BTC) bc1qma9gmt7njg0pjftv3grpgj7l052j0d2f6a4zxh

## Project Overview :page_facing_up:

### Overview

We propose to port our programming language *Glow* to the Polkadot platform.
This three-month, $30,000 project will enrich the Polkadot platform
with a uniquely high-level portable language
that will bring its applications, users and developers to Polkadot.

In the short run, the project will benefit Polkadot by allowing its users
to use our cross-platform language, from which our compiler generates
matching smart contract and client/server code for financial interactions.
In the long run, our formal verification will drastically reduce the risks, and
layer2-aware code generation will help safely scale transactions and reduce fees,
thus making Polkadot a competitive blockchain for any smart contract-based business.

The proposed port would be a proof of concept of the *Glow* language on Polkadot.
If we demonstrate to the value of our language to the satisfaction of the Polkadot team,
we expect that further work will be funded to robustly support
the entire feature set of Polkadot.

#### Relevance to Polkadot

Polkadot is building the ultimate toolkit with which to build
blockchains and their applications. The potential is enormous.
But most DApp developers cannot and will not deal with the underlying complexity.
They want to be able to focus on the business problem they are innovating on,
from which any extraneous blockchain detail is a distraction:
selling or trading digital assets,
notarizing of large data sets,
synthetizing composite and derivative assets,
insuring property, etc.
*Glow* enables these DApp developers to leverage the power of the Polkadot platform
without having to delve into blockchain details
and it enables Polkadot builders to offer new features to these DApp developers
without requiring them to rewrite their DApps.
*Glow* offers a better division of labor between these builders and developers,
thereby increasing the value of the platform.

Compared to using Solidity or Ink! combined with JavaScript,
*Glow* provides a higher level of abstraction:
it automates a lot of error-prone drudgery in writing DApps,
making them both easier and safer to write, in much the same way that
Solidity or Ink! provide a higher level of abstraction than
writing in EVM or WebAsm, or that Python is higher level than C.
And much like Solidity, Ink! or Python don't make
the EVM, WebAsm or C disappear, *Glow* will not make Ink! disappear.
Instead, *Glow* will complement and extend Ink!, and displace it
from many use cases where developers want to focus on higher level concepts,
while developers keep using Ink! when dealing with
lower level aspects of their DApps.

This project will benefit Polkadot by making it a much more accessible platform
to target for a whole range of DApps that
*Glow* makes easier and safer to write.

### Project Details

#### Introduction: The Difficulty of Writing DApps

DApps are interactions between multiple mutually distrusting parties,
who exchange digital assets based on algorithmically verifiable rules
enforced by blockchain smart contracts.

DApps are extremely hard to write, because one single small bug
in the blockchain-facing part of a DApp can cause users to lose
tens of millions of dollars worth of digital assets, with no recourse.
Moreover, all the critical code and data involved in a DApp must be public
for it to be trusted by all participants—there is no possibility to hide
and guarded secrets to achieve security. Instead, there is an active
community of online predators eager to exploit any flaw to extract a fortune.

It is not just the on-chain smart contract that is at stake,
but also the off-chain client and server code running on the users' machine.
If that off-chain code fails to be not only correct on its own, but
also perfectly in synch with on-chain contract,
then the affected users also stand to lose their assets.

Moreover, this code is extremely hard to maintain:
even if one version of a DApp is bug-free,
small changes, to the code itself or to the context in which it is used,
can introduce subtle yet deadly bugs in any of the many parts of the DApp,
or in the way they interact with each other.
Such changes are themselves made necessary by a changing world.

#### The *Glow* Language: Safer, Cheaper DApps

[*Glow*](https://glow-lang.org) is
a domain-specific (programming) language for Decentralized Applications (DApps).
Compared to competing DApp languages, *Glow* provides much higher-level abstractions,
that make DApp development not only drastically simpler,
but also portable and amenable to formal verification.
With *Glow*, DApps will be much cheaper and faster to develop and to use,
but also, importantly, to audit and to trust—and thus safer in the end.

The *Glow* compiler automatically enriches a DApp with details like
intermediate transactions, timeouts, and collaterals.
It can emit code in “direct style” as typically followed by
humans writing DApps today, but also for “generalized state channels”
that allow for scalable private contracts.
The *Glow* compiler then generates not just a “smart contract” for a DApp,
but also matching client and server code.

Last but not least, *Glow* is designed to generate a logical model of the DApp.
The model notably uses Game Semantics to allow formal verification of security
properties in the adversarial environment of permissionless blockchains.
The model can then checked using a theorem prover such as Z3,
and DApps that do not pass all checks can be automatically rejected.
Entire classes of bugs thus disappear when using the *Glow* language,
that today cost millions of dollars in development
and/or operating losses to companies deploying DApps.

#### Relevance to Substrate & Polkadot

Substrate has got *Ink!*, a great language for contracts at the relatively low-level.

But it is missing a good higher-level language:

- A language with a builtin in notion of participant roles behind any action,
  thereby eliminating bugs due to missing or reversed authorization checks.

- A language that can express control flows across many transactions,
  including handling of timeouts when a participant fails to act as agreed.

- A language that from a single specification can generate not only a contract
  but also matching client/server code, and furthermore a formal model.

This port of *Glow* will spearhead the ability for Polkadot to host
DApps written in languages at a higher level of abstraction than its native Ink!.
Note that *Glow* does not aim at replacing Ink!
Instead, it will offer a higher point of view better suited
for a large class of DApps.

Since our approach innovates in many ways, porting *Glow* to Polkadot
might suggest changes to the Polkadot platform and its documentation.
These changes won’t be discovered until the attempt is completed,
yet may help the Polkadot ecosystem evolve toward effective
feature parity or superiority compared to its rivals
on the dimensions that matter to DApp development.
We notably sent a lot of feedback to the maintainers of Ethereum Classic and
Cardano when we ported our language to their respective platforms.

#### Team Motivation

We seek to empower humans to build secure decentralized applications
that are scalable, usable and robust enough to be used by regular consumers,
yet with drastically reduced costs and risks compared to existing solutions.

Our values include a commitment to open-source technologies, and to creating
synergies between people with a variety of complementary points of view.

Our team has notable expertise in game theory, computer science and economics,
that we want to share with the community.

#### *Glow* So Far

The first version of *Glow* was released in February 2021, and can work on
either the Ethereum Virtual Machine (EVM), or Cardano's Plutus ecosystem.
Documentation for *Glow* is available at https://glow-lang.org/docs/

[Mutual Knowledge Systems, Inc.](https://mukn.io), a.k.a. MuKn (pronounced “Moon”),
has been developing *Glow* for almost two years,
based on a prototype previously developed by one of its co-founders.
We are committed to ever growing the language and its ecosystem.

### Ecosystem Fit

Substrate provides a great platform to build the necessary lower-level layers
of blockchain infrastructure:
cryptography, gossip, consensus, scaling, elementary accounting, token economics,
isolated virtual machine evaluation, etc.
With *Glow*, we are focusing on higher-level layers of functionality:
interactions between distrusting human participants,
contract-level resource-preservation,
automating the use of escrows, collaterals and timeouts,
game theory, atomic transactions, etc.

We believe there is a great complementarity between our approaches, and that
together we can build a complete product that is robust underneath, while
providing users with a language embodying the concepts that matter to them:
resources being managed and traded between multiple participants.
The combination would provide enhanced security and usability
compared to the alternatives.

### Background on *Glow*

The *Glow* language itself is portable to any smart contract capable blockchain.
However, the compiler for *Glow* needs to be adapted
to each of the targetted blockchains.
We intend to port *Glow* to the Polkadot ecosystem in a way that uses
the existing Polkadot development toolchain and integrates with it.

Our initial port will take two months,
and support an elementary subset of features of our language.
It will enable testing of simple DApps end-to-end on Polkadot.
This project will open the Polkadot ecosystem to all the applications
that in the future can be written portably in *Glow*.

### Deliverable

Upon completion of the project, we will deliver a working demo
of DApps written in *Glow*, running on Polkadot,
with documentation and a guix recipe to deterministically reproduce the demo.

Our compiler and runtime are published under the Apache 2.0 license.
All work we do to support Polkadot will be included under the same license.

## Team :busts_in_silhouette:

### Team Members

* **François-René Rideau:** Team leader, Co-Founder, Chief Executive Officer
* **Alexander Smart:** Co-Founder, Chief Operating Officer
* **Gauthier Lamothe:** Co-Founder, Chief Communications Officer
* **Alexander Plotnick:** Developer
* **Drew Crampsie:** Senior Developer
* **Alexander Knauth:** Junior developer

### Contact

* **Contact Name:** François-René Rideau
* **Contact Email:** fare@mukn.io
* [**Glow Website**](https://glow-lang.org)
* [**Mutual Knowledge Systems Website**](https://mukn.io)

### Legal Structure

* **Registered Address:**
Mutual Knowledge Systems, Inc.
is a Delaware C corporation with its main office at
12 Aldwin Road, Boston, MA 02131, USA.
We are three co-founders, and are looking to raise money,
but without too much haste for we are currently cashflow positive.

* **Registered Legal Entity:**
We at Mutual Knowledge Systems, Inc. envision a world where
everyone uses blockchains for commercial and financial transactions.
In this world, simple auditable DApps maximize how much users can trust the
system while minimizing how much they need to trust other users.
And our *Glow* language helps make DApps orders of magnitude simpler and
more auditable.

### Team's experience

* **François-René Rideau** (Co-Founder, Architect):
François-René has been making programming languages and distributed systems
usable for 25 years.
Alumnus of the École Normale Supérieure,
Former Senior Engineer at ITA Software,
he also worked at Google and Bridgewater Associates.
While working in the industry, he notably maintained and rewrote ASDF,
the build system at the heart of the Common Lisp open source community;
he also kept publishing academic papers and
speaking at programming language conferences.
Early in his career, he even proved in Coq
the correctness of a (centralized) payment protocol.
Eventually, his interests in economics and software security converged with
his experience in open source software and formal methods and
he started working on Layer 2 solutions for the Blockchain.
Since January 2018, he has made plenty of mistakes as co-founder of startups,
and learned the hard way to become his own CEO.

* **Alexander Smart** (Co-Founder, COO):
Alexander has always thought fast, but learned to think deep and sharp
at UChicago. After studying law at Pepperdine, he spent nearly fifteen years
guiding executives and decision makers through litigation, in matters ranging
from shoplifting and speeding tickets
to multi-forum international investment bank disputes.
His practice honed his ability to quickly assimilate and master new information,
and deliver that information clearly at any level of sophistication.
Tiring of courthouses, he found his skills were readily applicable and
desperately needed in the blockchain space.

* **Gauthier Lamothe** (Co-Founder, CCO):
Gauthier has been a seasoned coach, psychotherapist and instructor in communication and management. He doubled his career as a media expert (film and software producer, then e-marketing manager).
He participated in a few blockchain projects, for entities such as the Free Republic of Liberland, and worked on decentralized justice systems, tokenization of governance, and of course crypto-currencies.
His work in the MuKn ecosystem is to take care of every aspect related to communications and human issues, both within the company and with customers and partners, for awareness of human-related safety risks are often dramatically underestimated in the blockchain space.

* **Alexander Plotnick** (CTO):
A Ph.D in computer science from Brandeis University,
Alex is an experienced and versatile programmer.
He has worked on natural language processing systems, machine learning,
embedded systems, and programming language design & implementation.
His skills include natural language processing, machine learning and
neural networks, knowledge representation and automated inference, and
many programming languages (Rust, JavaScript, Java, Ruby, Python,
Tcl, Perl, Prolog, C, Forth, Lisp, Fortran, Assembly…).

* **Drew Crampsie** (Developer):
Drew is an independent system developer with over 20 years of experience in
designing, implementing and maintaining Internet based applications and servers
with a focus on "bleeding edge" Web Apps.
Drew is a seasoned user in non-mainstream and mainstream techs and languages
(Scheme, Common Lisp, SQL, Javascript, C…).

* **Alexander Knauth** (Junior Developer):
Alex has already co-authored two notable papers and
contributed to the Racket ecosystem.
His previous work on combining types and macros
is directly relevant to building our compiler.

* **Noel Kwan** (Intern Developer):
Sophomore at the National University of Singapore, Noel already holds
significant experience in Haskell, Javascript, and Rust. He also has a strong
understanding of AWS systems, NixOS and even full-stack web development.
He already developed a DSL, a chat-server application, and worked on
several projects as a software engineering intern previously.

### Advisors and Partners

* [**Nada Amin**](https://namin.seas.harvard.edu/)
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

Our current Docker image is based on Nix, and we have a new one in progress
based on Guix.

Upcoming features include
a user-friendly web-browser [UI](https://www.youtube.com/watch?v=0ltm6RmyDnM),
a [MOOC](https://gitlab.com/mukn/glow-mooc), and
several new types of smart contracts.

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
| ------------- | ------------- | ------------- |
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
| ------------- | ------------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide both inline documentation of the code and a basic tutorial that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| 0c. | Testing Guide | Core functions will be fully covered by unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| 0d. | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an article/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.)|
| 1 | *Glow* backend into Substrate smart contracts | We will create passes for the *Glow* compiler and support in the *Glow* runtime so that existing *Glow* programs can be compiled on a Substrate chain. |
| 2 | Test environment | We will provide a deterministic build using Nix or GUIX, from which a docker image can be generated that can reliably run tests for CI/CD in gitlab |
| 3 | Documentation | We will update the documentation of *Glow* with explanations on how to deploy our DApps on a relevant test or production Substrate chains. |
| 4 | Slack | Handle unforeseen difficulties in the above

## Future Plans

We will publish progress reports on our Blog on < https://mukn.io >,
including a variant of our [tutorial](https://glow-lang.org/docs/Glow_Tutorial.html)
especially targeting using Polkadot test and production networks.

We are also currently developing a [MOOC](https://gitlab.com/mukn/glow-mooc).

## Additional Information :heavy_plus_sign:

### Bibliography

Our domain specific language, *Glow*,
was designed by our Co-Founder François-René Rideau,
formerly a researcher in Programming Language Semantics and Distributed Systems.

An extensive bibliography about the design and implementation of *Glow*,
including related present and past works by its authors, is available
[on our wiki](https://gitlab.com/mukn/glow/-/wikis/Bibliography/Glow).

### Sample DApps

[Some Simple DApps in *Glow*](https://gitlab.com/mukn/glow/-/tree/master/dapps)

[Comparison between the same contract in *Ink!* vs. *Glow*](https://gitlab.com/mukn/glow/-/wikis/Competition/Ink!)
