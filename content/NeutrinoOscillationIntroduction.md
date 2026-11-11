# Fundamental Neutrino Physics and Oscillations
*Based on MPS 137: Frontiers of Physics – Part 1 (University of Sheffield)*

---

## 1. The Standard Model and Where Neutrinos Fit In

The **Standard Model (SM) of Particle Physics** is the theoretical framework describing all known fundamental matter and three of the four fundamental forces: electromagnetism, the weak interaction, and the strong interaction (excluding gravity).

```
========================================================================================
                                    FERMIONS (Spin 1/2)
----------------------------------------------------------------------------------------
              QUARKS                                         LEPTONS
  (Feel Weak, EM, & Strong Force)                 (Do NOT feel Strong Force)
------------------------------------   -------------------------------------------------
 Generation 1: Up (u), Down (d)          Charged Leptons (-1e)   Neutrinos (0 Charge)
 Generation 2: Charm (c), Strange (s)    e⁻ (Electron, 0.511 MeV) ν_e (Electron Neutrino)
 Generation 3: Top (t), Bottom (b)       μ⁻ (Muon, 105.7 MeV)    ν_μ (Muon Neutrino)
                                         τ⁻ (Tau, 1776.8 MeV)   ν_τ (Tau Neutrino)
========================================================================================
                                    BOSONS (Force Carriers)
----------------------------------------------------------------------------------------
 Vector Bosons (Spin 1): Gluon (g, Strong), Photon (γ, EM), W⁺/W⁻/Z⁰ (Weak Force)
 Scalar Boson (Spin 0):  Higgs Boson (H, Mass generation)
========================================================================================
```

### Lepton Family & Neutrino Properties
Neutrinos ($\nu_e, \nu_\mu, \nu_\tau$) are neutral leptons ($Q=0, C=0$) with spin $1/2$. Because they carry no electric or color charge:
* They **do not feel the strong force** or electromagnetism.
* They interact **strictly via the weak nuclear force** (mediated by $W^\pm$ and $Z^0$ gauge bosons) and gravity.
* In the classical (massless) Standard Model, neutrinos were assumed to be strictly left-handed ($\nu_L$) and antineutrinos right-handed ($\bar{\nu}_R$).

---

## 2. Neutrino Sources and Production Mechanisms in Nature

Neutrinos are produced in nuclear reactions, particle decays, and astrophysical processes across the history of the universe.

```
                          SOURCES OF NEUTRINOS
                          
  Cosmological / Natural                       Anthropogenic (Human-made)
  ----------------------                       --------------------------
  • Big Bang (Cosmic Nu Background)            • Nuclear Power Reactors
  • Solar Core (Fusion pp-chain / CNO)         • Particle Accelerator Beams
  • Supernovae & Cosmic Rays                   • Nuclear Explosions (Atom Bombs)
  • Earth (Geoneutrinos: U/Th/K decay)         • Potassium-40 in Bananas (~5,000 ν/s)
```

### Natural and Human-made Sources
1. **The Big Bang:** Relic neutrinos from cosmic decoupling ($\sim 1\text{ s}$ after the Big Bang) forming the Cosmic Neutrino Background (CNB) with density $\sim 336 \text{ cm}^{-3}$ at $T_\nu \approx 1.95 \text{ K}$.
2. **Solar Neutrinos:** Fusion reactions in the Sun's core ($p + p \rightarrow {}^2\text{H} + e^+ + \nu_e$).
3. **Supernovae:** Core-collapse events release $\sim 99\%$ of their gravitational binding energy as a burst of all neutrino flavours ($\nu_e, \nu_\mu, \nu_\tau$ and their antiparticles).
4. **Atmospheric Neutrinos:** Primary cosmic rays strike air molecules in Earth's atmosphere, creating hadronic cascades:
   $$\pi^\pm \rightarrow \mu^\pm + \nu_\mu (\bar{\nu}_\mu), \quad \mu^\pm \rightarrow e^\pm + \nu_e (\bar{\nu}_e) + \bar{\nu}_\mu (\nu_\mu)$$
