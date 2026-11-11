# Fundamental Neutrino Physics and Introduction

*Based on MPS 137: Frontiers of Physics – Part 1 (University of Sheffield)*

## 1. The Standard Model and Where Neutrinos Fit In

The **Standard Model (SM) of Particle Physics** is the theoretical framework describing all known fundamental matter and three of the four fundamental forces: electromagnetism, the weak interaction, and the strong interaction (excluding gravity).

<table style="text-align: center; margin-left: auto; margin-right: auto;">
  <thead>
    <tr>
      <th colspan="5" style="text-align: center;">Fermions (Spin 1/2)</th>
    </tr>
    <tr>
      <th style="text-align: center;"></th>
      <th colspan="2" style="text-align: center;">Quarks</th>
      <th colspan="2" style="text-align: center;">Leptons</th>
    </tr>
    <tr>
      <th style="text-align: center;"></th>
      <th colspan="2" style="text-align: center;">(Feel Weak, EM, &amp; Strong Force)</th>
      <th colspan="2" style="text-align: center;">(Do NOT feel Strong Force)</th>
    </tr>
    <tr>
      <th style="text-align: center;"></th>
      <th style="text-align: center;"></th>
      <th style="text-align: center;"></th>
      <th style="text-align: center;">Charged Leptons (-1e)</th>
      <th style="text-align: center;">Neutrinos (0 Charge)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center;">Gen 1</td>
      <td style="text-align: center;">u (Up) </td>
      <td style="text-align: center;">d (Down)</td>
      <td style="text-align: center;">$e^{-}$ (Electron, 0.511 MeV)</td>
      <td style="text-align: center;">$\nu_{e}$ (Electron Neutrino)</td>
    </tr>
    <tr>
      <td style="text-align: center;">Gen 2</td>
      <td style="text-align: center;">c (Charm)</td>
      <td style="text-align: center;">s (Strange)</td>
      <td style="text-align: center;">$\mu^{-}$ (Muon, 105.7 MeV)</td>
      <td style="text-align: center;">$\nu_{\mu}$ (Muon Neutrino)</td>
    </tr>
    <tr>
      <td style="text-align: center;">Gen 3</td>
      <td style="text-align: center;">t (Top)</td>
      <td style="text-align: center;">b (Bottom)</td>
      <td style="text-align: center;">$\tau^{-}$ (Tau, 1776.8 MeV)</td>
      <td style="text-align: center;">$\nu_{\tau}$ (Tau Neutrino)</td>
    </tr>
    <tr>
      <td colspan="5" style="text-align: center;">Bosons (Spin 0,1)</td>
    </tr>
    <tr>
      <td style="text-align: center;"></td>
      <td colspan="2" style="text-align: center;">Vector Bosons (Spin 1)</td>
      <td colspan="2" style="text-align: center;">Scalar Boson (Spin 0)</td>
    </tr>
    <tr>
      <td style="text-align: center;"></td>
      <td colspan="2" style="text-align: center;">Gluon (g, Strong), Photon (&gamma;, EM), $W^{+};$W^{-}$;$Z^{0}$; (Weak Force)</td>
      <td colspan="2" style="text-align: center;">Higgs Boson (H, Mass generation)</td>
    </tr>
  </tbody>
</table>

### Lepton Family & Neutrino Properties

Neutrinos ($\nu_e, \nu_\mu, \nu_\tau$) are neutral leptons ($Q=0, C=0$) with spin $1/2$. Because they carry no electric or color charge:

* They **do not feel the strong force** or electromagnetism.
* They interact **strictly via the weak nuclear force** (mediated by $W^\pm$ and $Z^0$ gauge bosons) and gravity.
* In the classical (massless) Standard Model, neutrinos were assumed to be strictly left-handed ($\nu_L$) and antineutrinos right-handed ($\bar{\nu}_R$).

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

   $$
   \pi^\pm \rightarrow \mu^\pm + \nu_\mu (\bar{\nu}_\mu), \quad \mu^\pm \rightarrow e^\pm + \nu_e (\bar{\nu}_e) + \bar{\nu}_\mu (\nu_\mu)
   $$

5. **Nuclear Reactors:** Beta decay of neutron-rich fission fragments emits intense isotropic fluxes of $\bar{\nu}_e$.
6. **Accelerators:** High-energy proton beams target stationary nuclei (e.g., beryllium or carbon) to generate focused pion/kaon decay channels.
7. **Terrestrial & Biological:** Beta decay of ${}^{40}\text{K}$ in everyday objects (e.g., bananas emit $\sim 5,000 \text{ antineutrinos/second}$).

