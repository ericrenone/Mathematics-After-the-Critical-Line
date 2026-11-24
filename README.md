# Mathematics After the Critical Line

## 2027 Outlook: How the Riemann Hypothesis Fell, What It Changes, and Where the Next Twelve Months Go

**ERI Labs · Eric Ren · Jersey City, New Jersey · November 2026 edition**

---

### At a glance

| | |
|---|---|
| **The event** | The Riemann Hypothesis, open since 1859, and the Generalized Riemann Hypothesis for Dirichlet L-functions were proved on November 20, 2026 and independently certified on November 21, 2026. |
| **The form** | ~17.4 million lines of machine-checked Lean code in 175,187 files. No human-readable paper. A 250,000-page prose draft was withheld as unreadable. |
| **The authors** | A human number theorist who chose the strategy, and a frontier AI model that found the decisive step and finished the argument. Elapsed time from first idea to final theorem: 41 days. |
| **The surprise** | Every public forecast was wrong by a decade or more. The consensus horizon in October 2026 was 2035–2050. |
| **The second proof** | A 940-page, twelve-year, all-human draft of a broader statement appeared the same afternoon by an unrelated route. It is unfinished and currently carries roughly 750 documented errata. |
| **What is still open** | Whether anyone can explain *why* the theorem is true; whether the proof extends to the wider families of L-functions; whether the $1 million prize can be awarded to a proof no journal has published; and what research mathematics looks like when a Millennium Problem falls in six weeks. |

---

## Executive summary

**1. The question changed from "if" to "why" in a single weekend.** Since 1859 the Riemann Hypothesis organized analytic number theory as a conditional discipline: hundreds of theorems began "assuming RH." As of November 21, 2026, those theorems are unconditional, the de Bruijn–Newman constant is exactly zero, and the question that remains is explanatory: no operator, no spectral interpretation, no human narrative yet accounts for the result. The field's center of gravity moves from proving the hypothesis to understanding a theorem.

**2. The decisive capability was synthesis across registers, not invention.** The proof transplants a 1969 elementary argument from curves over finite fields into the integers, using machinery (theta correspondences, Arakelov slopes, Iwasawa theory) built for other purposes. The partial result six weeks earlier (the quasi-Riemann Hypothesis, via metaplectic forms) was described by its human readers as introducing no new concepts. The pattern across 2026 is consistent: frontier models win by connecting known structures that human specialization had kept apart. Organizations planning around "AI cannot create genuinely new mathematics" planned around the wrong constraint.

**3. Verification, not discovery, became the scarce institutional asset.** The certificate was issued by an independent open-source community in under 24 hours, against a published four-point checklist, using multiple independently written proof checkers. The AI lab that employed the author played no role in certification. The 940-page human draft, released without formal verification, was found to contain hundreds of errors within 72 hours by AI-assisted readers and volunteer formalizers. The lesson for every institution that validates knowledge: the formal check is now the entry ticket; prose is commentary.

**4. Research mathematics has bifurcated, and both cultures are productive.** The two November 20 proofs were posted hours apart by people who had never coordinated: one AI-integrated and Lean-only, one human-only and prose. Human mathematicians re-proved the August AI result by hand within a month; volunteer formalizers are now applying AI tooling to the human draft. Neither culture is disappearing. Funders, departments and journals that have organized for one will need to serve both.

**5. Forecasting horizons compressed by an order of magnitude in eleven weeks.** Three Millennium-class events (a claimed Navier–Stokes resolution in September, the quasi-RH in October, RH in November) arrived between 1 and 3 months after the first indication, in August, that frontier models had crossed a threshold. Even the shortest published horizon for RH (2031) was four years too long. Any 2027 plan that assumes the current pace is a plateau should be treated as the optimistic case for incumbents, not the base case.