5. **Nuclear Reactors:** Beta decay of neutron-rich fission fragments emits intense isotropic fluxes of $\bar{\nu}_e$.
6. **Accelerators:** High-energy proton beams target stationary nuclei (e.g., beryllium or carbon) to generate focused pion/kaon decay channels.
7. **Terrestrial & Biological:** Beta decay of ${}^{40}\text{K}$ in everyday objects (e.g., bananas emit $\sim 5,000 \text{ antineutrinos/second}$).

---

## 3. Neutrino Energies, Cross-Sections, and Experimental Design Implications

### Energy Spectrum vs. Cross-Section
Neutrinos cover over 18 orders of magnitude in energy. The neutrino-nucleon cross-section $\sigma$ scales directly with energy:
* **Low Energy ($E_\nu \sim 1 \text{ MeV}$):** Quasi-elastic / Inverse Beta Decay ($\sigma \sim 10^{-44} \text{ cm}^2$).
* **High Energy ($E_\nu > 10 \text{ GeV}$):** Deep Inelastic Scattering ($\sigma \propto G_F^2 E_\nu$).

```
       NEUTRINO ENERGY SPECTRUM VS. CROSS-SECTION & DETECTORS
       
  Cross Section σ (mb)
    ^
10⁻¹|                                                      Cosmic / AGN
    |                                                      (IceCube, KM3NeT)
10⁻⁷|                                  Atmospheric
    |                                  (Super-K)
10⁻¹³|               Reactor / Solar
    |                (KamLAND, SNO)
10⁻¹⁹|  Big Bang
    |  (PTOLEMY)
10⁻³¹+-------------------------------------------------------------------> E_ν (eV)
       10⁻⁴        1           10⁴          10⁸          10¹²        10¹⁶
```

### The Elusive Nature of Neutrinos
Because $\sigma \sim 10^{-44} \text{ cm}^2$ at solar energies:
$$\text{Mean Free Path } \lambda = \frac{1}{n \cdot \sigma} \approx 6 \times 10^{12} \text{ miles } (\sim 1 \text{ light-year of solid lead})$$
To stop just half of incoming solar neutrinos requires $\sim 6 \text{ trillion miles}$ ($1 \text{ light-year}$) of lead shielding. 

Despite this, **flux is immense**: $\sim 100 \text{ billion } (10^{11})$ solar neutrinos pass through a human thumb every single second.

### Experimental Design Principles
To detect neutrinos efficiently given their tiny cross-section, experiments must satisfy:
1. **Enormous Mass (Volume):** Kilotons to Megatons of active target material.
2. **Background Reduction:** Deep underground installation (under thousands of meters of water equivalent, m.w.e.) to block cosmic ray muons.
3. **High-Intensity Sources:** Placing detectors near megawatt accelerators or multi-gigawatt nuclear reactors.

```
+------------------+-----------------------+----------------------------------+
| Experiment       | Target Volume / Mass  | Detection Technology             |
+------------------+-----------------------+----------------------------------+
| Super-Kamiokande | 50 kt (Water)         | Water Cherenkov (11,146 PMTs)    |
| Hyper-Kamiokande | 260 kt (Water)        | Next-gen Water Cherenkov         |
| JUNO             | 20 kt (Scintillator)  | Liquid Scintillator              |
| DUNE             | 40 kt (Liquid Argon)  | Liquid Argon TPC (LArTPC)        |
+------------------+-----------------------+----------------------------------+
```

---

## 4. History of Discovery: The Three Active Flavours

```
                     HISTORICAL DISCOVERY TIMELINE
=================================================================================
1930 Pauli proposes "neutrino" to preserve energy conservation in β-decay
1956 Cowan & Reines discover ν_e (Reactor Inverse Beta Decay) [1]
1962 Lederman, Schwartz, & Steinberger discover ν_μ (AGS Accelerator Beam) [2]
1989 LEP Z⁰ width measurements prove N_ν = 2.984 ± 0.008 [3]
2000 DONUT Collaboration directly observes ν_τ (Fermilab Tevatron) [4]
=================================================================================
```

