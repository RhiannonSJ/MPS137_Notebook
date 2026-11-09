# Neutrinos in the Standard Model

The **Standard Model of particle physics** classifies all known fundamental particles into elementary matter particles (fermions) and force-carrying particles (bosons).

Fermions are divided into two distinct families:

* **Quarks:** Particles that interact via the strong force (as well as weak and electromagnetic forces) to form hadrons like protons and neutrons.
* **Leptons:** Particles that do not feel the strong nuclear force.

Leptons are split into two categories:

1. **Charged Leptons:** The electron ($e^-$), muon ($\mu^-$), and tau ($\tau^-$), which carry an electric charge of $-1e$ and interact via electromagnetism and the weak force.
2. **Neutral Leptons (Neutrinos):** The electron neutrino ($\nu_e$), muon neutrino ($\nu_\mu$), and tau neutrino ($\nu_\tau$), which carry zero electric charge and interact **only via the weak nuclear force** (and gravity).

Because neutrinos lack electric charge and colour charge, they pass through ordinary matter almost unimpeded. In the original Standard Model framework, neutrinos were assumed to be **massless**, left-handed particles.

# Historical Background

In the early 20th century, measurements of beta decay showed that electrons were emitted with a continuous spectrum of energies, appearing to violate the laws of conservation of energy and momentum.

* **1930 (The Hypothesis):** Wolfgang Pauli proposed a neutral, lightweight particle—the "neutrino"—emitted alongside the electron during beta decay to carry away the missing energy and momentum.[^1]
* **1956 (Discovery):** Clyde Cowan and Frederick Reines experimentally detected electron antineutrinos near a nuclear reactor via inverse beta decay.[^2]
* **1960s (The Solar Neutrino Problem):** Raymond Davis Jr. built a massive underground detector filled with cleaning fluid (tetrachloroethylene) in the Homestake Gold Mine. He measured the flux of electron neutrinos coming from nuclear fusion in the centre of the Sun but consistently detected only about **one-third to one-half** of the rate predicted by astrophysicist John Bahcall's solar models.[^3]
* **1998–2001 (Resolution):** The Super-Kamiokande experiment in Japan (studying atmospheric neutrinos)[^4] and the Sudbury Neutrino Observatory (SNO) in Canada (studying solar neutrinos)[^5] confirmed that neutrinos change "flavour" on their way to Earth. This phenomenon is known as **neutrino oscillation**.

# Underlying Physics

Neutrinos come in three distinct **flavours** associated with their corresponding charged leptons:

* Electron neutrino ($\nu_e$)
* Muon neutrino ($\nu_\mu$)
* Tau neutrino ($\nu_\tau$)

## Flavour States vs. Mass States

The key to neutrino oscillations lies in the distinction between how neutrinos interact and how they travel:

1. **Flavour Eigenstates ($\nu_e, \nu_\mu, \nu_\tau$):** States produced or detected in weak interactions alongside an electron, muon, or tau.
2. **Mass Eigenstates ($\nu_1, \nu_2, \nu_3$):** States with definite, specific masses ($m_1, m_2, m_3$) that propagate through space as matter waves.

A neutrino produced as a specific flavour is not a single particle with a single mass, but rather a **quantum superposition** (a linear combination) of mass states.

## The PMNS Matrix

In the full three-flavour framework, the relationship between flavour eigenstates and mass eigenstates is defined by the **Pontecorvo–Maki–Nakagawa–Sakata (PMNS) matrix** ($U$):[^6][^7]

$$\begin{pmatrix} \nu_e \\ \nu_\mu \\ \nu_\tau \end{pmatrix} = \begin{pmatrix} U_{e1} & U_{e2} & U_{e3} \\ U_{\mu 1} & U_{\mu 2} & U_{\mu 3} \\ U_{\tau 1} & U_{\tau 2} & U_{\tau 3} \end{pmatrix} \begin{pmatrix} \nu_1 \\ \nu_2 \\ \nu_3 \end{pmatrix}$$

The PMNS matrix can be parameterised by three mixing angles ($\theta_{12}, \theta_{23}, \theta_{13}$) and a CP-violating phase factor ($\delta$):