**6. The twelve-month outlook is defined by five resolutions.** (i) Whether a human-readable account of the proof is accepted by experts, deciding if "alien proof" was a season or a permanent condition. (ii) Whether the route extends to Hecke and Dedekind L-functions, closing the gap between the certified theorem and the colloquial meaning of "GRH." (iii) Whether the human trace-formula draft is repaired, which would deliver the first spectral explanation. (iv) Whether a qualifying venue publishes a Lean-only proof, starting the prize clock. (v) Whether the next problem to fall is one anyone predicted.

---

## Part I — What happened

### Exhibit 1. The 2026 compression

| Date | Event | Form | Who |
|---|---|---|---|
| Aug 10 | Proportion of zeta zeros known on the critical line raised from 41.6% to 67.2% | Lean + preprint | Unreleased research model, prompted by a non-mathematician; reviewed by four mathematicians |
| Sep 2 | Human re-proof of the 67.25% bound by a simpler argument | arXiv | Lamzouri |
| Sep 8 | Claimed finite-time blowup for 3D Navier–Stokes with smooth forcing; credit dispute | Lean + 166-page manuscript | AI lab (≈10,000 agents, 88 hours); competing Lean-checked results from two human-led teams the same week |
| Sep 30 / Oct 6 | Quasi-Riemann Hypothesis: all nontrivial zeros of ζ and Dirichlet L-functions have real part in [1/8, 7/8] | Lean (199 pp.) + human-studied 49-page version | AI lab internal model; one of 722 released results |
| Oct 8–Oct 26 | Follow-on zero-free regions for Hecke and Dedekind families; multiple independent Lean formalizations | arXiv + Lean | Human mathematicians and a formal-math startup |
| Oct 6 → Nov 16 | The Riemann Hypothesis proof, from first idea ("Stepanov determinant") to GRH | Lean | One human number theorist with a frontier model |
| Nov 12 | A four-question checklist for trusting any "checked in Lean" claim is published | Blog post | Imperial College mathematician |
| Nov 20 (a.m.) | RH and Dirichlet GRH released: four-page note + 14 Lean archives | Lean only | Alpöge with Claude |
| Nov 20 (p.m.) | 940-page human draft of GRH for all Hecke L-functions released early | Manuscript | Masullo; posted by Vakil |
| Nov 21 | Joint certification by the Lean FRO and the Mathlib Initiative; independent verification ledger published | Statement + ledger | Open-source community; MIT |
| Nov 21–24 | Three third-party reconstructions (164, ~70 and 66 pages); public errata file for the human draft passes 750 entries | PDFs + GitHub | Waterloo, IHÉS, Arizona State; volunteer formalizers |

**Reading the exhibit.** The interval between "a model improved a 15-year-old bound" and "a model co-authored a proof of the most famous open problem in mathematics" is 102 days. The interval between release and certification of that proof is roughly 24 hours. The interval between release and the first documented errors in the competing human draft is roughly 8 hours.

### Exhibit 2. What was forecast, and when it actually happened

| Forecaster | Date of forecast | Forecast horizon for RH | Error |
|---|---|---|---|
| Leading analytic number theorist (public interview) | Oct 2026 | ~2050, humans and AI together | ~24 years |
| Community forecasting platform (median) | pre-Nov 2026 | ~May 2035 | ~8.5 years |
| The AI lab that employed the eventual author (public research note) | Aug 10, 2026 | Did not expect its model's techniques to lead to a proof | Correct about the technique; silent on the horizon |
| Senior number theorist, post-event | Stated Nov 21 | Had privately expected "several years" | ≥ 2 years |
| ERI Labs | Aug 11 / Aug 23, 2026 | Not before 2031 | ≥ 4 years |
| **Actual** | | **Nov 21, 2026** | |

**Reading the exhibit.** The shortest public horizon was still four years too long. The forecasting failure was not one of optimism versus pessimism; it was structural. Every forecaster, including those who correctly predicted the *mechanism* (cross-register synthesis, Lean-only output, machine certification), exempted this specific problem from that mechanism. The single accurate statement on the public record before November was that *which* problem falls next is unpredictable from the mechanism alone.

### Exhibit 3. Anatomy of the proof that arrived