### 1. Proposal and Discovery of Electron Neutrino ($\nu_e$)
* **Problem (1930):** Beta decay ($\text{Nucleus}_A \rightarrow \text{Nucleus}_B + e^-$) produced a continuous electron energy spectrum instead of a discrete peak, seemingly violating energy/momentum conservation.
* **Pauli's Hypothesis:** Proposed a neutral, light spin-$1/2$ particle emitted alongside the electron.
* **Discovery (1956):** Cowan and Reines detected $\bar{\nu}_e$ at the Savannah River reactor using Inverse Beta Decay (IBD):
  $$\bar{\nu}_e + p \rightarrow e^+ + n$$
  * *Signature:* Prompt $e^+e^-$ annihilation ($2 \times 511 \text{ keV} \, \gamma$-rays) followed $\sim 5 \, \mu\text{s}$ later by a delayed $\gamma$-ray cascade from neutron capture on Cadmium.

```
       COWAN-REINES INVERSE BETA DECAY SIGNAL PATTERN
       
  ν̄_e + p  --->  e⁺  +  n
                 │      │
                 │      └---> (Capture on Cd) ---> Delayed γ-ray cascade (~5 μs)
                 └---> (Annihilation with e⁻) ---> Prompt 2 x 511 keV γ-rays
```

### 2. Proposal and Discovery of Muon Neutrino ($\nu_\mu$)
* **Puzzle:** The decay $\mu \rightarrow e + \gamma$ was never observed, suggesting $\nu_\mu \neq \nu_e$.
* **Discovery (1962):** Lederman, Schwartz, and Steinberger used the Brookhaven AGS accelerator [2]:
  1. $15 \text{ GeV}$ protons struck a Be target to produce $\pi^\pm$.
  2. Pions decayed in flight: $\pi^+ \rightarrow \mu^+ + \nu_\mu$.
  3. A $13.5 \text{ m}$ steel shield stopped all charged particles ($\mu, \pi$).
  4. The purified neutrino beam hit a 10-ton spark chamber, producing **only muons** ($\nu_\mu + n \rightarrow \mu^- + p$) and **zero electrons**, proving $\nu_\mu$ is a distinct flavour.

### 3. Proposal and Discovery of Tau Neutrino ($\nu_\tau$)
* **Prediction (1975):** Followed Martin Perl's discovery of the $\tau$ lepton at SLAC.
* **Challenge:** Tau neutrinos cannot be produced in pion decay due to mass thresholds; they require decay of heavy charmed mesons ($D_s \rightarrow \tau + \nu_\tau$), demanding $800 \text{ GeV}$ protons.
* **Discovery (2000):** The **DONUT** collaboration at Fermilab observed $\nu_\tau + N \rightarrow \tau^- + X$ using high-resolution nuclear emulsion plates to resolve the characteristic "kinked" decay track of the short-lived $\tau$ lepton ($\tau \sim 1 \text{ mm}$) [4].

---

## 5. Constraint on Active Neutrino Flavours: LEP $Z^0$ Width Limit

At CERN's Large Electron-Positron Collider (LEP), the combined ALEPH, DELPHI, L3, and OPAL collaborations measured the $Z^0$ resonance curve at $\sqrt{s} \approx 91.2 \text{ GeV}$ [3].

```
                 LEP Z⁰ RESONANCE FIT FOR FLAVOUR NUMBER
  
  σ_hadronic (nb)
    ^
 35 |           / \           --- 2 Light Neutrino Flavours
    |          /   \          ─── 3 Light Neutrino Flavours (EXACT MATCH)
 30 |........./.....\........ --- 4 Light Neutrino Flavours
    |        /   │   \
 20 |       /    │    \
    +------+-----+-----+-------------------> E_cm (GeV)
          88    91.2   94
```

The total decay width $\Gamma_Z$ is given by:
$$\Gamma_Z = \Gamma_{\text{hadronic}} + 3\Gamma_{\text{charged leptons}} + N_\nu \Gamma_{\nu\bar{\nu}}$$

Measuring the hadronic peak cross-section $\sigma_{\text{hadronic}}^0 = \frac{12\pi}{M_Z^2} \frac{\Gamma_{ee} \Gamma_{\text{hadronic}}}{\Gamma_Z^2}$ yielded:
$$N_\nu = 2.984 \pm 0.008$$