$$U = \begin{pmatrix} 1 & 0 & 0 \\ 0 & \cos\theta_{23} & \sin\theta_{23} \\ 0 & -\sin\theta_{23} & \cos\theta_{23} \end{pmatrix} \begin{pmatrix} \cos\theta_{13} & 0 & \sin\theta_{13}e^{-i\delta} \\ 0 & 1 & 0 \\ -\sin\theta_{13}e^{i\delta} & 0 & \cos\theta_{13} \end{pmatrix} \begin{pmatrix} \cos\theta_{12} & \sin\theta_{12} & 0 \\ -\sin\theta_{12} & \cos\theta_{12} & 0 \\ 0 & 0 & 1 \end{pmatrix}$$

* **$\theta_{12}$ (Solar Angle):** Dominates oscillations of solar neutrinos.
* **$\theta_{23}$ (Atmospheric Angle):** Dominates oscillations of atmospheric neutrinos.
* **$\theta_{13}$ (Reactor/Short-Baseline Angle):** Governs transitions between first and third mass states.
* **$\delta$ (CP-Violating Phase):** Determines whether neutrinos and antineutrinos oscillate at different rates.

## Quantum Superposition and Quantum Beats

* When an electron neutrino ($\nu_e$) is created, it is emitted as a wave packet made of $\nu_1, \nu_2,$ and $\nu_3$.
* As the neutrino travels through space at near light speed, the mass components travel with slightly different wave frequencies because their masses ($m_1, m_2, m_3$) differ.
* This difference in propagation speeds creates an interference pattern (similar to musical "beats").
* As a result, the probability of detecting the particle as a $\nu_e, \nu_\mu,$ or $\nu_\tau$ oscillates as a function of distance travelled.

## Probability Equations

### Two-Flavour Approximation

For simplified calculations involving two-neutrino mixing, the probability ($P$) that a neutrino of flavour $\alpha$ transforms into flavour $\beta$ after travelling a distance $L$ with energy $E$ is:

$$P(\nu_\alpha \rightarrow \nu_\beta) = \sin^2(2\theta) \cdot \sin^2\left( \frac{\Delta m^2 \cdot L}{4E} \right)$$

### Full Three-Flavour Equation

In the general three-flavour framework, the transition probability from initial flavour $\alpha$ to final flavour $\beta$ includes both CP-conserving (real) and CP-violating (imaginary) components:

$$P(\nu_\alpha \rightarrow \nu_\beta) = \delta_{\alpha\beta} - 4 \sum_{i > j} \text{Re}(U_{\alpha i}^* U_{\beta i} U_{\alpha j} U_{\beta j}^*) \sin^2\left( \frac{\Delta m_{ij}^2 \cdot L}{4E} \right) + 2 \sum_{i > j} \text{Im}(U_{\alpha i}^* U_{\beta i} U_{\alpha j} U_{\beta j}^*) \sin\left( \frac{\Delta m_{ij}^2 \cdot L}{2E} \right)$$

Where:

* **$\delta_{\alpha\beta}$:** Kronecker delta (1 if $\alpha = \beta$, 0 if $\alpha \neq \beta$).
* **$U_{\alpha i}$:** Elements of the PMNS matrix.
* **$\text{Re}(\dots)$ & $\text{Im}(\dots)$:** The real and imaginary parts of the PMNS matrix element product.
* **$\Delta m_{ij}^2 = m_i^2 - m_j^2$:** Mass-squared differences between mass states $i$ and $j$.
* **$L$:** Distance travelled from source to detector.
* **$E$:** Energy of the neutrino.

**(Note: For antineutrinos, the sign of the imaginary term is reversed, allowing tests for CP violation.)**

# Short-Baseline Anomalies and Beyond the Standard Model (BSM) Physics

While the standard 3-flavour oscillation framework successfully explains the majority of solar, atmospheric, and long-baseline reactor data, several persistent experimental anomalies at short baselines (where $L/E \sim 1\text{ m/MeV}$ or $1\text{ km/GeV}$) conflict with standard predictions.

## Experimental Tensions

* **LSND and MiniBooNE Anomalies:** The Liquid Scintillator Neutrino Detector (LSND)[^8] and MiniBooNE experiments observed a significant excess of electron-type (anti)neutrinos in muon (anti)neutrino beams over short distances. This suggested an oscillation driven by a mass-squared difference of $\Delta m^2 \sim 1\text{ eV}^2$—much larger than the solar ($\sim 10^{-5}\text{ eV}^2$) or atmospheric ($\sim 10^{-3}\text{ eV}^2$) mass splittings.
* **Gallium Anomaly:** Underground calibration tests using radioactive sources (SAGE, GALLEX, and BEST) measured an unexpected deficit (20–24%) of electron neutrinos reacting with gallium targets at distances of less than a few metres.[^9]
* **Reactor Antineutrino Anomaly:** Early re-evaluations of reactor fluxes indicated an overall deficit in expected electron antineutrinos detected a short distance from nuclear cores.[^10]

