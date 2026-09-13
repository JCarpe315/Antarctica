# The ANITA Anomaly & Strange Signals in Antarctica
## A Complete Research Compilation — Topic 5 of the Antarctic Deep-Dive Series

*Compiled September 2026, from three dedicated research runs (eleven search rounds plus multiple full-text retrievals of the primary literature).*

---

## HOW TO READ THIS DOCUMENT

This is a research compilation, not a conclusion. It gathers every piece of evidence our investigation could find about one of the strangest unresolved measurements in modern physics: a NASA balloon over Antarctica detected radio signals that appear to be cosmic rays coming **up out of the Earth** — something that, under the known laws of physics, should happen about once in a million tries.

A few ground rules before we begin:

**1. Every claim carries a pedigree tag.** We do not ask you to take anything on faith, including this document's own framing. Each factual claim is tagged with the type of source it comes from:

| Tag | What it means |
|---|---|
| [S] | Peer-reviewed journal publication, or an official record from a government agency, laboratory, or university |
| [A] | Preprint server (arXiv), conference proceedings, or official collaboration material that has not completed peer review |
| [B] | Credible secondary reporting — established science journalists and major newsrooms |
| [C] | Popular media, tabloids, and aggregators. These are cited **only** to document what was publicly claimed or said — never as evidence about nature itself |
| [NA] | Not assessed — a claim resting on a single source, logged for the record but not endorsed |

**2. We do not adopt theories; we inventory them.** Dozens of explanations for the anomaly have been published. Some are mundane, some involve exotic new particles, one made newspaper headlines around the world. This document explains each one fairly, then states what the observational evidence has done to it: confirmed, constrained, disfavored, or excluded. Where the evidence is genuinely unresolved, we say so and leave it unresolved.

**3. Nothing is smoothed over.** Where our sources disagree with each other — and they do, in about a dozen places — both versions are presented side by side with a flag. A research file that hides its own contradictions is not a research file.

**4. The tone.** Imagine a good documentary narrator: precise about the science, patient with the reader, and honest about the difference between what we know, what we suspect, and what we merely hope. Technical terms are defined the moment they appear. Analogies are used where they genuinely illuminate, and abandoned where they would mislead.