This explicitly proved that **there are exactly three light active neutrino flavours** ($m_\nu < M_Z / 2$) in nature.

---

## 6. Physics of Neutrino Oscillations

### Flavour Identification vs. Mass Eigenstates
In detectors, we identify neutrino **flavour eigenstates** ($\vert{}\nu_e\rangle, \vert{}\nu_\mu\rangle, \vert{}\nu_\tau\rangle$) by the charged lepton produced at the weak interaction vertex ($W^\pm$ emission/absorption):
* $\bar{\nu}_e + p \rightarrow e^+ + n$
* $\nu_\mu + n \rightarrow \mu^- + p$
* $\bar{\nu}_\tau + p \rightarrow \tau^+ + n$

```
          WEAK CHARGED-CURRENT INTERACTION VERTICES
          
      ν̄_e ──>──/\──>── e⁺         ν_μ ──>──/\──>── μ⁻         ν̄_τ ──>──/\──>── τ⁺
               │                           │                           │
               ~~~~ W⁻                     ~~~~ W⁺                     ~~~~ W⁻
               │                           │                           │
        p ──>──\/──>── n            n ──>──\/──>── p            p ──>──\/──>── n
```

However, **flavour eigenstates are not mass eigenstates**. Neutrinos are produced and detected in flavour eigenstates, but propagate through space as **mass eigenstates** ($\vert{}\nu_1\rangle, \vert{}\nu_2\rangle, \vert{}\nu_3\rangle$).

### The PMNS Matrix Connection
The unitary **Pontecorvo-Maki-Nakagawa-Sakata (PMNS)** matrix $U$ rotates between bases [5,6]:
$$\vert{}\nu_\alpha\rangle = \sum_{k=1}^3 U_{\alpha k}^* \vert{}\nu_k\rangle \quad \Longleftrightarrow \quad \vert{}\nu_k\rangle = \sum_{\alpha} U_{\alpha k} \vert{}\nu_\alpha\rangle$$

```
                         3D FLAVOUR MATRIX ROTATION
                                   v_3
                                    ▲   v_μ
                                    │  /
                                 θ₁₃│ / θ₂₃
                         v_τ        │/
                           \        /──── v_2
                            \θ₂₃   /   /
                             \    /   / θ₁₂
                              \  /   /
                               \/___/________ v_1
                                 θ₁₂  v_e
```

The standard parameterisation using three mixing angles ($\theta_{12}, \theta_{23}, \theta_{13}$) and one Dirac CP phase $\delta_{CP}$ is:
$$U = \begin{pmatrix} 1 & 0 & 0 \\ 0 & c_{23} & s_{23} \\ 0 & -s_{23} & c_{23} \end{pmatrix} \begin{pmatrix} c_{13} & 0 & s_{13}e^{-i\delta_{CP}} \\ 0 & 1 & 0 \\ -s_{13}e^{i\delta_{CP}} & 0 & c_{13} \end{pmatrix} \begin{pmatrix} c_{12} & s_{12} & 0 \\ -s_{12} & c_{12} & 0 \\ 0 & 0 & 1 \end{pmatrix}$$
*(where $c_{ij} = \cos\theta_{ij}$ and $s_{ij} = \sin\theta_{ij}$)*

#### Non-Trivial Mass Superposition
Because mixing angles are large ($\theta_{12} \approx 33.7^\circ, \theta_{23} \approx 49.1^\circ, \theta_{13} \approx 8.5^\circ$), individual flavour states are spread significantly across mass states. For instance, the muon neutrino state $\vert{}\nu_\mu\rangle = U_{\mu 1}^* \vert{}\nu_1\rangle + U_{\mu 2}^* \vert{}\nu_2\rangle + U_{\mu 3}^* \vert{}\nu_3\rangle$ has fractional contents:
$$0.236 < \vert{}U_{\mu 1}^*\vert{} < 0.507, \quad 0.458 < \vert{}U_{\mu 2}^*\vert{} < 0.691, \quad 0.630 < \vert{}U_{\mu 3}^*\vert{} < 0.779$$
Thus, there is no single "mass of a muon neutrino."

---

## 7. Quantum Mechanical Propagation and Probability Derivation