## The Sterile Neutrino Hypothesis (3+1 Model)

To explain these anomalies within an oscillation paradigm, theorists proposed extending the PMNS framework by introducing one or more **sterile neutrinos** ($\nu_s$):

* **Properties:** Sterile neutrinos possess no weak charge ($I_3 = 0, Q = 0$) and interact exclusively via **gravity**. They do not couple directly to standard $W^\pm$ or $Z^0$ bosons.
* **Mechanism:** Active neutrinos ($\nu_e, \nu_\mu, \nu_\tau$) can mix with a fourth, predominantly sterile mass eigenstate ($\nu_4$) with mass $m_4 \sim 1\text{ eV}$. This allows ultra-fast oscillations at very short distances.

$$\begin{pmatrix} \nu_e \\ \nu_\mu \\ \nu_\tau \\ \nu_s \end{pmatrix} = \begin{pmatrix} U_{e1} & U_{e2} & U_{e3} & U_{e4} \\ U_{\mu 1} & U_{\mu 2} & U_{\mu 3} & U_{\mu 4} \\ U_{\tau 1} & U_{\tau 2} & U_{\tau 3} & U_{\tau 4} \\ U_{s1} & U_{s2} & U_{s3} & U_{s4} \end{pmatrix} \begin{pmatrix} \nu_1 \\ \nu_2 \\ \nu_3 \\ \nu_4 \end{pmatrix}$$

## Current Status and Alternative BSM Hypotheses

Recent high-precision measurements have severely constrained the simplest "3+1" single sterile neutrino scenario:

* High-precision experiments like **MicroBooNE** at Fermilab[^11] and **KATRIN** tritium decay measurements[^12] have strongly disfavoured or ruled out the baseline "3+1" model across significant portions of its expected parameter space.
* Alternative BSM solutions under active investigation include:
  1. **Multi-Sterile Models (3+N):** Incorporating two or more sterile states to account for complex interference patterns.
  2. **Decaying Sterile Neutrinos:** Models where a heavy sterile state decays in flight into lighter particles (e.g., a photon or scalar boson plus an active neutrino), producing the observed excess electromagnetic signals.
  3. **Non-Standard Interactions (NSIs):** Hypothesising new, exotic fundamental forces or matter interactions that modify neutrino propagation without needing additional physical mass states.

# CP Violation and Cosmological Consequences

In particle physics, **CP symmetry** combines Charge Conjugation (C), which transforms a particle into its antiparticle, and Parity (P), which flips spatial coordinates like a mirror image.

**Charge Conjugation (C) and Parity (P) Operations:**

* **Charge Conjugation (C):** Converts a left-handed neutrino $\nu_L$ into a hypothetical left-handed antineutrino $\bar{\nu}_L$.
* **Parity (P):** Flips spatial coordinates and helicity, converting $\nu_L$ into a right-handed neutrino $\nu_R$.
* **Combined CP Operation:** Maps a physical left-handed neutrino $\nu_L$ directly to a physical right-handed antineutrino $\bar{\nu}_R$.

$$\nu_L \quad \xrightarrow{\text{Charge Conjugation (C)}} \quad \bar{\nu}_L \quad \xrightarrow{\text{Parity (P)}} \quad \bar{\nu}_R$$

## CP Violation in Neutrino Oscillations

If CP symmetry holds, neutrinos and antineutrinos behave identically under physical laws, meaning $P(\nu_\alpha \rightarrow \nu_\beta) = P(\bar{\nu}_\alpha \rightarrow \bar{\nu}_\beta)$. However, if the phase factor $\delta \neq 0, \pi$ in the PMNS matrix:

* The imaginary term in the oscillation probability changes sign between neutrinos and antineutrinos.
* Consequently, **neutrinos and antineutrinos oscillate at different rates**.

## The Baryon Asymmetry of the Universe

According to the Big Bang model, equal amounts of matter and antimatter should have been created in the early universe. Had they behaved identically, they would have completely annihilated, leaving behind a universe made purely of photons.

To explain why our universe is made almost entirely of matter, Andrei Sakharov showed that three conditions must be met:[^13]