| Layer | What it is | Why it mattered |
|---|---|---|
| **Target statement** | A one-sided upper bound on a smoothed prime sum, G(x) ≤ x^{1/2+η}, needed only on sparse intervals | Reduces RH to a single inequality; the functional equation handles the other half of the strip |
| **Seed idea (Oct 6)** | A determinant playing the role of Stepanov's auxiliary polynomial: divisibility of an integer bounds its size, size bounds the primes | The 1969 finite-field argument, recognized as applicable over the integers |
| **The obstruction** | Stepanov needs *multiplicity* (vanishing to high order), which requires differentiation; there is nothing to differentiate in the whole numbers | The reason this route was considered closed for fifty years |
| **The breakthrough (Nov 15)** | Multiplicity manufactured by composing a chain of ≈√X theta lifts between definite unitary groups over a CM field | Found by the model; the human author reports limited expertise in this machinery |
| **Size control** | Bost's slope inequality; covolume bounds via Hodge bundles on moduli of CM abelian varieties; Petersson norms via special L-values | Existing Arakelov-geometric tools, repurposed |
| **Denominator control** | Congruences between Galois representations; Selmer-group bounds via Tate–Poitou, Taylor–Wiles, Kato's Euler system; vanishing of the Iwasawa μ-invariant | Existing arithmetic tools, repurposed |
| **The near-miss** | With a cruder error accumulation along the chain, the argument stops at exponent 2/3 (a zero-free region, not RH); the author's timeline records this a priori stopping point | The proof passed through the quasi-RH regime on its way to the line |
| **Human contribution** | Problem selection; two ideas in a toy setting; recognition of the Stepanov structure in a competitor's release; steering to the right setting | Strategy and taste |
| **Model contribution** | The key step, the chain length, the automorphic-forms execution, the formalization, the timeline itself | Execution across registers the human did not command |

**Reading the exhibit.** No layer of this proof is new technology. Every tool existed; several were decades old. The achievement is the *path*, and the path required holding automorphic forms, Arakelov geometry, Iwasawa theory and elementary point-counting in one working memory at once. That is precisely the capability human specialization selects against and frontier models select for.

## Part II — Six shifts that will define 2027

### Shift 1. From conditional to explanatory mathematics

For a century, analytic number theory maintained two ledgers: results proved outright, and results proved "under RH." On November 21 the second ledger was merged into the first. The consequences are immediate and mostly mechanical (Exhibit 4), but the strategic consequence is a change in what counts as a contribution. Proving something *assuming* RH is no longer a research output. Explaining *why* RH holds is now the open problem, and it is a different kind of problem: there is a certified answer and no account of it.

#### Exhibit 4. Immediately unconditional, as of November 21, 2026

| Result | Previously | Now |
|---|---|---|
| Prime number theorem error term ψ(x) = x + O(√x log² x), with explicit constants | Conditional on RH | Theorem |
| Prime gaps p_{n+1} − p_n ≪ √p log p | Conditional on RH | Theorem |
| Lindelöf bound for ζ and Dirichlet L-functions | Conditional | Theorem |
| Non-existence of Siegel zeros; effective constants replacing Siegel's ineffective theorem | Conditional on Dirichlet GRH | Theorem |
| Least prime in an arithmetic progression ≪ φ(q)² log² q | Conditional on Dirichlet GRH | Theorem |
| Miller's deterministic polynomial-time primality test | Conditional on Dirichlet GRH | Unconditional algorithm |
| de Bruijn–Newman constant | 0 ≤ Λ ≤ 0.22 | Λ = 0 exactly |
| Artin's primitive-root conjecture | Conditional on GRH for Dedekind zeta functions of Kummer fields | **Still conditional** (outside the certified scope) |

**What to expect in 2027.** A wave of short papers converting conditional results to unconditional ones, most of them trivial, a few of them not (where the conditional proof assumed a GRH broader than the one certified). A sharper separation between "GRH" as proved (Dirichlet characters) and "GRH" as colloquially used (all automorphic L-functions). And a reorientation of the spectral and physical research programs, which no longer need to prove RH and can therefore state their real objective honestly: an operator whose spectrum is the zeros.