### Wavefunction Evolution in Space
Each mass eigenstate $\vert{}\nu_k\rangle$ evolves as a plane wave:
$$\vert{}\nu_k(x)\rangle = e^{-i \frac{m_k^2 x}{2E}} \vert{}\nu_k(0)\rangle$$

Because $m_1 \neq m_2 \neq m_3$, the phase velocity of each mass component differs. As the neutrino travels distance $L$, a phase shift accumulates between mass components, causing the superposition—and thus the observed flavour composition—to change.

```
                  MASS EIGENSTATE PHASE EVOLUTION
  
   Position x_0 (Source)          Position x_1                   Position x_2
   Pure |ν_e⟩                     Mix of |ν_e⟩ + |ν_μ⟩          Reconstituted |ν_e⟩
   
    Phase Wave |ν₁⟩ ────\           /\    /\    /\                /\    /\    /\
    Phase Wave |ν₂⟩ ─────>======== /  \  /  \  /  \  ============ /  \  /  \  /  \
    Phase Wave |ν₃⟩ ────/          \__/  \__/  \__/               \__/  \__/  \__/
                                   (Out of phase)                 (In phase)
```

### General Oscillation Probability Formula
The probability of a neutrino produced with flavour $\alpha$ being detected with flavour $\beta$ after baseline distance $L$ and energy $E$ is:
$$P_{\alpha \rightarrow \beta}(L/E) = \sum_{k,j=1}^3 U_{\alpha k}^* U_{\beta k} U_{\alpha j} U_{\beta j}^* \exp\left( -i \frac{\Delta m_{kj}^2 L}{2E} \right)$$
where $\Delta m_{kj}^2 \equiv m_k^2 - m_j^2$.

---

## 8. Experimental Measurement Regimes and $L/E$ Optimization

To measure specific parameters ($\Delta m_{ij}^2, \theta_{ij}$), an experiment must match its baseline distance $L$ and energy $E$ to the scale of the mass splitting:
$$\left| \Delta m^2 \right| \sim \frac{E}{L}$$

```
========================================================================================
EXPERIMENT TYPE        SOURCES          L / E RANGE           SENSITIVE PARAMETERS
========================================================================================
Short-Baseline (SBN)   Accelerator/Src  L/E ~ 1 km/GeV        Searches for Δm² ~ 1 eV²
Long-Baseline (LBL)    Accelerator Beam L/E ~ 10³ km/GeV     θ₂₃, θ₁₃, Δm₃₁², δ_CP (DUNE/T2K)
Reactor & Solar        Reactors / Sun   L/E ~ 10⁴ - 10⁶ km/GeV θ₁₂, Δm₂₁² (JUNO/KamLAND)
========================================================================================
```

### Probability Curves by Channel
Depending on initial flavour, probabilities show distinctive oscillation frequencies over $L/E$:

```
                       OSCILLATION PROBABILITY VS. L/E
  
  P(ν_e -> ν_α)                                    P(ν_μ -> ν_α)
  1.0| \  ν_e -> ν_e                               1.0| \  ν_μ -> ν_μ
     |  \     /\     /                                |  \     /\     /
  0.5|---\---/--\---/----                          0.5|---\---/--\---/----
     |    \_/    \_/  ν_e -> ν_μ, ν_τ                 |    \_/    \_/  ν_μ -> ν_e, ν_τ
  0.0+------------------------> L/E                0.0+------------------------> L/E
     0      10³      10⁶ (km/GeV)                     0      10³      10⁶ (km/GeV)
```

---

## 9. Experimental Setups: Near/Far Detectors vs. Flux Modeling

### 1. Two-Detector Setup (Accelerator Beams)
For artificial beams (e.g., DUNE, T2K, MINOS), experiments utilize a **Near Detector** and a **Far Detector**:
* **Near Detector:** Positioned near the beam target ($L \sim \text{hundreds of meters}$) before oscillations occur. Measures initial flux, flavour composition, and interaction cross-sections.
* **Far Detector:** Positioned hundreds of kilometers away ($L \sim 300\text{--}1300 \text{ km}$) at peak oscillation distance to measure flavour disappearance/appearance.