## 3. Neutrino Energies, Cross-Sections, and Experimental Design Implications

### Energy Spectrum vs. Cross-Section

Neutrinos cover over 18 orders of magnitude in energy. The neutrino-nucleon cross-section $\sigma$ scales directly with energy:

* **Low Energy (**$E_\nu \sim 1 \text{ MeV}$**):** Quasi-elastic / Inverse Beta Decay ($\sigma \sim 10^{-44} \text{ cm}^2$).
* **High Energy (**$E_\nu > 10 \text{ GeV}$**):** Deep Inelastic Scattering ($\sigma \propto G_F^2 E_\nu$).

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

$$
\text{Mean Free Path } \lambda = \frac{1}{n \cdot \sigma} \approx 6 \times 10^{12} \text{ miles } (\sim 1 \text{ light-year of solid lead})
$$

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
* **Discovery (1956):** Cowan and Reines detected $\bar{\nu}_e$ at the Savannah River reactor using Inverse Beta Decay (IBD) \[1\]:

  $$
  \bar{\nu}_e + p \rightarrow e^+ + n
  $$

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
* **Discovery (1962):** Lederman, Schwartz, and Steinberger used the Brookhaven AGS accelerator \[2\]:

  1. $15 \text{ GeV}$ protons struck a Be target to produce $\pi^\pm$.
  2. Pions decayed in flight: $\pi^+ \rightarrow \mu^+ + \nu_\mu$.
  3. A $13.5 \text{ m}$ steel shield stopped all charged particles ($\mu, \pi$).
  4. The purified neutrino beam hit a 10-ton spark chamber, producing **only muons** ($\nu_\mu + n \rightarrow \mu^- + p$) and **zero electrons**, proving $\nu_\mu$ is a distinct flavour.

### 3. Proposal and Discovery of Tau Neutrino ($\nu_\tau$)

* **Prediction (1975):** Followed Martin Perl's discovery of the $\tau$ lepton at SLAC.
* **Challenge:** Tau neutrinos cannot be produced in pion decay due to mass thresholds; they require decay of heavy charmed mesons ($D_s \rightarrow \tau + \nu_\tau$), demanding $800 \text{ GeV}$ protons.
* **Discovery (2000):** The **DONUT** collaboration at Fermilab observed $\nu_\tau + N \rightarrow \tau^- + X$ using high-resolution nuclear emulsion plates to resolve the characteristic "kinked" decay track of the short-lived $\tau$ lepton ($\tau \sim 1 \text{ mm}$) \[4\].

## 5. Constraint on Active Neutrino Flavours: LEP $Z^0$ Width Limit

At CERN's Large Electron-Positron Collider (LEP), the combined ALEPH, DELPHI, L3, and OPAL collaborations measured the $Z^0$ resonance curve at $\sqrt{s} \approx 91.2 \text{ GeV}$ \[3\].

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

$$
\Gamma_Z = \Gamma_{\text{hadronic}} + 3\Gamma_{\text{charged leptons}} + N_\nu \Gamma_{\nu\bar{\nu}}
$$

Measuring the hadronic peak cross-section $\sigma_{\text{hadronic}}^0 = \frac{12\pi}{M_Z^2} \frac{\Gamma_{ee} \Gamma_{\text{hadronic}}}{\Gamma_Z^2}$ yielded:

$$
N_\nu = 2.984 \pm 0.008
$$

This explicitly proved that **there are exactly three light active neutrino flavours** ($m_\nu < M_Z / 2$) in nature.

## References

\[1\] Cowan, C. L., Reines, F., et al. (1956). "Detection of the Free Neutrino: a Confirmation". *Science*, 124(3212), 103–104.

\[2\] Danby, G., et al. (1962). "Observation of High-Energy Neutrino Reactions and the Existence of Two Kinds of Neutrinos". *Physical Review Letters*, 9(1), 36.

\[3\] ALEPH, DELPHI, L3, OPAL Collaborations, LEP Electroweak Working Group (2006). "Precision electroweak measurements on the $Z$ resonance". *Physics Reports*, 427(5–6), 257–454.

\[4\] Kodama, K., et al. (DONUT Collaboration) (2001). "Observation of tau neutrino interactions". *Physics Letters B*, 504(3), 218–224.