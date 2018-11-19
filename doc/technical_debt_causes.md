# Software technical debt causes

* Business pressures: where the business considers getting something released sooner before all of the necessary changes are complete, builds up technical debt comprising those uncompleted changes.
* Lack of process or understanding: where businesses are blind to the concept of technical debt, and make decisions without considering the implications.
* Lack of building loosely coupled components: where functions are not modular, the software is not flexible enough to adapt to changes in business needs.
* Lack of a test suite: which encourages quick and risky band-aids to fix bugs.
* Lack of documentation: where code is created without necessary supporting documentation. That work to create the supporting documentation represents a debt that must be paid.
* Lack of collaboration: where knowledge isn't shared around the organization and business efficiency suffers, or junior developers are not properly mentored.
* Parallel development: at the same time on two or more branches can cause the buildup of technical debt because of the work that will eventually be required to merge the changes into a single source base. The more changes that are done in isolation, the more debt that is piled up.
* Delayed refactoring: as the requirements for a project evolve, it may become clear that parts of the code have become unwieldy and must be refactored in order to support future requirements. The longer that refactoring is delayed, and the more code is written to use the current form, the more debt that piles up that must be paid at the time the refactoring is finally done.
* Lack of alignment to standards: where industry standard features, frameworks, technologies are ignored. Eventually, integration with standards will come, doing sooner will cost less (similar to 'delayed refactoring').
* Lack of knowledge: when the developer simply doesn't know how to write elegant code.
* Lack of ownership: when outsourced software efforts result in in-house engineering being required to refactor or rewrite outsourced code.
* Poor technological leadership: where poorly thought out commands handed down the chain of command increases the technical debt rather than reduce it
* Last minute specification changes: these have potential to percolate throughout a project but no time or budget to see them through with documentation and checks
* Scope Doping: unmanaged scope reduction or shedding of scope by project managers, or indeed technical staff. Subtly different to Business pressures in that, while business pressures may be a cause, Scope Doping will also cause business pressure due to unmanaged work scope that has been shed.