### Shift 2. From invention to synthesis as the frontier capability

Three data points from 2026 line up.

- The August proportion result was described by the lab that produced it as recombining existing research (Weil positivity, Montgomery pair correlation, a 2024 unconditional pair-correlation theorem, a 2000 paper of Bombieri).
- The October quasi-RH was described by the human expert closest to its ingredients as an unexpected synthesis of familiar ideas introducing no new concepts; another expert had come near the right family in 2002 and missed it.
- The November proof is a transplant of a 1969 argument through machinery built for other problems; the open question is whether *any* genuinely new theory sits inside the 17 million lines, with estimates ranging from none to on the order of a thousand pages.

The strategic reading is that the binding constraint on frontier mathematics was never a shortage of ideas. It was the cost of holding enough distant ideas simultaneously to see that one was the missing piece of another. That cost has collapsed. Planning assumptions built on "models recombine, humans invent" should be replaced with "models recombine at a scale at which recombination *is* invention."

**What to expect in 2027.** The problems most at risk are those whose solution plausibly lives in an adjacent, well-developed field that the problem's own community does not read. Candidates on the public record include the remaining register-crossing bets (prime gaps below 100; the sunflower conjecture; the chromatic number of the plane; R(5,5)) and the extension of the November route to Hecke and Dedekind L-functions. Problems requiring a genuinely new object remain the harder case, and 2026 produced no clear example of a model inventing one.

### Shift 3. From peer review to formal certification as the gate

The November 21 certification was the first time a Millennium-class claim was validated by (a) a statement that pre-existed the proof in a public library, (b) two independent tools confirming the proof targets that statement, (c) dozens of independent reproductions of the build, and (d) acceptance by several independently written checkers, including two carrying their own formal soundness proofs, run on an inert export that malicious source code could not reach. The entire process took about a day and involved no journal, no editor, and no referee in the traditional sense.

The same weekend produced the control case. A 940-page manuscript by a well-trained mathematician, read privately for months by a leading expert, was released without formalization. Within eight hours AI-assisted readers reported a specific theorem failing at the prime 2 and a basis claim on page 444 that appears false; within three days a volunteer formalization logged roughly 750 errata, including a structure theorem in Chapter 5 whose printed proof does not work and a final chapter containing only placeholders.

**What to expect in 2027.** Formalization becomes a *precondition* for serious attention to any claimed solution of a named open problem, not a post-hoc nicety. Journals face a concrete test case: the only proof of RH that exists is 17 million lines of code, and the prize rules require publication in a qualifying outlet. Expect at least one major venue to announce a formal-proof track or an equivalent instrument in 2027, and expect the first disputes over what "publication" of a Lean library means. Expect, too, a rise in human-readable *interpretation* documents (the three reconstructions of the November proof are the prototype) as a recognized scholarly genre with its own standards, since all three currently describe themselves as conditional, incomplete, or AI-drafted.

### Shift 4. From one research culture to two

The two proofs of November 20 were produced by people who did not coordinate, by routes that do not overlap, in forms that do not translate. One is executable; the other is readable. One was certified in a day; the other may take a year to repair. One carries the name of an AI model as a co-discoverer; the other was released with the explicit statement that no AI was involved.

Three months of evidence suggest both cultures persist and interact. Human mathematicians re-proved the August AI result by a simpler route within four weeks. Volunteer formalizers are now applying Lean to the human draft. A leading number theorist repurposed a graduate course to study an AI-generated proof. The reconstructions of the November proof are human-edited documents built on AI readings of code.

**What to expect in 2027.** Institutions will be forced to choose which culture they serve, and the best ones will serve both. Hiring, tenure and prize committees will encounter the first candidates whose principal output is Lean libraries or interpretation documents rather than papers. Funders will see proposals for formalization infrastructure compete with proposals for traditional research. The professional-identity stress visible in the "wonder and loss" framing of November coverage is the leading indicator of a generational shift in who enters the field and why.