1. **Baryon number violation:** Mechanisms that change the net amount of matter.
2. **(C) and CP violation:** Differences in physical behaviour between matter and antimatter.
3. **Interactions out of thermal equilibrium:** Processes occurring during rapid cosmic expansion.

While CP violation is observed in the quark sector, it is mathematically far too small to explain the observed surplus of matter.

## Leptogenesis: The Neutrino Connection

Leptogenesis is a primary BSM candidate for solving this puzzle using neutrino CP violation:[^14]

* **Heavy Majorana Neutrinos:** Very heavy, right-handed neutrinos created at extremely high energies in the early universe decay unevenly into leptons versus antileptons due to leptonic CP violation ($\delta \neq 0$).
* **Lepton-to-Baryon Conversion:** Sphaleron processes (non-perturbative electroweak interactions) then convert this excess of leptons into a net surplus of **baryons** (protons and neutrons).

Thus, measuring CP violation in current and upcoming long-baseline experiments (such as DUNE and Hyper-Kamiokande) could provide the crucial evidence explaining **why matter exists today**.

# Key Takeaways for Physics

* **Non-Zero Mass:** If neutrino oscillations occur, then at least two $\Delta m^2$ values must be non-zero, mathematically proving that **neutrinos must have non-zero mass**.
* **Standard Model Extension:** The original Standard Model assumed neutrinos were completely massless. The discovery of oscillations required a fundamental expansion of particle physics theory, and ongoing short-baseline anomalies continue to push searches for new physics.
* **Cosmological Link:** Leptonic CP violation via neutrino oscillations offers one of the most promising avenues to explain the matter-antimatter asymmetry of the Universe.

---

## References

[^1]: Pauli, W. (1930). Open letter to the group of Radioactive Persons at the Regional Society meeting in Tübingen.
[^2]: Cowan, C. L., Reines, F., et al. (1956). "Detection of the Free Neutrino: a Confirmation". *Science*, 124(3212), 103–104.
[^3]: Davis, R., Harmer, D. S., & Hoffman, K. C. (1968). "Search for Neutrinos from the Sun". *Physical Review Letters*, 20(21), 1205.
[^4]: Fukuda, Y., et al. (Super-Kamiokande Collaboration) (1998). "Evidence for Oscillation of Atmospheric Neutrinos". *Physical Review Letters*, 81(8), 1562.
[^5]: Ahmad, Q. R., et al. (SNO Collaboration) (2001). "Measurement of the Rate of $\nu_e + d \rightarrow p + p + e^-$ Interactions Produced by $^8\text{B}$ Solar Neutrinos at the Sudbury Neutrino Observatory". *Physical Review Letters*, 87(7), 071301.
[^6]: Pontecorvo, B. (1957). "Inverse Beta Processes and Non-conservation of Lepton Charge". *JETP*, 7, 172.
[^7]: Maki, Z., Nakagawa, M., & Sakata, S. (1962). "Remarks on the Unified Model of Elementary Particles". *Progress of Theoretical Physics*, 28(5), 870–880.
[^8]: Athanassopoulos, C., et al. (LSND Collaboration) (1996). "Evidence for $\bar{\nu}_\mu \rightarrow \bar{\nu}_e$ Oscillations from the LSND Experiment". *Physical Review Letters*, 77(15), 3082.
[^9]: Barinov, V. V., et al. (BEST Collaboration) (2022). "Results from the Baksan Experiment on Sterile Neutrinos (BEST)". *Physical Review Letters*, 128(23), 232501.
[^10]: Mention, G., et al. (2011). "The Reactor Antineutrino Anomaly". *Physical Review D*, 83(7), 073006.
[^11]: Abratenko, P., et al. (MicroBooNE Collaboration) (2022). "Search for an Excess of Electron Neutrino Interactions in MicroBooNE". *Physical Review Letters*, 128(24), 241801.
[^12]: Aker, M., et al. (KATRIN Collaboration) (2022). "Direct Neutrino-Mass Measurement with Sub-eV Sensitivity". *Nature Physics*, 18, 160–166.
[^13]: Sakharov, A. D. (1967). "Violation of CP Invariance, C Asymmetry, and Baryon Asymmetry of the Universe". *JETP Letters*, 5, 24–27.
[^14]: Fukugita, M., & Yanagida, T. (1986). "Baryogenesis Without Grand Unification". *Physics Letters B*, 174(1), 45–47.