```
       TWO-DETECTOR LONG-BASELINE EXPERIMENTAL DESIGN
       
   Target / Beam      Near Detector                        Far Detector
   ┌──────────┐       ┌───────────┐                        ┌───────────┐
   │ p⁺ -> π  │======>│ Measure   │=======================>│ Measure   │
   │  -> ν_μ  │       │ Unoscillated                       │ Oscillated│
   └──────────┘       │ Flux      │                        │ Spectrum  │
   x = 0              └───────────┘                        └───────────┘
                      x ~ 500 m                            x ~ 300-1300 km
```

### 2. Natural Source Setup (Solar & Atmospheric)
For natural sources (the Sun, atmospheric showers), placing a near detector at the source is impossible. Experiments rely on:
1. High-precision theoretical models of source flux (e.g., Bahcall's Standard Solar Model).
2. Known source-to-detector baseline geometry ($L$).

---

## 10. Summary of Key Knowledge Confirmed by 20th Century Physics

By the end of the 20th century, neutrino experiments confirmed four fundamental pillars:
1. **Three Flavour Eigenstates:** $\nu_e, \nu_\mu, \nu_\tau$.
2. **Neutrino Oscillations:** Neutrinos dynamically switch flavour in transit.
3. **Non-Zero Neutrino Mass:** Oscillations require $\Delta m_{ij}^2 \neq 0$, proving at least two neutrino mass states are non-zero.
4. **Chiral Suppression:** Right-handed neutrinos (and left-handed antineutrinos) do not participate in Standard Model weak interactions.

---

## 11. Open Questions at the End of the 20th Century

```
                        OPEN QUESTIONS IN NEUTRINO PHYSICS
  
      Mass Mechanism             Mass Ordering                 CP Violation
  ┌────────────────────┐     ┌────────────────────┐     ┌────────────────────┐
  │ Dirac or Majorana? │     │  Normal vs.        │     │ Is δ_CP ≠ 0?      │
  │ (Seesaw Model?)    │     │  Inverted Hierarchy│     │ (Leptogenesis?)    │
  └────────────────────┘     └────────────────────┘     └────────────────────┘
```

1. **Mass Generation Mechanism:** Are neutrinos **Dirac** particles (mass from Higgs coupling) or **Majorana** particles (particles are their own antiparticles)? Does the *Seesaw Mechanism* explain why neutrino masses are so extraordinarily light ($\sim 10^6$ times lighter than electrons)?
2. **Neutrino Mass Ordering (Hierarchy):** Is the hierarchy **Normal** ($m_1 < m_2 < m_3$, $\Delta m_{31}^2 > 0$) or **Inverted** ($m_3 < m_1 < m_2$, $\Delta m_{31}^2 < 0$)?
3. **Leptonic CP Violation:** Is the Dirac phase $\delta_{CP} \neq 0$? Can CP violation in the lepton sector explain the matter-antimatter asymmetry of the universe via **leptogenesis**?
4. **Flavour Count:** Are there additional non-interacting **sterile neutrinos** ($\nu_s$) suggested by short-baseline anomalies (LSND/MiniBooNE)?

---

## References

\[1\] Cowan, C. L., Reines, F., et al. (1956). "Detection of the Free Neutrino: a Confirmation". *Science*, 124(3212), 103–104.  
\[2\] Danby, G., et al. (1962). "Observation of High-Energy Neutrino Reactions and the Existence of Two Kinds of Neutrinos". *Physical Review Letters*, 9(1), 36.  
\[3\] ALEPH, DELPHI, L3, OPAL Collaborations, LEP Electroweak Working Group (2006). "Precision electroweak measurements on the $Z$ resonance". *Physics Reports*, 427(5–6), 257–454.  
\[4\] Kodama, K., et al. (DONUT Collaboration) (2001). "Observation of tau neutrino interactions". *Physics Letters B*, 504(3), 218–224.  
\[5\] Pontecorvo, B. (1957). "Inverse Beta Processes and Non-conservation of Lepton Charge". *JETP*, 7, 172.  
\[6\] Maki, Z., Nakagawa, M., & Sakata, S. (1962). "Remarks on the Unified Model of Elementary Particles". *Progress of Theoretical Physics*, 28(5), 870–880.  