### Shift 5. From institutional prestige to verification credibility

The names attached to the November event, after the author's, are not universities. They are an open-source foundation, a community-maintained library, an independent verifier at MIT who published a public ledger, and the author of the checklist the community used. Credit for *discovery* still flowed to the human who steered (one senior number theorist proposed a Fields Medal); credit for *truth* flowed to the verifiers. The lab that employed the author timed the release after its own public listing and pre-empted the cynical reading in the release note; the certification's independence from the lab is what made that defense credible.

**What to expect in 2027.** Verification capacity becomes a strategic asset for institutions that want to remain relevant to frontier results they did not produce. Expect departments to stand up formalization groups, expect at least one national funder to treat proof-checking infrastructure as research infrastructure, and expect AI labs to invest in independent verification channels precisely because dependence on in-house validation is now a reputational liability.

### Shift 6. From decade-scale to quarter-scale planning horizons

Exhibit 2 shows forecast errors of 4 to 24 years on a single question. Exhibit 1 shows three Millennium-class events in eleven weeks. The compression is not confined to one problem: the August proportion result, the September fluid-dynamics claim, and the October quasi-RH span three unrelated areas of mathematics.

**What to expect in 2027.** Any plan with a multi-year horizon that depends on a named open problem *remaining* open should carry an explicit scenario in which it falls within the planning period. The converse also holds: plans that assume continued acceleration should carry a scenario in which the November result is the high-water mark for some time, because a 41-day proof of RH is consistent both with a new regime and with a one-off alignment of the right human, the right prior release, and the right model.

---

## Part III — Scenarios for 2027

Three scenarios, defined by two uncertainties: whether the November proof becomes *humanly understood*, and whether frontier models produce *further* Millennium-class results. Likelihoods are indicative judgments, not measurements.

#### Exhibit 5. Three scenarios

| | **A. Absorption** | **B. Cascade** | **C. Plateau** |
|---|---|---|---|
| **Indicative likelihood** | ~45% | ~35% | ~20% |
| **Human-readable RH proof accepted by experts** | By Q2 2027; the proof shortens substantially | Partial; attention moves to the next result before interpretation completes | Yes, and it reveals the argument was closer to known methods than it first appeared |
| **Further Millennium-class results in 2027** | One or two, in adjacent areas; extensions of existing routes (Hecke/Dedekind GRH) | Three or more, including at least one problem outside number theory and fluids | None certified; claims arrive but fail verification or stall |
| **Human trace-formula draft** | Repaired in part; delivers a spectral framework but not an independent proof | Overtaken; formalized by volunteers as a historical artifact | Becomes the second proof, restoring a human-readable route |
| **Verification regime** | Formal-proof tracks established at major venues; prize clock starts | Verification capacity becomes the bottleneck; certification lags release by weeks | Prose review reasserts itself for the human draft; formal check remains standard for AI output |
| **Two-cultures dynamic** | Stable coexistence; interpretation becomes a recognized genre | Human-led culture contracts in frontier areas; shifts toward interpretation and verification | Human-led culture regains confidence; AI-integrated culture consolidates in specific registers |
| **Signposts (first half of 2027)** | Author's write-up; proof-golf results; a ledger entry for Hecke L-functions | A second lab claim certified at the RH standard; a non-number-theory Millennium claim | No new certified Millennium-class result by June; errata on the human draft trending to zero |

**Base case: Absorption.** The proof is understood within months, shortens, and extends to the next family of L-functions. One or two further large results arrive in areas adjacent to those already touched. Institutions adapt incrementally: formal tracks, interpretation documents, formalization groups. This is the scenario in which the lessons of 2026 are learned without a second shock.