One note on dates: all dates are UTC unless stated. "As of this writing" means September 2026 — which matters, because the single most important next step in this story (the analysis of the successor mission PUEO's data) is expected within months of this document's compilation.

---

## PART ONE: THE STAGE — WHY ANTARCTICA, WHY BALLOONS, WHY RADIO

To understand the anomaly, you first have to understand the experiment that produced it — because the anomaly only looks impossible once you appreciate what the experiment was designed to see, and why it was built the way it was.

### 1.1 The quietest laboratory on Earth

Picture the cleanest, stillest place you can imagine. Now make it four kilometers deep and the size of a continent. That is the Antarctic ice sheet.

When a high-energy particle — say, a neutrino traveling for millions of light-years — happens to strike the ice, it triggers a miniature explosion of secondary particles, a cascade called a *shower*. As that shower develops in the dense ice, it emits a faint, brief pulse of radio waves. This is the **Askaryan effect**, predicted by Soviet-Armenian physicist Gurgen Askaryan in 1962 [S]: the shower's electrons and positrons bunch together and radiate coherently, like a choir singing the same note at the same moment instead of individuals humming at random. The result is a detectable radio chirp — impossibly faint, but coherent, which means it can be picked out of the noise.

Antarctica is uniquely suited to hearing these chirps for three reasons. First, the ice is astonishingly pure and cold, so radio signals travel through it with very little absorption. Second, the continent is electrically quiet — there are no cities, no power grids, almost no human radio chatter. Third, the ice sheet is *thick* and *vast*, giving the rare incoming particle an enormous target.

There is a second signal Antarctica is good for. When an ultra-high-energy **cosmic ray** — a single atomic nucleus, hurled across the galaxy or beyond at nearly the speed of light — slams into the top of the atmosphere, it doesn't penetrate to the ice. Instead it detonates high above the ground, spraying billions of secondary particles downward in a cascade called an **extensive air shower** (EAS). This cascade, too, emits radio — generated when its electrons and positrons are bent by Earth's magnetic field. Physicists call this **geomagnetic emission**, and it has a distinctive fingerprint: it is polarized **horizontally**, meaning the electric field of the radio wave wiggles side-to-side in a predictable plane tied to the direction of Earth's magnetic field. Hold on to that detail. It becomes the single most important clue in this entire file.

### 1.2 The ghost particle and the tennis ball

Two kinds of messenger arrive from the cosmos carrying news about the universe's most violent places: cosmic rays and neutrinos.

A **neutrino** is the closest thing in nature to nothing. It is a fundamental particle with (almost) no mass and no electric charge, and it interacts with matter so rarely that trillions of them are streaming through your body as you read this sentence, and essentially all of them will pass through the entire planet without touching anything. That ghostliness is exactly why physicists love them: light can be absorbed and bent; cosmic rays can be deflected by magnetic fields; but a neutrino points straight back at whatever monster produced it, because nothing has touched it since.

An **ultra-high-energy neutrino** — the kind this story concerns — carries at least one **EeV** (an exa-electron-volt, 10^18 electron-volts). Numbers that large stop meaning anything, so here is the standard comparison physicists use, and it is literally true: a single EeV neutrino carries about as much kinetic energy as a tennis ball served at professional speed — compressed into one subatomic particle. The Large Hadron Collider, the most powerful machine humans have ever built, accelerates particles to about one ten-thousandth of that energy per particle.

Particles with this kind of energy are extremely rare. Detecting them requires enormous targets and patient listening — which brings us to the instrument.

### 1.3 ANITA: a radio ear hanging over the pole

The **Antarctic Impulsive Transient Antenna** (ANITA) was, in concept, disarmingly simple: a payload of radio antennas, hung from a high-altitude balloon, listening down at the ice and the atmosphere as the circumpolar winds carried it around the continent at the edge of space [S/A].

In institutional terms, ANITA was the first observatory NASA ever operated whose purpose was to detect neutrinos of any kind [S/B]. The Principal Investigator was physicist **Peter Gorham** of the University of Hawaiʻi at Mānoa; the program was funded by NASA and the U.S. Department of Energy, with partner institutions including the University of Chicago, Washington University in St. Louis, Penn State, Ohio State, University College London, the U.S. Naval Research Laboratory, and the Jet Propulsion Laboratory [S/B].

The payload, in more detail [A: EPJ ARENA 2017 proceedings; S: collaboration papers]:

- **Antennas:** 32 to 48 dual-polarization horn antennas depending on the flight, each able to sense both horizontal and vertical polarization — the instrument's two "ears," one tuned to each of the two signals described above.
- **Frequency range:** roughly 200 to 1300 megahertz, a slice of the radio spectrum chosen because Askaryan and geomagnetic pulses are strong there and human interference is minimal.
- **Digitizers:** custom LAB4 chips sampling at 2.6 billion times per second, capturing the exact shape of each pulse — its amplitude, its polarization, and crucially its *phase*, which we will explain when it matters.
- **Trigger:** a fast first-level circuit (tunnel-diode detectors) watching for anything above the noise, backed by programmable logic (FPGAs) that decided within microseconds whether an event was worth recording.
- **Altitude:** about 37 to 40 kilometers — high enough to see the horizon curve away roughly 400 kilometers in every direction, and to look *down* at the top of the atmosphere from above.
- **Launch site:** NASA's Long Duration Balloon facility at Williams Field, on the Ross Ice Shelf near McMurdo Station; the polar vortex winds carry the balloon on a roughly circular path around the continent for weeks at a time [B: stratocat flight logs].

Before we go further, one more piece of physics, because everything hinges on it. When a radio pulse reflects off a surface, its phase inverts — think of a ball bouncing off a hard floor: the bounce flips its motion relative to the incoming path. A pulse that reflects off the ice arrives with **inverted polarity** compared with a pulse that traveled directly. And a pulse that comes from *below* — from a shower traveling upward through the Earth and out the atmosphere — arrives with the *original, non-inverted* polarity, like a ball that was thrown up from under the floor and never bounced. ANITA's ability to read polarity meant it could, in principle, tell a reflected down-going cosmic ray from a genuine up-going event. In principle.

### 1.4 The calibration program: HiCal

Here is a question the whole mission depended on: when a radio pulse grazes the Antarctic ice at a very shallow angle, how much of it reflects, and how? Common sense says glancing reflections off snow should be messy. The ANITA team decided to measure it rather than assume it, and built **HiCal** — a small bistatic radar transmitter that flew with the payload and fired calibration pulses down at the ice so the main instrument could watch the reflections [S: arXiv:1703.00415; PRD 98, 042004].

- **HiCal-1** (January 2015, ANITA-III's season) produced the first surprise: the ice's reflectivity at very glancing angles *exceeded* the textbook Fresnel predictions. The ice reflected radio better than expected.
- **HiCal-2** (December 2016, ANITA-IV's season) fired of order 10,000 pulses across distances of 100 to 700 kilometers and found broad agreement with models that account for the Earth's curvature and the ice's surface roughness [S].

Remember HiCal. It exists because the interpretation of the anomaly depends entirely on knowing how radio behaves at grazing angles over this ice — and HiCal's data will later be called as a witness by *both sides* of the central argument.

Also on the record: the Askaryan effect itself was first demonstrated experimentally by the team that would become the ANITA collaboration, at the Stanford Linear Accelerator in 2000 (Saltzberg et al.), and re-verified in a ten-ton block of ice at SLAC in 2006 [S/B]. The effect the instrument was built to detect was real and well understood. The anomaly was not in the calibration; it was in the sky. Or rather, in the ground.

### 1.5 Four flights, four seasons

**Flight record [B: stratocat flight logs; A/S: collaboration papers]:**

| Flight | Launch | Duration | Notes |
|---|---|---|---|
| ANITA-I | December 14, 2006 | ~35 days | 32 antennas; ~8.2 million radio triggers recorded; 16 ultra-high-energy cosmic-ray events seen in initial summaries |
| ANITA-II | December 2008 | ~29 days | 40 antennas; deliberately flown with a vertically-polarized-only trigger — blind to air showers, tuned instead for neutrino cascades in ice; 2 cosmic-ray events |
| ANITA-III | December 17, 2014 | 22 d 9 h | 48 antennas; 28 cosmic-ray events |
| ANITA-IV | December 2, 2016 | 27 d 17 h | Added tunable notch filters ("TUFFs") at 260 MHz and 360–450 MHz to suppress satellite interference; 29 cosmic-ray-like events |

*Logged discrepancy:* one conference presentation lists ANITA-IV's flight window as December 6–29, 2016, while flight records give a December 2 launch with a 27-day, 17-hour duration [A vs. B]. The event data is unaffected; the discrepancy lives in secondary reporting of the launch window, and we note it because this document's rule is that contradictions stay visible.

### 1.6 How ANITA sorts its events

Cosmic-ray-like events fall into three classes, in the collaboration's terminology [A: Salvado review material]:

- **Type 1 — direct:** an ordinary cosmic ray arrives from above the horizon; its air shower's radio pulse is received directly, with normal polarity. Fully expected.
- **Type 2 — reflected:** an ordinary cosmic ray arrives from above; its pulse bounces off the ice before reaching the antenna. The bounce inverts the polarity. Also fully expected — in fact, most of ANITA's events are Type 2, because looking down at the ice, a reflected pulse is often louder than a direct one.
- **Type 3 — anomalous:** the event appears to arrive from *below the horizon*, with non-inverted polarity — the fingerprint of a shower that traveled **upward**, out of the Earth, without ever bouncing. Under known physics, essentially only one thing can make that: a neutrino that converted into a heavier cousin particle inside the planet and decayed on the far side. More on that mechanism shortly.

The per-flight census, from the collaboration's own review presentations [A: Salvado, MPI 2022; review arXiv:2309.17139]:

| Flight | Type 1 (direct) | Type 2 (reflected) | Type 3 (anomalous) |
|---|---|---|---|
| ANITA-I | 2 | 14 | 1 (event 3985267) |
| ANITA-II | — | 2 cosmic-ray events (air-shower classes not applicable to its trigger) | — |
| ANITA-III | 3 | 17 | 1 (event 15717147) |
| ANITA-IV | 2 | 23 | 4 (the near-horizon set) |

*Logged counting discrepancy:* the per-flight Type 2 figures above sum to 54, while the program's summary paper quotes 64 reflected events across all four flights, and ANITA-I's total appears as both 16 and 17 in different summaries [S: PRD 105 vs. A: review slides]. No single published table reconciles these counts; the differences are consistent with different event-quality cuts, but we flag rather than resolve them.

Total haul across four flights: 6 anomalous Type 3 events, plus a separate class of 7 "atmosphere-skimming" events we will meet later. Six anomalous events is the canonical count used by the collaboration's own members [A: Wissel, public talks and CV].

---

## PART TWO: THE PEOPLE

Before the physics resumes, the cast — because in this story, *who* measured something, *who* cross-checked it, and *who* is building the sequel matters as much as the numbers.

- **Peter Gorham** — Principal Investigator of ANITA, University of Hawaiʻi at Mānoa. Led the experiment from its SLAC calibration origins through four Antarctic flights [S/B].
- **Stephanie Wissel** — Penn State; ANITA collaborator, now co-investigator of the successor mission PUEO *and* a Principal Investigator of the next-generation ground array HERON. In June 2025 she gave the most-quoted public assessment of the anomaly (quoted in full in Part Six): the signals are "most likely not representing neutrinos" [B/A].
- **Abigail Vieregg** — University of Chicago; Principal Investigator of PUEO, the successor balloon mission [A].
- **Brian Rauch** — Washington University in St. Louis; ANITA veteran, PUEO co-investigator; his university published the most detailed post-flight recovery reporting in August 2026 [B].
- **Ibrahim Safa** — ANITA collaborator who became, in April 2020, the team's clearest public voice pushing back on "parallel universe" headlines [B/C].
- **Kumiko Kotera** and **Jaime Álvarez-Muñiz** — leading theorists of the radio-detection technique; co-Principal Investigators of HERON; authors or co-authors of many of the explanation papers cataloged in Part Five [S/A].
- **Javier Salvado** — whose 2022–2024 review talks and review article (arXiv:2309.17139) supply much of the program-level accounting used in this document [A].
- **Stephanie Wissel's team at Penn State, the UH Mānoa group, the UChicago group** — and across the Atlantic, **Massimo Villata** of INAF Turin, author of the most radical cosmological explanation on record (Part Five, §5.4), a single-author theorist with a two-decade program behind him.
- **The rival observatories** — IceCube (South Pole), the Pierre Auger Observatory (Argentina), KM3NeT (Mediterranean Sea), HAWC (Mexico), EUSO-SPB2 (a NASA balloon): the judges. Every one of them looked for confirmation of ANITA's events and reported what they found, including the nothing.

Why this matters: one of the through-lines of this dossier is that the anomaly has been investigated hardest by the people who discovered it. The firn-reflection hypothesis was developed by ANITA-adjacent physicists; the phase-inversion limits were computed by ANITA-adjacent physicists; the axion proposal came from inside the analysis team. Whatever one thinks of the mystery, no one can fairly call the collaboration credulous — they have spent fifteen years trying to kill their own anomaly, and published every swing.

---

## PART THREE: THE SIX EVENTS

This is the core evidence. Everything else in this document — every cross-check, every theory, every successor experiment — exists because of the six events described here.

### 3.1 Event one: December 28, 2006

**Pedigree: [S] PRL 117, 071101 (2016); [A] collaboration review material**

At 00:33:20 UTC on December 28, 2006 — four days before the end of ANITA-I's first flight — the payload recorded a radio pulse of a kind no one had expected.

The full reconstructed data [S/A]:

- **Event ID:** 3985267
- **Elevation:** −27.4° ± 0.3° — that is, 27 degrees *below* the geometric horizon. The ray traced back through the air and into the ice sheet, pointing down into the planet.
- **Energy:** the parent shower carried an estimated 0.6 ± 0.4 EeV — of order a hundred million times more energetic per particle than anything at CERN.
- **Location over the ice:** 82.66° S, 17.28° E, deep on the plateau.
- **Payload altitude at the trigger:** 2.56 kilometers above the ice reference surface; the ice below was 3.53 kilometers thick.
- **Arrival azimuth:** 159.62° ± 0.7°.
- **Sky coordinates (equatorial):** right ascension 282.14°, declination +20.33° — a direction in the northern celestial hemisphere, meaning the ray had passed through the entire planet to get there.
- **Polarization:** horizontal, and geomagnetically correlated — the unmistakable fingerprint of an extensive air shower, not of an Askaryan cascade in ice.
- **A posteriori background probability:** the chance that a mundane background fluctuation would fake this event, evaluated *after* seeing it, is quoted in the literature between roughly 4×10⁻⁴ [A: review material] and ≲10⁻⁵ [S: paper-era estimates]. *Logged discrepancy:* the spread reflects different analysis assumptions; no single canonical figure is quoted consistently across sources.

In plain terms: the pulse looked exactly like an air shower — except air showers fall *down* from the sky, and this one appeared to be rising *out of the ground*.

### 3.2 Event two: December 20, 2014

**Pedigree: [S] PRL 121, 161102 (2018)**

Eight years later, on ANITA-III's second flight, lightning struck twice.

- **Event ID:** 15717147
- **Date/time:** December 20, 2014, 08:33:22.5 UTC
- **Elevation:** −35.0° ± 0.3° — even steeper below the horizon than the first event
- **Energy:** 0.56 EeV (with stated asymmetric uncertainties of roughly +0.3/−0.3 EeV)
- **Location:** 81.40° S, 129.02° E
- **Payload altitude:** 2.75 km; ice below: 3.22 km thick
- **Arrival azimuth:** 61.41° ± 0.7°
- **Sky coordinates:** RA 50.78°, Dec +38.65°
- **Polarization:** horizontal, geomagnetically correlated — an air-shower fingerprint again
- **A posteriori background probability:** ≲10⁻³ [S: PRL 121, 161102]

*Logged discrepancy:* the PUEO white paper later quotes this event's elevation as −36.7° rather than −35.0° [A: arXiv:2010.02892 vs. S: PRL 121]. Both numbers come from the same collaboration; they represent different reconstruction iterations, and the published paper's value is the one to cite.

A single weird event can be a fluke. Two, from two different flights eight years apart, with the same impossible signature, in the same energy range, constitute a *class* of events. That is when the physics community sat up straight.

### 3.3 Why these events are impossible — in the plainest possible terms

Here is the entire mystery in one paragraph of physics.

An upward-going air shower below the horizon can be made, under the known laws of physics, by exactly one mechanism: a **tau neutrino** — the heaviest and rarest of the three neutrino types — arrives nearly parallel to the surface, skims through thousands of kilometers of rock, and in its very rare interactions converts into a **tau lepton**, a heavier unstable cousin of the electron. If that conversion happens at just the right depth, the tau survives the remaining rock, exits into the atmosphere, and decays — spraying an upward-going particle cascade that ANITA can see. Physicists call this the **Earth-skimming** channel, and it is a real, accepted part of the Standard Model. Every up-going air shower ever credibly claimed before ANITA went through this door.

The problem is arithmetic. For the ANITA-I event, the geometry of the observation requires the neutrino to have traveled a chord of about **5,785 kilometers** through rock and mantle. For the ANITA-III event, about **7,309 kilometers** [A: arXiv:1804.05362, citing the event geometry]. At EeV energies, matter is — astonishingly — almost opaque to neutrinos: the distances above correspond to roughly **8 to 10 interaction lengths**. An interaction length is the average distance a particle travels before reacting; after 8 to 10 of them, the survival probability is **less than about one in a million** (≲10⁻⁶) [A/S].

So there are only two doors out of the room:

1. **The flux door.** Perhaps the sky is raining tau neutrinos at such a colossal rate that even one-in-a-million survivors show up regularly. But that rate would be so enormous that every other neutrino observatory on Earth would drown in the same particles. They did not (Part Four). The door is barred.
2. **The fake door.** Perhaps the events were never up-going neutrino showers at all. Something — in the ice, in the atmosphere, in the instrument, or in the physics — imitated the signature. Then the question is no longer "where do these neutrinos come from?" but "what is the impersonator, and why does it impersonate so well?"

Every theory in this document walks through one of those two doors. Keep both in mind.

### 3.4 The supernova that almost explained everything (but didn't)

**Pedigree: [S] PRL 121, 161102 (2018)**

The 2018 paper reported a coincidence that briefly electrified the collaboration: the ANITA-III event had arrived from within **1.19°** of the sky position of supernova **SN 2014dz** — a Type Ia supernova at redshift z = 0.017 — and within about five hours of the supernova's discovery announcement. The a posteriori chance of such a pairing was computed at 3.4×10⁻³, about a 2.7σ curiosity [S].

Why it couldn't be the answer: for the supernova to be the source, its peak neutrino luminosity would have to exceed the supernova's *entire* electromagnetic output — about 4.4×10⁴² erg per second — unless the emission were somehow beamed like a lighthouse [S]. Nature does not lightly break its own luminosity budgets. The paper also noted a blazar, J0322+3948, near the arrival direction; not statistically significant.

And the final nail came later, quietly: a **blind catalog-association search** performed in a University of Hawaiʻi PhD dissertation (Prechelt, 2022) looked for any statistically significant association between the anomalous events' directions and known astronomical catalogs, without preconceptions. It found none [A]. The supernova connection is preserved in this file as what it was: a legitimate, published coincidence that physics declined to endorse.

### 3.5 The four near-horizon events: ANITA-IV's strange sequel

**Pedigree: [S] PRL 126, 071103 (2021); PRD 105, 042001 (2022, Prechelt et al.); [A] review material**

ANITA-IV flew in December 2016 with a new generation of hardware — including the notch filters that excised satellite interference — and it delivered a twist: **no steeply up-coming events at all**, like its two predecessors. Instead, four events that looked like up-going showers but hugged the horizon, each arriving within about a degree of the radio horizon with angular resolution around 0.2° [S].

The four events and their individual characteristics [S: PRD 105]:

| Event ID | Distinctive feature |
|---|---|
| 4098827 | Detected with all three notch-filter settings — which rules out an instrumental artifact tied to the new filters |
| 72164985 | The best match of the four to an up-going tau air shower in Monte Carlo reconstruction |
| 19848917 | Arrived with **suppressed power at low radio frequencies (below ~500 MHz)** — an anomaly within the anomaly; see below |
| 50549772 | Also shows the low-frequency suppression |

As a cross-check on the polarimetry pipeline, the team verified that an ordinary reflected down-going cosmic ray recorded during the same flight (event 36785931) showed the inverted polarity it was supposed to show — the instrument's polarity-reading was working [S].

**The full analysis findings, one by one [S: PRD 105]:**

- **Significance.** The four events together represent a background fluctuation at the **3.2σ** level (p = 5.3×10⁻⁴). The analysis estimates the most probable number of genuinely-anomalous events among the four as **three**.
- **Energies.** Monte Carlo reconstruction (using the tapioca shower code and the emcee statistical sampler): assuming the events came from an E⁻²-spectrum source, the parent neutrino energies run from roughly 1 to 50 EeV, with the best-matching event (72164985) pointing to a central value around 15 EeV.
- **Shape agreement.** Kolmogorov–Smirnov tests — a standard statistical test for "does this data look like this model?" — find the four events' measured properties statistically consistent with up-going tau air-shower simulations, with p-values of order 0.5, *including* their elevation angles. Whatever made them looked, in shape, like the real thing.
- **Yet the flux is impossible.** A *diffuse* tau-neutrino flux at the implied rate is ruled out — it is in direct tension with ANITA-IV's own exposure and livetime. The events cannot be common; there are too few of them for that. So the analysis turns to a *point source* — one special direction producing rare bursts — and finds that interpretation squeezed too: the implied fluence conflicts with the Pierre Auger Observatory's limits across energies, **and** with ANITA-IV's own vertically-polarized Askaryan channel at the highest energies (above ~10^18.8 eV). And as a matter of geometry, none of the four arrival directions happened to be visible to Auger at the relevant times.
- **Direction-quality caveat.** At review level [A: Salvado, arXiv:2309.17139]: two of the four events carry only 1–2σ direction significance, meaning their reconstructed arrival directions are individually shaky — each could, in isolation, be an above-horizon event misreconstructed downward. Coherence and propagation constraints make that unlikely for the set as a whole, but the per-event quality is uneven, and honesty requires saying so.
- **The low-frequency anomaly.** Events 19848917 and 50549772 arrived with diminished power below about 500 MHz. The paper's tentative attribution: atmospheric propagation effects over very long, near-horizon path lengths — and it explicitly flags this as a technical challenge **not modeled** in the analysis [S: PRD 105, §V.1]. This is not a footnote; "something odd happens to radio near the horizon" is exactly where one of the leading mundane explanations lives (Part Five), and here the anomaly's own data carries a fingerprint of it.
- **Program-level significance.** The same review material places the anomalous-event significance across the whole four-flight program at **3.3 ± 0.5σ** [A].

*Logged gap:* the PRD paper states that the true reconstructed sky coordinates of the four events "will be published in a follow-up paper by the ANITA collaboration." That follow-up was searched for three separate times over the course of this research, in every major index. **It has never appeared.** The promise is on the record; the paper is not. This matters because without public coordinates, independent groups cannot run their own sky-association analyses — the kind of analysis that might have settled the transient-source question.

### 3.6 A separate species: the seven atmosphere-skimming events

Distinct from the six anomalous events — and distinct from ordinary cosmic rays — ANITA's four flights together recorded **seven "atmosphere-skimming" (AS) events**: showers from cosmic rays entering the atmosphere at such shallow angles that they fly 20 to 30 kilometers *sideways* through the upper atmosphere, still above the horizon, before hitting the ground [A: arXiv:2404.01239; Salvado review]. The 2016 paper had already described three such events from ANITA-I alongside the first anomaly [S: PRL 117].

Why they belong in this file: they are a newly recognized event class that ANITA effectively discovered, and they matter to the anomaly in two ways. First, they demonstrate that the instrument can recognize and classify exotic geometries — the AS events are not mysterious. Second, the physics that lets a shallow-angle shower skim the atmosphere (refraction and propagation near Earth's limb) is the *same family of physics* invoked to explain the anomalous events. EUSO-SPB2's Cherenkov telescope has since observed AS-shower candidates in optical light; the radio emission of AS showers has been modeled (Tueros et al., JCAP 01(2025)112); and a Snowmass planning document notes that the growing AS dataset "will help quantify refraction near Earth limb" — words that should be kept next to the ANITA mystery [S/A]. The AS events are logged as context: a discovered species, not a mystery.

### 3.7 The one vertical event

One more entry in the ledger: ANITA-III recorded a single **vertically polarized (V-POL) candidate** — the signature of an Askaryan cascade *inside the ice*, i.e., a genuine neutrino interaction candidate. Its background estimate was 0.7 (+0.5/−0.3) events per polarization, and the flight recorded no human radio activity within 260 kilometers of the arrival direction [A: Cremonesi seminar material]. It is consistent with background and was never claimed as a detection — but it is preserved here because it is the lone vertically-polarized event in the program with no obvious human culprit, while all of the program's *mysteries* arrived horizontally polarized. The pattern may mean nothing. It is in the record.

---

## PART FOUR: THE JUDGES — WHAT EVERY OTHER OBSERVATORY SAW

A measurement is only as strong as the failure of other experiments to confirm it. Here is the crucial structural fact of the ANITA anomaly: the same geometry that makes the events impossible under known physics also makes them *checkable*. If EeV tau neutrinos really are streaming up through the Earth along those directions at those rates, they cannot avoid leaving traces in other detectors. Three of the world's great observatories went looking. What each found — and did not find — is the subject of this part.

### 4.1 IceCube and the regeneration argument (January 2020)

**Pedigree: [S] M. Aartsen et al., ApJ 892 (2020), arXiv:2001.01737; [B] contemporaneous coverage with collaboration-member statements**

**The observatory.** IceCube is a cubic kilometer of Antarctic ice — a thousand meters on a side — instrumented with over five thousand light sensors, buried at the South Pole itself. It is the world's flagship neutrino telescope, and it detects neutrinos of energies a thousand to a million times *lower* than ANITA's events. That energy gap is not a weakness; it is the key to the cross-check.

**The logic — why a null result here is devastating.** Think of the Earth-skimming neutrino as a runner trying to cross a minefield thousands of kilometers long. The ANITA events require the runner to get almost all the way across before detonating — an event with probability under one in a million. But a runner who *almost* makes it is not silent on the way: every near-miss interaction sprays lower-energy secondary neutrinos — daughters of the tau's repeated decays and regenerations — in a cone around the original direction. Those secondaries are exactly the energies IceCube eats for breakfast: TeV to PeV, arriving from the same patch of sky. So even if the parent neutrino misses every detector, its family should rain down on IceCube from the anomalous arrival directions. Physicists call this **tau regeneration**, and it converts "one observatory saw something weird" into "two observatories must agree, or the story is wrong."

**The search.** IceCube took 7–8 years of data and ran three separate analysis strategies — including ones generous to the anomaly, testing time windows of different lengths around the event epochs [S].

**The result: nothing.** Zero correlated events. The paper's conclusion, quoted in its own restrained language: an astrophysical explanation of the anomalous events under Standard-Model assumptions "is severely constrained regardless of source spectrum" [S].

**What the scientists said.** In the coverage accompanying the paper [B], three IceCube members stated the conclusion for a general audience — Alex Pizzuto, Raquel Barbano, and Ibrahim Safa: the events were inconsistent with any known astrophysical source; the simplest explanations were excluded; and the remaining possibilities were unpalatable — either the events were not neutrinos at all, or the physics was not the Standard Model. Safa would become the collaboration's most quotable spokesperson three months later, for a different reason (Part Six).

**Why this matters:** the regeneration argument does not depend on any assumption about what makes the events. It only requires that *if* they are EeV tau neutrinos, the minefield of Earth must have sprayed detectable shrapnel at IceCube. It didn't. The flux door — Door Number One from §3.3 — is not merely closed; it is welded shut for any steady, sky-distributed population.

### 4.2 The Pierre Auger Observatory and the up-going shower search (March 2025)

**Pedigree: [S] Pierre Auger Collaboration, PRL 134, 121003 (2025); [A] Auger collaboration presentation, ICNFP 2025**

**The observatory.** Auger is the largest cosmic-ray detector ever built: an array of particle detectors covering 3,000 square kilometers of Argentine pampas, overlooked by fluorescence telescopes that watch the sky for the faint ultraviolet glow of air showers. If up-going air showers at EeV energies exist at any meaningful rate, Auger's eyes must eventually see them.

**The search.** The collaboration combed 2004–2018 data for **up-going air showers** — events arriving from zenith angles greater than 110°, i.e., from below the horizon, in the reconstructed energy range 0.1 to 33 EeV. This is precisely the class ANITA's polarimetry claimed [S].

**The result: one event, against 0.27 ± 0.12 expected from background.** And the decisive arithmetic: normalize the up-going flux to ANITA's events, and Auger should have seen **more than 34 events** if the spectrum falls as E⁻², or **more than 8.1 events** for a steeper E⁻⁵ spectrum. One is not eight. One is not thirty-four. The interpretation that the ANITA events were genuine up-going showers is, in the collaboration's assessment, excluded [S].

**The blind spot — an important nuance, kept in the record.** As the ANITA-IV analysis itself noted [S: PRD 105], Auger's separate fluorescence **Earth-skimming tau** channel had historically only considered events with tau exit elevation angles greater than 20°. The ANITA-IV *near-horizon* events — arriving within a degree of the horizon — fall outside that channel's reach. So the cross-check ledger reads with precision:
- The two *steep* events (elevations −27.4° and −35.0°): directly constrained by Auger's up-going-shower search and IceCube's regeneration argument. Heavily constrained.
- The four *near-horizon* events: not directly covered by that Auger channel; constrained instead by flux-tension arguments — they demand a source so rare that nothing else saw it either, which is a weaker but still uncomfortable argument.

*Logged cross-collaboration discrepancies:* (a) Auger's conference material quotes the ANITA event energies as "E₁,₂ ≈ 0.2 EeV" [A] — versus ANITA's own published 0.6 and 0.56 EeV [S]. Two collaborations, two reconstruction conventions for showers no one fully understands; flagged, not resolved. (b) The same Auger material quotes tau exit angles of roughly 30° — a geometry detail that matters precisely because of the blind-spot boundary described above.

### 4.3 The long-lived particle rescue attempt — and its exclusion

**Pedigree: [A/S] M. Bertólez-Martínez et al., JHEP 07(2023)005, arXiv:2305.03746; Auger collaboration follow-up presented at NEUTRINO 2024**

One serious strategy for saving an up-going interpretation was to change the particle, not the flux. Bertólez-Martínez and collaborators proposed a beyond-Standard-Model, tau-*like* **long-lived particle** produced inside the Earth — a heavy exotic state that interacts, exits, and decays upward like a tau but with different probabilities. Fitting the ANITA-IV data produced a specific benchmark: interaction cross section σ = 8.9×10⁻³³ cm², lifetime T = 1.3×10⁻³ seconds, flux Φ = 1.8 events per square kilometer per day [A].

Then Auger did to this hypothesis what it does: it searched its own data (both the fluorescence up-going channel and the surface-detector Earth-skimming channel) for the same signature and **excluded that parameter region** [A].

Why log this specifically? Because it establishes a pattern that runs through this entire dossier: each new rescue hypothesis that makes *specific, testable* predictions is being met with a specific, published null result. The anomaly is not being ignored; it is being hunted, hypothesis by hypothesis.

### 4.4 The reckoning: "Four, One, and None" (July 2026)

**Pedigree: [A/S] D. Chattopadhyay, C. Argüelles et al., arXiv:2607.19487 (July 21, 2026); supported by DOE grant DE-SC0016013**

The most complete statistical statement of the problem to date — and the freshest peer-facing entry in this file, submitted eight weeks before compilation.

The title says it all: **four** near-horizon events (ANITA-IV), **one** ultra-high-energy track (KM3NeT's KM3-230213A — Part Seven), and **none** at IceCube.

The authors built semi-analytic, energy- and direction-dependent "effective areas" — maps of how sensitive each detector is, as a function of where in the sky and at what energy a particle arrives — for all three observatories, and folded in the time-dependent exposures of ANITA-IV and KM3NeT. Then they asked the joint dataset one question: *can any single population of sources, under Standard-Model physics, produce exactly this pattern?*

The two scenarios tested:

- **Diffuse flux** — a steady, all-sky drizzle of ultra-high-energy neutrinos: **no fit exists.** The best possible configuration sits at **~7.5σ tension** — and even it predicts about five IceCube events that were never seen, while *underpredicting* the ANITA and KM3NeT counts. That is as close as statistics gets to saying "impossible."
- **Rare transients** — rare, brief flares aimed exactly along the observed directions during the detection windows: the tension drops, but only by embracing a "highly fine-tuned" geometry. And if such flares exist but are aimed randomly across the sky over IceCube's ~15-year lifetime, other flares must have fired in IceCube's view. The authors ran 100,000 Monte Carlo realizations of plausible transient populations and found the best of them still at **5.9σ tension**.

**Conclusion, quoted in substance:** within the Standard Model, neither directional nor temporal structure can reconcile the ANITA-IV and KM3NeT observations with IceCube's null result [A/S].

What this paper does *not* say is as important as what it says: it does not identify the cause. It does not endorse new physics. It quantifies, with modern statistical machinery, exactly how stuck the Standard-Model explanations are. When the eventual history of this anomaly is written, "Four, One, and None" will likely be the citation for the sentence "by mid-2026, the conventional explanations were measured to be excluded at between six and seven and a half sigma."

---

## PART FIVE: THE EXPLANATION LANDSCAPE

Roughly thirty papers proposing explanations have been cataloged in the course of this research. Each is presented here on the record: what it proposes, in plain language; who proposed it; and what the evidence has done to it. The status labels are ours, derived from the published cross-checks described in Part Four — the papers themselves, naturally, argue for themselves.

The landscape sorts into four families: **mundane** (the anomaly is a mirage — ice, air, or instrument effects), **Standard-Model-adjacent** (real particles, but the wrong ones, or with the wrong properties), **beyond-Standard-Model** (new particles or interactions), and **speculative cosmology** (new universes). We take them in order of how much of physics each one is willing to break.

### 5.1 Family One: mundane explanations

#### (a) The firn hypothesis — reflections from under the surface

**Proposed by:** Ian Shoemaker and colleagues, Annals of Glaciology (2020), arXiv:1905.02846 [S/A]. Notably, this idea comes from *within* the particle-physics community, not from outside critics.

**The idea, in plain language.** ANITA's logic assumed a simple world: any cosmic-ray pulse that bounces off Antarctica inverts its phase, so a non-inverted below-horizon pulse must have come up through the Earth. Shoemaker pointed out that the real Antarctic surface is not simple. Between loose surface snow and solid ice lies the **firn** — a tens-of-meters-thick layer of compressed snow, still porous, where density increases with depth in a gradient that is usually smooth but *not always*. Radar surveys had found places where the density profile bends backward, creating buried reflecting boundaries. A pulse from a down-going cosmic ray could travel past the surface, reflect off a buried density discontinuity, and climb back to the balloon — without the surface-bounce phase inversion. To the antenna, it would look exactly like an up-going shower. The mirage analogy is nearly literal: like a patch of hot road ahead appearing to reflect the sky, a buried layer can present a false image of where the light came from.

**The quantitative demands.** Pretty is not enough; the hypothesis must also produce the *rate*. The paper's analysis (its Figure 1 quantifies the requirement) showed that explaining ANITA's events needs suitable reflectors over on the order of **7% or more** of the surveyed ice at the right geometry, and tilted so as not to produce a tell-tale double pulse (a real subsurface reflection should often arrive in pairs, which ANITA does not see) [S/A]. The paper surveyed candidate structures: double layers of ice over hoar frost found to be "extensive" in West Antarctica at 400 MHz radar frequencies; wind-glaze and sastrugi (wind-sculpted surface features) covering up to ~11% of the East Antarctic ice sheet; ice-fabric layers. It evaluated subglacial lakes and found them unpromising — less than 1% areal coverage.

**The proposed test, and its absence.** The paper specified exactly how to settle the matter: radar surveys of the ground beneath the two steep-event sites, looking for the required reflectors. As of September 2026 — more than six years later — **no such survey has appeared in any published form**. Whether one was ever performed is not on the public record. *This is one of the most consequential open threads in the entire dossier: the anomaly's leading mundane explanation has a defined, affordable, ground-truth experiment, and the ground truth is missing.*

**The counter-attack from calibration.** The ANITA team responded with its own published analysis (Gorham et al., JCAP 04(2021)016, arXiv:2009.13010) [S]: HiCal-2's recorded reflection waveforms do **not** match subsurface-reflector models; an embedded tilted layer is allowed only at the 2–3% coverage level (below the ~7% the hypothesis needs); the thin-layer model at 7% coverage is clearly disfavored; and — most sharply — at the near-horizon geometries of the ANITA-IV events, more than 95% of the incident radio amplitude reflects at the *surface itself*, leaving too little to penetrate, reflect subsurface, and return coherently.

**Status:** the firn hypothesis is *not dead in principle* — buried reflectors exist, and no one has surveyed the actual event sites — but it is under siege from the mission's own calibration data, and its decisive experiment has gone undone. Two honest papers currently point in opposite directions, and the tiebreaker fieldwork has not been published.

#### (b) Transition radiation — the boundary pulse

**Proposed by:** Motloch, Álvarez-Muñiz and colleagues, PRD 95, 043004 (2017); extended by de Vries & Prohira (2019) [S/A].

**The idea.** When an ultra-relativistic charged particle crosses the boundary between two media — air into firn, say — it emits a small electromagnetic flash called **transition radiation**. Could such flashes, produced by particles in cosmic-ray showers crossing the air-ice boundary, mimic or distort ANITA's near-horizon events?

**Status: disfavored, on ANITA's own data.** One event was already in roughly 2.5σ tension with the transition-radiation prediction; and decisively, ANITA recorded *many* steep, ordinary, reflected cosmic-ray events that transition radiation should also have modified. The effect simply does not appear in the data where it must [A: Salvado review]. As with the firn hypothesis, this kill-shot came from the ANITA community itself.

#### (c) "It was an ordinary reflected cosmic ray, and the phase reading was wrong"

**The idea.** The simplest possibility of all: Type 3 events are misclassified Type 2s — ordinary down-going cosmic rays whose reflections failed to invert, or whose polarity was misread.

**Status: excluded at roughly 4.5σ** by the collaboration's own polarimetry and angular analyses (Esteban, López-Pavón, Martínez-Soler, Salvado, EPJC 80, 259 (2020), and related work) [S/A]. This matters for fairness: the *first* escape hatch any skeptic reaches for — "the polarity measurement must be off" — is precisely the escape hatch the discoverers tested first and closed themselves.

#### (d) The Brewster-angle axion — the in-house exotic-mundane hybrid

**Proposed by:** R. Esteban, J. López-Pavón, M. Martínez-Soler, J. Salvado, EPJC 80, 259 (2020) [S]. Again: from inside the analysis world.

**The idea, in two steps.** First, a burst of low-energy photons — for instance from **axion-like particles** (hypothetical lightweight particles from beyond the Standard Model) converting in Earth's magnetic field — striking the ice at the **Brewster angle** would reflect *without* phase inversion, faking an up-going signature. The Brewster angle is the special incidence angle at which one polarization of reflected light vanishes — the same physics that makes polarized sunglasses kill lake glare at one particular viewing angle. For ANITA's geometry, that magic angle is about **−37°** — uncomfortably close to both steep-event elevations (−27.4° and −35.0°). Second, the axion-to-photon conversion can be resonantly amplified by factors of hundreds to a thousand in the **ionosphere**, Earth's electrically charged upper layer — supplying the brightness. And because the events would be low-energy photons rather than EeV neutrinos, IceCube and Auger would see nothing — neatly sidestepping every null result.

**Status: open and unfalsified so far — with published kill-conditions.** This is the most disciplined proposal on record: its authors specified exactly how to test it, including a reanalysis with relaxed trigger cuts looking for paired events and non-geomagnetic polarization patterns [S]. Until someone runs those tests, it stands.

#### (e) Unknown radio propagation near the horizon — the standing suspicion

This is less a single paper than a persistent, openly voiced hunch — most clearly articulated by **Stephanie Wissel** in June 2025 [B/A], whose assessment deserves quotation in full:

> The signals are "most likely not representing neutrinos." Her working guess: "some interesting radio propagation effect occurs near ice and also near the horizon that I don't fully understand." And: "it does not indicate that there is new physics, but rather more information to add to the story."

The supporting fingerprints inside ANITA's own data: the two ANITA-IV events with suppressed low-frequency power (≲500 MHz) — precisely the kind of distortion long near-horizon atmospheric paths produce [S: PRD 105] — and the near-horizon clustering of all four ANITA-IV events, exactly where propagation physics is most exotic. Independent fieldwork has begun quantifying how weird near-surface radio over ice can be: RNO-G's measurements at Summit, Greenland, show sub-nanosecond time-of-flight structure and **seasonal** variation in the firn's refractive index — genuine, irreducible systematics for any experiment that reconstructs events from radio skimming the ice [A: ARENA 2026 material].

**Status:** no one has yet produced a quantitative propagation mechanism reproducing the events' polarization, coherence, and angular pattern. The category remains a hunch with partial fingerprints — and it is the hunch of the scientist best positioned to know.

### 5.2 Family Two: Standard-Model-adjacent particle physics — all disfavored

- **Plain Earth-skimming tau neutrinos.** The legitimate door, described in §3.3. It fails on flux (IceCube's regeneration argument, §4.1) and on angular distribution: the Standard Model predicts Earth-skimming events should cluster *at* the horizon, while ANITA's two famous events arrived steeply from well below it [S].
- **Sterile neutrinos.** Cherry & Shoemaker (PRD 99, 063016) and Huang et al. (PRD 98, 043019) showed that a hypothetical fourth, "sterile" neutrino mixing with the tau flavor could raise the through-Earth survival probability enough to explain the events [S]. Elegant — but the same mixing predicts IceCube should detect roughly **six times** ANITA's event rate. IceCube's null result kills it [S]. This is the cleanest example in the whole landscape of a theory that explains the anomaly perfectly and the rest of reality not at all.

### 5.3 Family Three: beyond-Standard-Model physics — constrained, mostly squeezed

Each entry below was a serious, calculation-level proposal, published in reputable journals, taken seriously by the community. Each now carries an observational wound.

- **Superheavy dark matter.** The early universe may have produced relic particles far heavier than anything at the LHC; their slow decays could yield the events (Hooper et al., PRD 100, 043019; related work by Fox et al.; boosted-dark-matter variants by Heurtier & Mambrini) [S]. Wounds: the extragalactic gamma-ray background and IceCube/Auger nulls squeeze the decay channel severely; the July 2026 joint analysis (§4.4) narrows the surviving space further.
- **Supersymmetry, several routes.** R-parity-violating bino decays (Collins et al., PRD 99, 043009); long-lived staus — the superpartner of the tau lepton — produced in cosmic-ray air showers and decaying upward (Connolly, Allison, Banerjee, Learned and related 2018 work); sphaleron transitions inside Earth converting baryons to leptons (Anchordoqui & Antoniadis, PLB 790, 578) [S]. Wounds: Large Hadron Collider long-lived-particle searches and the IceCube/Auger null network.
- **Gravitino decay** (Dudas et al., PRD 98, 015030) and **quasi-stable dark matter gravitationally trapped in Earth's core** (Anchordoqui and collaborators) — a genuinely poetic idea: a reservoir of exotic matter accumulated inside the planet over billions of years, decaying upward in occasional bursts [S/A]. Wound: the same flux arithmetic as everything else; also, a trapped reservoir predicts correlations with Earth's mass distribution that the directional data do not obviously show.
- **The BSM tau-like long-lived particle** of Bertólez-Martínez et al. (§4.3): best-fit parameter point **excluded by Auger** [A].
- **Magnetic monopoles and other exotic relics** — cataloged candidate up-going primaries; none has survived contact with the cross-check data [A].

A fair summary of Family Three: these papers did their job. They mapped which new-physics ideas *could* produce the events and showed that most could — briefly. Then the world's observatories voted.

### 5.4 Family Four: speculative cosmology — on the record, not adopted

#### (a) The CPT-symmetric universe, or "the parallel universe" that wasn't

**Pedigree: [S/A] L. Anchordoqui, V. Barger, J. Learned, D. Marfatia, T. Weiler, arXiv:1803.11554, published in LHEP 2, 13 (2018); [C/B] New Scientist, April 2020; [C] USA Today fact-check**

The serious paper proposed something specific and physical: the events could be decays of **right-handed neutrino dark matter** — a candidate relic population — gravitationally captured by the Earth over cosmic time, decaying to a Higgs boson and a tau neutrino [S/A]. That mechanism belongs to Family Three and carries Family Three's wounds.

What the world *heard*, in April 2020, was something else. A *New Scientist* article connected the anomaly to **Neil Turok's CPT-symmetric cosmology** — a speculative but legitimate research program in which the Big Bang produced two universes, ours of matter and a mirror of antimatter, with reversed arrow of time — and the headline machine did the rest [C]: *"We may have spotted a parallel universe going backwards in time"* became, in the tabloid cascade, *"NASA scientists detect parallel universe"* [C]. There was no NASA announcement. There was no detection claim. There was a theoretical proposal about dark matter, and a philosophical cosmology, welded together by deadline pressure.

The pushback is on record: Ibrahim Safa — "a long ways away from even claiming there's any new physics" [B/C]. A USA Today fact-check rated the viral claims "Partly False" [C].

This episode earns its own section in this dossier (Part Six) for one reason: it demonstrates how a genuine, rigorously measured, honestly reported anomaly can be converted into a cultural rumor within a week — which is precisely why every claim in this file carries a pedigree tag, and why the exotic cosmologies are quarantined here, in their own family, clearly labeled as what they are: proposals without experimental support, not discoveries.

#### (b) Villata's antimatter-sector cosmology (2026)

**Pedigree: [S] M. Villata, arXiv:2604.12562, published Annalen der Physik 538, e00616 (2026); reception history documented below**

The most radical entry on record, and the one the project's working notes flagged for special attention. **Massimo Villata**, an astronomer at Italy's National Institute for Astrophysics in Turin, has spent two decades constructing a "lattice Universe" in which CPT symmetry — the deep principle that physics is unchanged when particles are swapped for antiparticles, mirror-reflected, and time-reversed — extends to **gravity itself**: antimatter, in his framework, experiences reversed gravitational interaction, and antimatter domains exist in the large cosmic voids between galaxy concentrations [S: his program's earlier papers, EPL 94, 20001 (2011); Ann. Phys. (2015) on antimatter in Kerr black-hole geometries; the 2012–2013 lattice-Universe papers].

Applied to ANITA, the claims are specific:

- The ANITA-I event's arrival direction lies inside **Void #10 in the constellation Lepus** — a substructure of the Local Void, quoted extent about 6.3 megaparsecs — and Void #19 in Libra is also invoked. In the theory, such voids are where antimatter domains live.
- The up-going events are not up-going at all: they are emissions from antimatter structures that our instruments register with reversed time-ordering and apparent negative energy — which is why they seem to violate the survival arithmetic of §3.3. The impossibility, in this reading, is an artifact of assuming matter-sector physics.
- The paper ties itself to other anomalies: AMS-02's candidate antihelium events, and the ALPHA-g experiment's antihydrogen results (with Villata's own 2024 response to ALPHA-g in its reference list) [S].

**Reception history — kept, because it is evidence about the evidence.** The only formal engagement with Villata's broader program remains a 2011 exchange: physicist Marcoen Cabbolet published a critique (Ap&SS 337; arXiv:1108.4543), with a separate response by D.C. Cross (arXiv:1108.5117), followed by Villata's reply (arXiv:1109.1201) [S/A]. His 2026 ANITA paper is single-author, explicitly speculative, published in a legitimate journal — and as of September 2026 has attracted **no published response specific to its ANITA claims** [gap logged]. It is cataloged here as fringe-but-formal: its central claim is not testable by any experiment currently funded, and no working physicist in the ANITA/KM3NeT/IceCube mainstream has adopted it. But it is published, citable, and on the record — which is where this file keeps it.

---

## PART SIX: THE MEDIA ANOMALY (APRIL–MAY 2020)

**Pedigree: [B] New Scientist, April 8, 2020; [C] tabloid cascade; [C] USA Today fact-check**

Worth its own chapter, because the distortion of this story is itself part of the story — and because anyone researching the topic today inherits the debris.

The sequence, reconstructed from the coverage: on April 8, 2020 — three months after IceCube's null result had made the anomaly look *worse*, not better — *New Scientist* published a piece discussing Neil Turok's CPT-symmetric cosmology as one speculative lens on the ANITA events [C]. The article's headline ventured "we may have spotted a parallel universe going backwards in time." Within days, the New York Post, the Express, the Daily Star, and hundreds of aggregators had converted speculation into announcement: "NASA scientists detect parallel universe" [C]. The chain contained at least three independent failures: there was no NASA statement (NASA funds the balloon; NASA made no claim); there was no detection claim by the collaboration (they had claimed *events without explanation*, a very different thing); and the cosmology cited was a philosophical research program, not a prediction.

The scientific community's response was swift and unified on the record: team members emphasized the anomaly's unexplained status and the live mundane hypotheses; Safa's quote (§5.4a) became the canonical rebuttal; fact-checkers rated the viral version false or partly false [C].

**Why this matters beyond public relations.** The parallel-universe episode contaminated the information environment around a real measurement problem. It created a perverse incentive for working scientists — each new public statement about the anomaly risks re-igniting the carnival — and it seeded the internet with thousands of pages that conflate the ANITA events with every Antarctic myth this project's other topics debunk. Anyone reading about the anomaly today must first clear away a layer of folklore. That clearing-away is one of this document's jobs.

**And the quieter aftermath:** the episode also illustrates something easy to miss — that the *boring* explanations were, and remain, the working hypotheses of the scientists closest to the data. The people most qualified to cry "new physics" have spent fifteen years crying "check the ice."

---

## PART SEVEN: PUEO — THE SUCCESSOR MISSION

**Pedigree: [A] pueo.space mission pages, NASA and university releases (UChicago, Penn State, WashU), stratocat flight records; [S] white paper JINST 16, P08035 (arXiv:2010.02892); [A] sensitivity study arXiv:2512.20594**

When ANITA completed its four flights, the community did what science does with an unsolved problem: it built a better instrument. That instrument is **PUEO** — Hawaiian for the short-eared owl (*Asio flammeus*), a predator that hunts by listening — the first mission selected under NASA's new Astrophysics Pioneers program [A].

### 7.1 The people

- **Abigail Vieregg** (University of Chicago) — Principal Investigator [A].
- **Stephanie Wissel** (Penn State) — co-investigator; the anomaly's most quoted assessor; also a HERON Principal Investigator (Part Eight).
- **Brian Rauch** (Washington University in St. Louis) — ANITA veteran; his institution published the most complete post-flight reporting in August 2026 [B].
- Operations with NASA's Wallops Flight Facility, the Columbia Scientific Balloon Facility, and Peraton/Aerostar balloon support [A].

### 7.2 The instrument: every design choice is an answer to the mystery

This is the part of the PUEO story that deserves slow reading. PUEO's design reads like a checklist of the ANITA anomaly's open questions:

- **Interferometry — 108 main antennas.** Ninety-six dual-polarization antennas arranged in five rings of 24 azimuthal sectors, canted 10° downward, plus a 12-antenna bottom ring canted at 40°. Interferometric timing across the array improves pointing resolution by an order of magnitude over ANITA — because one of ANITA's soft spots was direction reconstruction (two of its four anomalous events carried only 1–2σ direction significance) [A].
- **Frequency coverage 300–1200 MHz, 216 digitized channels**, with signal transported over fiber (radio-over-fiber) to keep the readout clean [A].
- **The sub-payload — the decisive addition.** Four dual-polarization antennas on an eight-channel digitizer, dangling *below* the main payload on a boom, looking outward at the air directly — no ice surface in the path at all. This is the design answer to the firn/reflection controversy: if an up-going shower is real, the sub-payload sees it directly, with no reflection physics involved; if the ANITA events were subsurface or surface-reflection artifacts, the geometry differences expose the trick [A].
- **Low-threshold triggering:** the trigger reaches 50% efficiency for signals below signal-to-noise ratio 1 — pulling weaker, fainter events out of the noise that ANITA's cruder trigger would have missed [A].
- **128 terabytes of onboard storage, triply redundant** — because the payload lands in one of the least accessible places on Earth and the drives are the mission [A].
- **Net sensitivity:** about ten times ANITA's at 1 EeV, spanning 1–1000 EeV, with sub-degree pointing [A].

### 7.3 The flight: December 2025–January 2026

**Pedigree: [A] mission pages, stratocat, WashU reporting dated August 23, 2026**

- **Launch:** December 19, 2025, 16:54–16:56 UTC (05:56 New Zealand time on December 20), from the Long Duration Balloon facility on the Ross Ice Shelf.
- **Duration:** 23 days, 9 hours, floating at roughly 120,000 feet.
- **Calibration companions:** HiCal-3a and HiCal-3b, the latest incarnations of the ice-reflectivity radar, launched roughly a day after the main payload; one flew about 5 days 2 hours and the other about 12 days, once again mapping how radio reflects off Antarctic ice along the flight path [A: ARENA 2026 report]. *Logged discrepancy:* the mission reports consulted during this research attach the two durations to HiCal-3a and HiCal-3b inconsistently; the public record does not consistently state which unit flew which profile.
- **Termination:** 02:00 UTC, January 12, 2026. Landing on the East Antarctic Plateau, roughly 255 kilometers from the South Pole.
- **Recovery:** the payload was recovered by Arctic Trucks vehicles; the data drives were hand-carried back. More than **50 terabytes of data** returned; the instrument staged through Christchurch, New Zealand [A/B].
- **Same-season company:** the Antarctic campaign also carried the GAPS antiparticle-spectrometer payload (roughly a 25-day flight) — logged because campaign manifests occasionally matter when auditing radio-interference candidates [A/B].
- **Conference footprint (design-level only):** an ICRC 2025 presentation (Q. Abarr, "Searching for ultrahigh energy neutrinos with PUEO," PoS 501, 976); a design contribution at Neutrino 2026 (UC Irvine, June 2026); a flight report at ARENA 2026 (June 2026). The mission's publications page lists only the white paper [A].

### 7.4 The prediction ledger: what PUEO should see

**Pedigree: [A] J. Sherman, K. Fang, D. Hooper, "The Sensitivity of PUEO to Cosmogenic Neutrinos and Exotic Physics Scenarios," arXiv:2512.20594 (v2, April 2026)**

A sensitivity study by a team at Wisconsin asked the practical question: under each existing model of the ultra-high-energy sky, how many events does PUEO actually expect? Their numbers, for a 90%-confidence Poisson limit with roughly 2.3 observed events setting the floor:

| Model | Predicted PUEO events |
|---|---|
| Pierre Auger best-fit diffuse neutrino flux | 0.0003 |
| Telescope Array best-fit flux | 0.37 |
| Superheavy dark matter | 0.02 |
| Topological cosmic strings | 0.13 – 1.1 |

Read those numbers slowly. Under every conventional model of the high-energy universe, PUEO is expected to see *essentially nothing*. Which means PUEO functions as a clean binary test: **if the ANITA-anomalous flux was real, PUEO's superior sensitivity should see multiple events, and its sub-payload should see their true geometry. If the anomaly was an artifact of ice, horizon, or instrument, PUEO should see none — and quite possibly tell us what fooled its predecessor.**

### 7.5 Status as of September 2026

Analysis is in progress and, per the team's public statements, may take up to a year from the flight. **First results are expected around December 2026–January 2027** — within months of this document's compilation [A/B]. Nothing physics-level is public yet. Whatever PUEO finds — confirmation, null, or a new oddity — it will be the single most important new evidence in this file's story, and this dossier should be read as the state of play on the eve of that result.

---

## PART EIGHT: RELATED ANOMALIES — THE SAME SIGNATURE, ELSEWHERE

The ANITA events did not appear in a vacuum. Two other observatories, on two other continents, in two different detector technologies, have since produced events that belong to the same evidentiary family: something apparently emerging from solid matter at ultra-high energy, in directions and at rates that strain known physics. Neither confirms ANITA — but each makes "one experiment had one weird glitch" harder to say.

### 8.1 KM3-230213A — the Mediterranean event (February 2023)

**Pedigree: [S] KM3NeT Collaboration, Nature 638, 376 (2025, with erratum); [S] "global landscape" analysis PRX 15, 031016 (2025); [S/A] theory follow-ups cited below**

**The observatory.** KM3NeT is a neutrino telescope at the bottom of the Mediterranean Sea — cubic-kilometer-scale volumes of seawater watched by strings of light sensors. Unlike IceCube, which looks for neutrinos arriving from the sky, KM3NeT's partially built arrays also have unusual sensitivity to particles arriving nearly horizontally — skimming through the Earth's crust beneath the sea floor and emerging into the detector's field of view.

**The event.** In February 2023, KM3NeT recorded a single track, cataloged **KM3-230213A**, with a reconstructed energy in the hundreds of PeV — about 220 PeV in the initial reconstruction, with later global analyses allowing roughly 100–450 PeV depending on the assumed source direction [S]. A single ultra-energetic muon track is not, by itself, anomalous. What strained interpretation was the *rate implied by seeing one such event so early* in the detector's incomplete configuration, and its energy regime, relative to IceCube's and Auger's far larger exposures. The global landscape analysis (PRX 15, 031016) quantified the mismatch at **2.5–3σ tension** [S].

**The theory response — a familiar playbook.** The proposals that followed mapped almost one-to-one onto the ANITA landscape: **Yasaman Farzan** (JHEP 10(2025)208) proposed dark-sector particles that convert to Standard-Model particles inside the detector; **O. Adriani and collaborators** (arXiv:2502.08387) argued for a galactic-origin flux that would reconcile rates; **Vedran Brdar and Dibya Chattopadhyay** (arXiv:2502.21299) worked the connection to up-going air-shower physics [S/A].

**The bridge to ANITA.** The direct link was built by **M. Bertólez-Martínez et al.** (JHEP 07(2023)005): ANITA-IV's near-horizon events and KM3NeT's track could be unified under a single new source — ultra-high-energy particles of a tau-like or muon-like long-lived species produced inside the Earth — with one parameter fit covering both datasets [A]. That unification was the BSM hypothesis later excluded by Auger's null searches (§4.3). And the July 2026 joint analysis (§4.4) folded everything into the 7.5σ/5.9σ reckoning.

**Status: one event, high tension, unresolved.** Logged as **anomaly #2**.

### 8.2 HAWC's horizontal tracks — the Mexican event (August 2026)

**Pedigree: [S/A] HAWC Collaboration, "Anomalous horizontal track-like events at the HAWC observatory: candidate neutrino-induced charged leptons from the Pico de Orizaba volcano," arXiv, submitted August 28, 2026 (inspirehep record 3197860); background pedigree: A. Albert et al., Astropart. Phys. 137, 102670 (2022)**

The newest entry in this file — submitted weeks before compilation, and therefore the least digested.

**The observatory.** HAWC (the High-Altitude Water Cherenkov Observatory) is an array of water tanks on the slope of Mexico's Sierra Negra volcano. When charged particles from an air shower strike the water, they emit faint flashes of blue light (Cherenkov radiation), and the pattern of flashes reconstructs the shower. HAWC looks *up* at the sky — and, along the horizon, at the slopes of neighboring volcanoes.

**The background, first.** HAWC has been seeing horizontal particle tracks — particles skimming in nearly parallel to the ground — for years. Its earlier published analysis (Albert et al., 2022) examined 122 such track events and found the natural explanation: **scattered atmospheric muons**, ordinary cosmic-ray debris that random air-scattering nudges into near-horizontal trajectories, with a most probable energy of only about 4 GeV and a strong suppression of such tracks above 100 GeV [S]. So HAWC's default assumption, like ANITA's, was mundane.

**The anomaly.** The 2026 paper reports track events that **do not fit that population** — anomalous horizontal track-like events whose reconstructed geometry points back at the flank of **Pico de Orizaba**, Mexico's highest volcano, as if the particles originated *inside the mountain* [S/A]. The collaboration's interpretation: candidate **neutrino-induced charged leptons** — neutrinos interacting in the volcano's rock, converting to a tau or muon, which then exits the mountainside and crosses the detector horizontally. That is the same physical channel as ANITA's Earth-skimming taus: neutrino in, dense rock, charged particle out.

**Status: anomaly #3 — days old at research time.** No replication, no independent confirmation, no published theoretical response yet. It is logged exactly as submitted, with the explicit caveat that August-2026 papers have not faced the years of scrutiny that the ANITA events have.

**Why these two matter even without confirmation.** Three observatories, three technologies (radio over ice, light in seawater, light in mountain water), three continents, all reporting the same family of signature — energy emerging from solid matter at impossible angles — gives the collective anomaly a weight no single experiment can carry alone. Equally, none of the three has been confirmed by any other, and the strongest joint statistical statement ("Four, One, and None") says the family *cannot* be reconciled internally under known physics. Both things are true at once, and this file holds them side by side.

---

## PART NINE: THE WIDER DETECTION LANDSCAPE

For completeness — and because the anomaly's resolution may arrive from any direction — here is every major current or planned effort hunting the same signals, each with a note on why it belongs in this file.

- **BEACON** (Benchmark Experiment for Atmospheric Cosmic-ray Observations) — [S/A: JCAP 11(2020)069; prototype results arXiv:2206.09660]. A ground-based proof of concept on White Mountain, California, at 3.8 km altitude, running since 2018: just four crossed dipole antennas at 30–80 MHz, demonstrating that a mountaintop radio array can trigger on air showers. Why it matters here: the BEACON concept — using mountains as the converter for tau neutrinos — fed directly into the PUEO design philosophy, and its next generation adds scintillation detectors.
- **GRAND** (Giant Radio Array for Neutrino Detection) — [A: ICRC 2025 proceedings]. A planned radio array of ~200,000 km² in western China, targeting 10^16.5–10^18 eV cosmic rays and neutrinos. The GRANDProto300 prototype had 65 of 300 antennas deployed by June 2025, with machine-learning (graph neural network) shower reconstruction already demonstrated.
- **RNO-G** (Radio Neutrino Observatory in Greenland) — [S: instrument paper JINST 20, P04015 (2025); Astropart. Phys. 164, 103024]. Seven stations near Summit Station, Greenland, listening for Askaryan pulses in the ice. Two entries in its record matter directly to the ANITA mystery: it has detected radio emission from solar flares and cosmic-ray showers (proving its ears work), and its ARENA 2026 measurements of the firn's refractive index — sub-nanosecond time-of-flight structure with **seasonal** variation — quantify the near-surface radio-propagation systematics that the "unknown propagation near ice and horizon" hypothesis invokes. The ice's radio behavior at the surface is genuinely more complicated than simple models assume; RNO-G is measuring exactly how.
- **HERON** — [A/S: ERC Synergy Grant announcement, December 2025; Penn State release]. The next-generation ground array: a €14 million European Research Council Synergy Grant (a 66-of-712 success rate; Penn State frames its share within a $16.3M total), with Principal Investigators **Kumiko Kotera** (IAP, Paris), **Jaime Álvarez-Muñiz** (IGFAE, Spain), **Martine Martineau** (LPNHE), and **Stephanie Wissel** (Penn State), and Argentina's CNEA as a partner. Design: 24 phased radio stations of 24 antennas each, plus 360 standalone antennas, along a 72 km ridge line at ~1,000 m elevation in San Juan province, Argentina — projected sensitivity 10–20× current instruments, sub-degree resolution, on an initial six-year construction-and-operations program. The thread to notice: Wissel — the anomaly's most careful public assessor — is building the machine intended to see it, or its absence, at scale.
- **POEMMA / PBR** — [A: Snowmass materials]. The Probe of Extreme Multi-Messenger Astrophysics concept; its balloon-radio pathfinder, PBR (POEMMA Balloon with Radio), is scheduled for a 2028 flight from Wanaka, New Zealand — another balloon ear over the southern ice.
- **EUSO-SPB2** — [S/A: arXiv:2511.10944]. The Extreme Universe Space Observatory's second super-pressure balloon, flown May 2023 (cut short at 36 hours 52 minutes by a balloon failure), carrying a Cherenkov telescope that watches the atmosphere in optical light. It observed atmosphere-skimming shower candidates, has now published its first neutrino constraints, and its planned AS-shower program is explicitly aimed at quantifying refraction near Earth's limb — the same physics sitting under the ANITA anomaly.
- **The South Pole itself.** IceCube's continued operation and its 2025 ultra-high-energy constraints (PRL 135, 031001) keep tightening the flux ceiling under which every explanation must fit — each year of IceCube nulls is another year of exclusion for diffuse models.

A landscape this crowded has a message: even if every anomalous event on record turns out to be a mirage, the world's physics community now has a dozen instruments designed around the possibility that the mirage is hiding something real. That, in itself, is a lasting consequence of six unexplained radio pulses over Antarctica.

---

## PART TEN: MASTER TIMELINE

| Date | Event | Pedigree |
|---|---|---|
| 1962 | Gurgen Askaryan predicts coherent radio emission from particle cascades in dense media | [S] |
| 2000 | Saltzberg et al. observe the Askaryan effect at the Stanford Linear Accelerator — the future ANITA team's first proof | [S] |
| Dec 14, 2006 | ANITA-I launches from the Ross Ice Shelf | [S/B] |
| Dec 28, 2006 | Event 3985267 — the first anomaly — recorded at 00:33:20 UTC | [S] |
| Dec 2008 | ANITA-II flies, with a deliberately air-shower-insensitive trigger | [A/B] |
| Dec 17, 2014 | ANITA-III launches | [S/B] |
| Dec 20, 2014 | Event 15717147 — the second anomaly — recorded at 08:33:22.5 UTC | [S] |
| Jan 2015 | HiCal-1 calibration flight: glancing-angle ice reflectivity exceeds textbook predictions | [S] |
| 2016 | PRL 117, 071101 published: the ANITA-I anomalous event, plus three atmosphere-skimming events | [S] |
| Dec 2, 2016 | ANITA-IV launches, carrying HiCal-2 and the new notch filters | [S/B] |
| Dec 2016 | The four near-horizon events recorded | [S] |
| 2018 | PRL 121, 161102 published: the ANITA-III event, the SN 2014dz coincidence, first cross-checks | [S] |
| Jan 8, 2020 | IceCube's regeneration null result published (ApJ 892) | [S] |
| Apr 8, 2020 | New Scientist's "parallel universe" article triggers the global tabloid cascade; team pushback follows within days | [B/C] |
| 2020 | Firn/subsurface-reflection hypothesis published (Shoemaker et al.); axion-Brewster proposal (Esteban et al.); HiCal-vs-firn rebuttal analysis (Gorham et al., published 2021) | [S/A] |
| 2021 | PRL 126, 071103: the four ANITA-IV near-horizon events announced | [S] |
| 2022 | PRD 105, 042001 (Prechelt et al.): full ANITA-IV analysis — the low-frequency anomaly documented; KM3NeT records KM3-230213A in February; HAWC's 122-track background study published | [S] |
| May 2023 | EUSO-SPB2 flies (36 h 52 m, curtailed); atmosphere-skimming candidates observed | [S/A] |
| 2023 | ANITA-IV + KM3NeT unification proposal (Bertólez-Martínez et al.) | [A/S] |
| Mar 2025 | Auger PRL 134, 121003: up-going shower search finds 1 event vs. 0.27±0.12 expected; ANITA-normalized flux excluded | [S] |
| 2025 | KM3-230213A published (Nature 638, 376, with erratum); global-tension analysis (PRX 15, 031016); IceCube UHE constraints (PRL 135, 031001) | [S] |
| Jun 2025 | Wissel's public assessment: the signals are "most likely not representing neutrinos"; her horizon-propagation guess enters the record; PUEO sensitivity study submitted (revised April 2026) | [B/A] |
| Dec 19, 2025 | PUEO launches from the Ross Ice Shelf at 16:54–16:56 UTC | [A] |
| Dec 2025 | HERON awarded its €14M ERC Synergy Grant | [A/S] |
| Jan 12, 2026 | PUEO flight terminated; landing on the East Antarctic Plateau ~255 km from the Pole; recovery by Arctic Trucks; 50+ TB of data secured | [A/B] |
| Apr 14, 2026 | Villata submits the antimatter-sector ANITA paper (published: Ann. Phys. 538, e00616) | [S] |
| Jul 21, 2026 | "Four, One, and None" (arXiv:2607.19487): the joint 7.5σ / 5.9σ reckoning | [A/S] |
| Aug 23, 2026 | Washington University publishes its detailed PUEO recovery feature; analysis ongoing | [B/A] |
| Aug 28, 2026 | HAWC submits its anomalous horizontal-track paper (Pico de Orizaba) | [S/A] |
| ~Dec 2026 – Jan 2027 | PUEO first results expected — the next decisive date in this file | [A] |

---

## PART ELEVEN: OPEN THREADS, GAPS, AND DATA DISCREPANCIES

Everything unresolved, in one place. These are not footnotes; they are the research agenda — the list a future investigator, journalist, or doctoral student could work from tomorrow.

1. **PUEO's results.** The single most important open thread, expected within months of this writing. PUEO's sub-payload geometry was designed specifically to arbitrate between "real up-going events" and "reflection/propagation artifact." Whatever it finds moves this file's story decisively.
2. **The firn hypothesis vs. HiCal — a published standoff.** Shoemaker's subsurface-reflector model needs ~7% areal coverage; HiCal-2's waveforms allow 2–3% and disfavor the model; the ANITA-IV near-horizon events appear irreconcilable with subsurface reflection at their geometries (>95% surface amplitude reflection) [S vs. S]. Two honest, published analyses point in opposite directions.
3. **The radar survey that was proposed and never published.** Ground-truthing radar of the two steep-event sites was specified as the decisive test in 2019–2020. Six years on, no such survey has appeared in any index. Whether it was ever done is not on the public record.
4. **The promised ANITA-IV coordinate paper never appeared.** PRD 105 committed to publishing the four events' true reconstructed sky coordinates in a follow-up. Searched for three separate times across two research runs; no such paper exists. The missing coordinates block every independent sky-association analysis.
5. **The low-frequency anomaly inside the anomaly.** Two of the four ANITA-IV events arrived with power missing below ~500 MHz — attributed in the paper itself to unmodeled long-path atmospheric effects. Unexplained and unmodeled to this day [S].
6. **No response to Villata (2026).** The antimatter-void ANITA paper stands unrebutted and unadopted; the only reception history for its author's program is the 2011–2012 critique chain [S/A].
7. **Cross-collaboration discrepancies on record:** (a) ANITA-III event elevation −35.0° [S] vs. −36.7° [A]; (b) event energies 0.56–0.6 EeV [S: ANITA] vs. ~0.2 EeV [A: Auger conference slides] under different shower-model reconstructions; (c) ANITA-IV launch December 2 vs. December 6, 2016 [B vs. A]; (d) the ANITA-I event's a posteriori background probability quoted between ~10⁻⁵ and ~4×10⁻⁴ across sources; (e) per-flight Type 2 counts summing to 54 vs. a program total of 64 [S vs. A]; (f) HiCal-3a/3b duration assignments swapping between mission reports [A]; (g) the project's working summary sheet described ANITA as "flown 2016–2018" — in fact the flights were 2006–2016 and the *publications* were 2016/2018; corrected and flagged here.
8. **HAWC anomaly #3 is weeks old** at research time: no replication, no independent confirmation, no published theory response [S/A].
9. **The technosignature side-door (peripheral, logged for completeness).** A May 2026 paper explored adapting ANITA-class radio-interference mitigation techniques to the search for extraterrestrial technosignatures — evidence of how portable the instrument craft has become, though peripheral to the anomaly itself [A].
10. **The missing middle.** No published analysis yet combines *all six* ANITA events (steep + near-horizon) with the KM3NeT and HAWC candidates in one statistical framework; "Four, One, and None" covers ANITA-IV and KM3NeT only. A six-plus-one-plus-N joint analysis is an obvious next paper, and its absence is a gap in the literature, not just this file.

---

## PART TWELVE: KEY SOURCES (BY PEDIGREE)

**Primary event publications [S]:**
- P. Gorham et al., "Characteristics of Four Upward-Pointing Cosmic-Ray-like Events Observed with ANITA," PRL 117, 071101 (2016)
- P. Gorham et al., "Observation of an Unusual Upward-going Cosmic-ray-like Event in the Third Flight of ANITA," PRL 121, 161102 (2018)
- ANITA Collaboration, "Unusual Near-Horizon Cosmic-Ray-like Events Observed by ANITA-IV," PRL 126, 071103 (2021)
- S. Prechelt et al., "Analysis of a tau neutrino origin for the near-horizon air shower events observed by the fourth flight of the Antarctic Impulsive Transient Antenna," PRD 105, 042001 (2022)
- P. Gorham et al., ANITA-IV diffuse ultra-high-energy neutrino flux constraint, PRD 99, 122001 (2019)
- M. Aartsen et al. (IceCube), ApJ 892 (2020), arXiv:2001.01737
- Pierre Auger Collaboration, "Search for the anomalous events detected by ANITA using the Pierre Auger Observatory," PRL 134, 121003 (2025)
- A. Vieregg et al., "The Payload for Ultrahigh Energy Observations (PUEO): A White Paper," JINST 16, P08035 (2021), arXiv:2010.02892
- J. Cherian et al., HiCal calibration papers, arXiv:1703.00415; PRD 98, 042004
- P. Gorham et al., "Experimental constraints on the subsurface reflection model for the anomalous ANITA events," JCAP 04(2021)016, arXiv:2009.13010

**Explanation papers [S/A]:**
- I. Shoemaker et al., Annals of Glaciology (2020), arXiv:1905.02846 — firn/subsurface reflection
- M. Motloch et al., PRD 95, 043004 (2017); K. de Vries & S. Prohira (2019) — transition radiation
- J. Cherry & I. Shoemaker, PRD 99, 063016; J. Huang et al., PRD 98, 043019 — sterile neutrinos
- R. Esteban, J. López-Pavón, M. Martínez-Soler, J. Salvado, EPJC 80, 259 (2020) — phase-inversion limits; Brewster/axion proposal
- L. Anchordoqui et al., arXiv:1803.11554, LHEP 2, 13 (2018) — right-handed-neutrino dark matter; N. Turok's CPT cosmology via New Scientist (Apr 2020) [C]
- D. Hooper et al., PRD 100, 043019 — superheavy dark matter; S. Dudas et al., PRD 98, 015030 — gravitino; P. Collins et al., PRD 99, 043009 — RPV bino; L. Anchordoqui & I. Antoniadis, PLB 790, 578 — sphalerons; P. Allison, S. Banerjee, J. Conway, J. Learned, PRD 98, 083002 — long-lived particles
- M. Bertólez-Martínez et al., JHEP 07(2023)005, arXiv:2305.03746 — BSM unification of ANITA-IV + KM3NeT (Auger exclusion follow-up, NEUTRINO 2024)
- M. Villata, arXiv:2604.12562 → Ann. Phys. 538, e00616 (2026); background program: EPL 94, 20001 (2011); Ann. Phys. (2015); lattice-Universe papers (2012–2013); critique chain: M. Cabbolet, Ap&SS 337 / arXiv:1108.4543; D.C. Cross, arXiv:1108.5117; Villata reply, arXiv:1109.1201

**Joint and recent analyses [A/S]:**
- D. Chattopadhyay, C. Argüelles et al., "Four, One, and None," arXiv:2607.19487 (2026)
- KM3NeT Collaboration, Nature 638, 376 (2025, with erratum); global landscape, PRX 15, 031016 (2025); Y. Farzan, JHEP 10(2025)208; O. Adriani et al., arXiv:2502.08387; V. Brdar & D. Chattopadhyay, arXiv:2502.21299
- HAWC Collaboration, "Anomalous horizontal track-like events…," arXiv (Aug 2026), inspirehep 3197860; background: A. Albert et al., Astropart. Phys. 137, 102670 (2022)
- EUSO-SPB2 CT: arXiv:2511.10944 (Nov 2025); AS-shower radio emission: M. Tueros et al., JCAP 01(2025)112; ANITA AS events: arXiv:2404.01239
- PUEO sensitivity: J. Sherman, K. Fang, D. Hooper, arXiv:2512.20594 (v2, Apr 2026)
- IceCube UHE constraints, PRL 135, 031001 (2025) — the flux ceiling under all EeV explanations
- J. Salvado, review/conference material incl. arXiv:2309.17139

**Institutional and mission sources [A/B]:**
- pueo.space mission and publications pages; UChicago, Penn State, WashU releases (2025–2026); WashU physics feature, Aug 23, 2026; NASA/CSBF/stratocat flight records
- ICRC 2025 (Q. Abarr, PoS 501, 976); Neutrino 2026 (UC Irvine, PUEO design contribution); ARENA 2026 (PUEO flight report; RNO-G firn measurements)
- HERON: ERC Synergy Grant announcement (Dec 2025); Penn State release ($16.3M framing); IAP project page
- BEACON: JCAP 11(2020)069; GRANDProto300 ICRC 2025 proceedings; RNO-G: JINST 20, P04015; Astropart. Phys. 164, 103024; POEMMA/PBR: Snowmass materials
- Media record: New Scientist (Apr 8, 2020); USA Today fact check ("Partly False"); Wissel quotes via Penn State/ScienceDaily (Jun 2025); E. Siegel, Medium (Jun 2025) [B/C]

---

## CLOSING NOTE

This file was compiled under a standing rule: no adopted theories, no omitted evidence, no smoothed contradictions. The ANITA anomaly survives that treatment intact — which is itself informative. Six rigorously measured events, fifteen years of the world's best cross-checks, a published seven-and-a-half-sigma statement that the Standard Model cannot hold them all, a calibration standoff over the ice itself, a promised paper that never came, a radar survey that never published, and a successor mission — aloft as this was written — carrying the specific instrument that can settle it.

The most honest sentence in the record remains the one Stephanie Wissel gave in June 2025 [B]: the events do not announce new physics. They are, as she put it, "more information to add to the story." That story's next chapter is already on hard drives in Christchurch, and it is expected before this document is a season old.

*End of compilation. September 2026.*