**Upside case for capability, downside for institutions: Cascade.** Further results arrive faster than they can be interpreted. Verification, not discovery, becomes the constraint; certification queues form. The explanatory deficit grows: several certified theorems, none humanly understood. This scenario is the one for which almost no institution is prepared, and it is the one the eleven-week sequence of autumn 2026 most resembles.

**Downside case for capability: Plateau.** The November proof turns out, on human inspection, to be nearer to known methods than it looked, the human draft is repaired, and no further Millennium-class claim survives verification in 2027. The field re-reads 2026 as a singular event rather than a regime change. This scenario should not be dismissed: a 41-day proof depended on a specific human recognizing a specific structure in a specific prior release, and that alignment may not recur on demand.

**What all three share.** RH stays proved. The explanatory question stays open. Formal verification stays the gate. The two cultures stay. Planning horizons stay short. The scenarios differ in *pace*, not in *direction*.

## Part IV — Implications by stakeholder

### Research institutions and departments

**The exposure.** Frontier results now originate inside AI labs with internal models, and the first public step after a result is certification by an open-source community, not review by a department. A department with no formalization capacity has no role in either step.

**Priorities for 2027.**
- Stand up a formalization and verification capability, even a small one. The skill set (Lean, Mathlib, the four-question checklist, independent kernel replay) is learnable in months and was the only thing that mattered on November 21.
- Recognize interpretation as research. The three reconstructions of the November proof are the first instances of a genre that will grow; promotion criteria that cannot count them will lose the people who write them.
- Decide, explicitly, how to serve the human-led culture. It is productive (the September re-proof; the 940-page draft's genuine ideas) and it is where most current faculty live.

### AI laboratories

**The exposure.** The November release demonstrated that independence of certification is the lab's best defense against the charge of self-interested timing. It also demonstrated that a lab's own statement about what its techniques can do (August: not expected to lead to a proof) can be correct and still miss the horizon by a decade, because the next proof used different techniques.

**Priorities for 2027.**
- Treat independent verification as infrastructure the lab funds but does not control. The value of the November certificate came from the lab's absence from it.
- Publish human-readable accounts alongside formal ones, or fund those who will. A 250,000-page draft withheld as unreadable is a signal that generation outran exposition; the explanatory deficit is now the lab's reputational exposure as much as the field's problem.
- Expect credit disputes as the norm. September's Navier–Stokes episode (two teams, overlapping results, one lab announcing on a press call while the other posted Lean-checked preprints) is the template for every contested result in 2027.

### Journals, learned societies, and prize bodies

**The exposure.** The prize rules for the Millennium Problems require publication in a qualifying outlet, two years of scrutiny, and general acceptance. The only extant proof of RH is a code library. No qualifying outlet has a mechanism for publishing it. The problem's status has moved from "unsolved" to "active" without being "solved," and that limbo is now the prize body's to resolve.

**Priorities for 2027.**
- Define what publication of a formal proof means: what is reviewed (the statement's fidelity, the build, the axioms, the kernels), by whom, and what the published object is.
- Define the standing of interpretation documents relative to the formal proof they interpret.
- Decide whether prize and award criteria that assume a human-readable argument should be amended, and say so before the first case forces the issue in public.

### Funders

**The exposure.** The marginal dollar in mathematics has historically bought discovery. In 2027 the binding constraint in the Cascade scenario is verification and interpretation capacity, and in all scenarios formalization infrastructure (the shared library, the checkers, the tooling) is a public good that no single institution is incentivized to maintain.

**Priorities for 2027.**
- Fund the shared formal library and the independent checkers as research infrastructure, on the model of telescopes and sequencing centers rather than individual grants.
- Fund interpretation explicitly: the work of turning certified code into mathematics humans can teach.
- Preserve funding for the human-led culture in areas where it remains competitive and in areas where the explanatory question (an operator, a trace formula) is the live one.

### Individual mathematicians

**The exposure.** The November author's own account is the clearest guide: he chose the problem, found two ideas in a toy setting, recognized a structure in someone else's release, and steered; the model executed in registers he did not command. The most valuable human contribution was taste, problem selection, and recognition.

**Priorities for 2027.**
- Invest in breadth over depth at the margin. The proof rewarded someone who could *recognize* Stepanov in an automorphic setting, not someone who could compute theta lifts by hand.
- Learn to read formal proofs well enough to interpret them. The reconstruction documents are the new expository frontier and are currently authored by a handful of people.
- Choose problems whose answers plausibly live in an adjacent field. That is where the 2026 results came from and where the 2027 results are most likely to come from.

### Adjacent fields: physics, cryptography, computer science

**Physics.** The proof supplies no Hamiltonian. The Hilbert–Pólya program, the CPT-gauging proposal, and the dynamical-phase-transition experiments are untouched in status: suggestive, numerically striking, unproved as explanation. The spectral program (truncated Weil forms, zeta spectral triples) is now the leading candidate for the explanatory answer, and its open convergence question is, if anything, more important than before.

**Cryptography and computation.** Dirichlet GRH is now unconditional, so results that assumed it (Miller's deterministic primality test; effective bounds for primes in progressions) are theorems. No widely deployed cryptosystem depended on RH being *false*; the practical impact is in effective constants and in the removal of a standing hypothesis from complexity-theoretic results that used it.

**Formal methods.** The November certificate is the largest single validation of the formal-proof ecosystem to date: a 17-million-line library checked by multiple independent kernels in a day. Expect demand for formal-methods talent from mathematics departments, AI labs, and verification startups to exceed supply through 2027.

---

## Part V — Signposts to watch

#### Exhibit 6. Dated signposts and what they decide

| Signpost | Decides | Earliest plausible date |
|---|---|---|
| Human-readable account of the RH proof accepted by analytic number theorists | Whether "alien proof" was seasonal or permanent; which 2027 scenario is in play | Q1 2027 (one leading formalizer expects weeks) |
| Verification ledger entry for Hecke L-functions over CM fields, then Dedekind zeta functions | Whether the certified theorem converges with the colloquial meaning of GRH; whether the route generalizes | Author: "with more time" |
| Proof-golf results on the upstream library | How much of the 17 million lines is essential; indirectly, how much new theory is inside | Rolling from Q1 2027 |
| Revised human trace-formula draft with Chapter 13 written and the Chapter 5 structure theorem repaired | Whether a second, spectral, human-readable proof exists; whether the explanatory deficit closes by a human route | Author's plan: ~1 year |
| A qualifying venue publishes the Lean library | Starts the prize clock; sets the template for formal publication | 2027 |
| Independent certification of the September Navier–Stokes claim at the RH standard, or a prize-body statement on it | Whether 2026 produced one or two Millennium-class theorems | 2027 |
| A proof of convergence for the truncated-Weil-form zeros | A Hilbert–Pólya operator for a theorem now known true; the first "why" | Open-ended |
| Any certified Millennium-class result outside number theory and fluids | Cascade versus Absorption | Monitor monthly |
| Resolution of the named register-crossing bets (prime gaps < 100; sunflower; chromatic number ≥ 6; R(5,5)) | Whether the synthesis mechanism generalizes to combinatorics as forecast | 2027–2028 |

---

## Closing note

The Riemann Hypothesis was, for 167 years, the problem that defined the gap between what mathematicians believed and what they could prove. That gap closed in November 2026, in a form no one can read, by a route almost no one was watching, years ahead of every public forecast including this author's. What remains is a different gap: between what has been certified and what has been understood. The institutions that will matter in 2027 are the ones that treat that second gap as the real work, that build the capacity to verify what they did not discover, and that plan on a horizon measured in quarters rather than decades. The direction is not in doubt. Only the pace is.

---

*Edition note: current to November 24, 2026. Figures and dates are drawn from the primary record (the author's release note, the joint certification statement, the independent verification ledger, the public reconstructions, and the arXiv record of 2026). Scenario likelihoods are indicative judgments. Next edition on the first accepted human-readable account of the proof or on the first ledger entry beyond Dirichlet L-functions, whichever comes first.*
