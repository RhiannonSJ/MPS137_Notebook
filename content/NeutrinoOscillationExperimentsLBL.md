# Long Baseline Neutrino Oscillation Experiments 

## 1. Classification of Neutrino Oscillation Experiments

Neutrino oscillation experiments measure how the quantum state of a neutrino changes as it travels over a distance $L$. Experiments fall into two fundamental operational classes[^1]:

1. **Disappearance Experiments:** The experiment measures a reduction in the flux of the initial, original neutrino flavour ($\nu_\alpha \rightarrow \text{anything else}$).
2. **Appearance Experiments:** The experiment measures the emergence of a neutrino flavour different from the initial state ($\nu_\alpha \rightarrow \nu_\beta$ where $\alpha \neq \beta$).

### Energy Threshold Constraints
For low-energy electron (anti)neutrinos ($E_\nu < m_\mu c^2 \approx 105.7\text{ MeV}$), such as those produced by the Sun or nuclear reactors, **only disappearance experiments are kinematically possible**[^1]. The incoming neutrino does not possess enough energy to produce a muon ($m_\mu$) or tau ($m_\tau$) lepton via Charged-Current (CC) interactions. For higher-energy neutrinos, combined appearance and disappearance measurements are used to disentangle oscillation mixing angles such as $\theta_{13}$ and $\theta_{23}$[^1].

---

## 2. Neutrino Sources, Production Mechanisms, and Detection

Neutrino experiments rely on different natural and artificial production mechanisms, each yielding distinct energy spectra and sensitivity to different PMNS matrix parameters ($\theta_{12}, \theta_{23}, \theta_{13}$, and $\delta_{\text{CP}}$)[^2][^3].

| Source Type | Production Mechanism | Key Interaction / Flavour | Main Parameter Sensitivity | Example Experiments |
| :--- | :--- | :--- | :--- | :--- |
| **Reactor** | $\beta^-$ decay in nuclear reactors | Pure $\bar{\nu}_e$ | $\theta_{13}, \theta_{12}$ (depends on $L$) | KamLAND, Daya Bay, RENO, Double Chooz[^2] |
| **Solar** | Proton-proton chain & CNO cycle in the Sun ($pp$, $pep$, $hep$, $^{7}\text{Be}$, $^{8}\text{B}$) | Pure $\nu_e$ | $\theta_{12}, \theta_{13}$ | SAGE, GALLEX, Borexino, SNO[^2] |
| **Atmospheric** | Cosmic-ray protons hitting Earth's atmosphere $\rightarrow$ hadron shower ($\pi^\pm, K^\pm$) | Combined $\nu_e, \bar{\nu}_e, \nu_\mu, \bar{\nu}_mu$ (Expected $\nu_e:\nu_\mu \approx 1:2$) | $\theta_{23}, \theta_{13}, \delta_{\text{CP}}$ | Super-Kamiokande, IceCube[^3] |
| **Accelerator** | High-intensity $p^+$ beam hit on target $\rightarrow$ focused $\pi^\pm/K^\pm$ decay in flight | Highly pure $\nu_\mu$ or $\bar{\nu}_\mu$ beam | $\theta_{23}, \theta_{13}, \delta_{\text{CP}}$ | T2K, Super-K, Hyper-K, NO$\nu$A, MINOS(+), DUNE, SBN[^3] |

### Production Details by Flavour
* **$\nu_\mu$ Beams:** Protons are accelerated and fired at a dense target (e.g., graphite), producing charged pions ($\pi^\pm$). Magnetic "horns" focus either positive or negative pions into a parallel beam. The pions decay in flight (e.g., $\pi^+ \rightarrow \mu^+ + \nu_\mu$), producing an almost pure $\nu_\mu$ or $\bar{\nu}_\mu$ beam[^3][^4]. The decay of secondary muons ($\mu^\pm \rightarrow e^\pm + \nu_e/{\bar{\nu}_e} + \bar{\nu}_\mu/{\nu}_\mu$) introduces a small intrinsic $\nu_e$ background[^4].
* **$\nu_e$:** Readily available from natural sources (Sun) and nuclear reactors ($\bar{\nu}_e$)[^5].
* **$\nu_\tau$:** Tau neutrinos cannot be produced via pion decay due to the high mass of the $\tau$ lepton. Instead, they require the decay of charmed mesons, requiring primary proton beams with energies $\sim 100\times$ higher than those needed for muon neutrinos[^6]. $\nu_\tau$ are detected via CC interactions ($ \nu_\tau + N \rightarrow \tau^- + X $), requiring high neutrino energy ($E_\nu > m_\tau c^2$) and ultra-high resolution detectors (such as DONUT) capable of resolving the sub-millimetre "kinked" track of the short-lived $\tau$ lepton[^7].

---

## 3. Detector Technologies and Event Signatures

To distinguish between neutrino flavours, detectors identify the charged lepton produced in Charged-Current (CC) interactions ($\nu_\ell + N \rightarrow \ell^- + X$)[^5][^8].

```
Water Cherenkov                         Liquid Argon TPC (LArTPC)
----------------                        ------------------------
Muon: Sharp, clear ring                 Muon: Long, straight, clean track
Electron: Fuzzy, diffuse ring           Electron: Electromagnetic shower (cascading branching)
```

1. **Water Cherenkov Detectors (e.g., Super-Kamiokande):**
   * **Muon ($\nu_\mu$ signature):** A heavy muon travels at relativistic speeds through water without scattering much, producing a **sharp, well-defined Cherenkov light ring**[^8].
   * **Electron ($\nu_e$ signature):** A light electron undergoes multiple Coulomb scattering and pair-production/bremsstrahlung, creating an electromagnetic shower. This results in a **fuzzy, diffuse-edged ring**[^8].
2. **Liquid Argon Time Projection Chambers (LArTPCs) (e.g., DUNE, SBN):**
   * **Muon ($\nu_\mu$ signature):** Displays a single, long, sharp continuous ionizing track[^8].
   * **Electron ($\nu_e$ signature):** Displays an initial single track that rapidly branches into an electromagnetic shower pattern[^8].

---

## 4. Case Study 1: The T2K Experiment

The **T2K (Tokai to Kamioka)** experiment in Japan is a second-generation long-baseline neutrino oscillation experiment[^9].

### Core Parameters & Setup
* **Baseline ($L$):** $295\text{ km}$ from J-PARC (Tokai) to Super-Kamiokande (Kamioka)[^9].
* **Off-Axis Technique:** The beam is directed $2.5^\circ$ off-axis relative to the far detector. This off-axis geometry narrows the energy spectrum of the neutrino beam, peaking precisely at $\sim 0.6\text{ GeV}$, which matches the oscillation maximum for $L = 295\text{ km}$ while suppressing high-energy backgrounds[^9][^10].
* **Primary Physics Goals:** Precise measurement of $\theta_{13}$ (first established via $\nu_e$ appearance), refining $\theta_{23}$, and probing the CP-violating phase $\delta_{\text{CP}}$[^9].

### Beam Production and Magnet System
1. 30 GeV protons from the J-PARC Main Ring hit a graphite rod target, generating charged pions ($\pi^\pm$)[^11].
2. Three magnetic horns focus $\pi^+$ (for neutrino mode) or $\pi^-$ (for antineutrino mode) into a $110\text{ m}$ decay volume where they decay to $\mu^+ + \nu_\mu$ or $\mu^- + \bar{\nu}_\mu$[^11].

### Detector Suite
* **INGRID (Interactive Neutrino GRID):** On-axis near detector ($280\text{ m}$ from target). Its cross-shaped structure of alternating iron/lead absorbers and plastic scintillators monitors beam center symmetry and flux daily via $\nu_\mu$ interactions[^10][^12][^13].
* **ND280:** Off-axis near detector ($280\text{ m}$ from target)[^10][^14]. Placed inside a $0.2\text{ T}$ recycled UA1 magnet, it uses Time Projection Chambers (TPCs), Fine-Grain Detectors (FGDs), Electromagnetic Calorimeters (ECALs), and recently a Super Fine-Grain Detector (SFGD)[^14][^15].
  * *Role:* Measures intrinsic $\nu_e$ background and characterizes neutral-current $\pi^0$ production cross-sections (since a single photon from $\pi^0 \rightarrow \gamma\gamma$ can fake a $\nu_e$ electron ring in Super-K)[^14].
* **Super-Kamiokande (Far Detector):** A $50\text{ kton}$ water Cherenkov detector situated under Mt. Ikeno-Yama ($1000\text{ m}$ rock cover / $2700\text{ m}$ water equivalent)[^9][^16].
  * *Inner Detector (ID):* Instrumented with $\sim 11,000$ inward-facing $50\text{ cm}$ Photomultiplier Tubes (PMTs)[^16].
  * *Outer Detector (OD):* Instrumented with $\sim 2,000$ outward-facing $20\text{ cm}$ PMTs serving as an active veto for cosmic rays[^16].
  * *Water Quality:* Highly purified through RO, UV, and ultra-filtration systems to minimize light absorption and radioactive backgrounds (e.g., Radon)[^19].

### Oscillation Results in T2K
* **$\nu_\mu / \bar{\nu}_\mu$ Disappearance:** A sharp drop in muon events around $E_\nu \sim 0.6\text{ GeV}$ constrains $\theta_{23}$ and $|\Delta m^2_{32}|$[18].
* **$\nu_e / \bar{\nu}_e$ Appearance:** Direct observation of $e$-like Cherenkov rings in a predominantly $\nu_\mu$ beam provided primary evidence for non-zero $\theta_{13}$ and initial constraints on $\delta_{\text{CP}}$[18].

---

## 5. Next-Generation Experiment: Hyper-Kamiokande

**Hyper-Kamiokande (Hyper-K)** is the flagship successor to T2K, featuring an upgraded beam intensity and a massive new far detector[^21].

### Key Upgrades
* **Far Detector Target Mass:** A giant cylindrical water Cherenkov tank containing **$258\text{ kton}$** of ultrapure water ($\sim 5\times$ larger target volume than Super-K)[^21][^23].
* **Photosensors:** High-efficiency PMTs with doubled quantum efficiency and better timing resolution compared to SK[^23].
* **Intermediate Detector ($\nu\text{PRISM}$):** Placed at $1\text{--}2\text{ km}$ from the target. The detector moves vertically inside a deep shaft, scanning across different off-axis angles ($1.0^\circ$ to $4.0^\circ$)[^22][^24][^25].
  * *Purpose:* By taking data at varying off-axis angles, $\nu\text{PRISM}$ can construct a customized, energy-dependent neutrino flux matching the oscillated spectrum at Hyper-K, dramatically reducing systematic errors on cross-sections[^24][^25].

---

## 6. Next-Generation Experiment: DUNE

The **Deep Underground Neutrino Experiment (DUNE)** is an international long-baseline experiment based in the United States[^27][^29].

### Experimental Architecture
* **Baseline ($L$):** $1300\text{ km}$ (800 miles), sending neutrinos through the Earth from Fermilab (Illinois) to the Sanford Underground Research Facility (SURF, South Dakota)[^27][^28].
* **Beam:** An on-axis, **broad-band** high-energy beam produced by the PIP-II proton accelerator at Fermilab[^27][^30]. The beam spectrum can be adjusted (e.g., Low Energy "LE" tune) to optimize sensitivity to $\delta_{\text{CP}}$[^30].
* **Far Detector:** Underground liquid argon TPCs (LArTPCs) modular system consisting of four $17\text{ kton}$ modules (both horizontal-drift and vertical-drift designs)[^28][^32].

### Scientific Capabilities & Complementarity with Hyper-K
1. **Matter Effects and Mass Hierarchy:** Because DUNE has a long baseline ($1300\text{ km}$) through Earth's mantle, electron neutrinos experience coherent forward scattering with electrons in terrestrial matter[^34]. This modifies the oscillation probability in a way sensitive to the sign of $\Delta m^2_{31}$, allowing DUNE to definitively resolve the **neutrino mass ordering** (Normal: $m_3 > m_2 > m_1$ vs. Inverted: $m_2 > m_1 > m_3$)[^34][^35].
2. **CP Violation Phase ($\delta_{\text{CP}}$):** Broad-band beam energy coverage allows DUNE to measure multiple oscillation nodes, disentangling CP violation effects from matter effects[^30][^35].
3. **Non-Accelerator Physics:** Search for proton decay, detection of atmospheric neutrinos, and sensitivity to galactic supernova neutrinos (DUNE is sensitive primarily to $\nu_e + ^{40}\text{Ar} \rightarrow e^- + ^{40}\text{K}^*$, whereas Hyper-K is sensitive to $\bar{\nu}_e + p \rightarrow e^+ + n$ via inverse beta decay)[^26][^28][^29].

---

## Comparison Summary: Hyper-K vs. DUNE

| Parameter / Feature | Hyper-Kamiokande (HK) | Deep Underground Neutrino Experiment (DUNE) |
| :--- | :--- | :--- |
| **Location** | Japan (J-PARC $\rightarrow$ Tochibora) | USA (Fermilab $\rightarrow$ SURF) |
| **Baseline ($L$)** | $295\text{ km}$ | $1300\text{ km}$ |
| **Beam Configuration** | Off-axis ($2.5^\circ$), Narrow-band | On-axis, Broad-band |
| **Far Detector Technology** | Water Cherenkov ($258\text{ kton}$) | Liquid Argon TPC ($4 \times 17\text{ kton}$) |
| **Supernova Sensitivity** | Primary sensitivity to $\bar{\nu}_e$ (IBD) | Primary sensitivity to $\nu_e$ ($\text{Ar}$-CC) |
| **Matter Effects** | Modest | Dominant (determines mass hierarchy cleanly) |

---

## References & Slide Citations

[^1]: MPS 137 Part 2 Slides, Slide 4: *Oscillation experimental choices*.  
[^2]: MPS 137 Part 2 Slides, Slide 2: *Neutrino oscillation experiments (Reactor & Solar)*.  
[^3]: MPS 137 Part 2 Slides, Slide 3: *Neutrino oscillation experiments (Accelerator & Atmospheric)*.  
[^4]: MPS 137 Part 2 Slides, Slide 5: *Choosing the initial neutrino flavour (Muon neutrino beams)*.  
[^5]: MPS 137 Part 2 Slides, Slide 6: *Choosing the initial neutrino flavour (Electron neutrinos)*.  
[^6]: MPS 137 Part 2 Slides, Slide 7: *Choosing the initial neutrino flavour (Tau neutrinos)*.  
[^7]: MPS 137 Part 2 Slides, Slide 9: *Detecting tau neutrinos*.  
[^8]: MPS 137 Part 2 Slides, Slide 8 & Slide 33: *Electron and muon neutrino signatures (Water Cherenkov vs. LArTPC)*.  
[^9]: MPS 137 Part 2 Slides, Slide 10: *Case study: T2K overview*.  
[^10]: MPS 137 Part 2 Slides, Slide 12: *T2K near detector suite overview*.  
[^11]: MPS 137 Part 2 Slides, Slide 11: *T2K neutrino beam construction*.  
[^12]: MPS 137 Part 2 Slides, Slide 13: *INGRID beam monitor structure*.  
[^13]: MPS 137 Part 2 Slides, Slide 14: *ND280 off-axis detector overview*.  
[^14]: MPS 137 Part 2 Slides, Slide 15: *ND280 upgrade and tracking elements*.  
[^15]: MPS 137 Part 2 Slides, Slide 16: *T2K far detector: Super-Kamiokande setup*.  
[^16]: MPS 137 Part 2 Slides, Slide 17: *Super-Kamiokande photo gallery*.  
[^17]: MPS 137 Part 2 Slides, Slide 18: *Neutrino oscillations in T2K (Data plots)*.  
[^18]: MPS 137 Part 2 Slides, Slide 19: *Implications for the detector (Water purification)*.  
[^19]: MPS 137 Part 2 Slides, Slide 20: *Hyper-Kamiokande title concept*.  
[^20]: MPS 137 Part 2 Slides, Slide 21: *Hyper-Kamiokande detector overview*.  
[^21]: MPS 137 Part 2 Slides, Slide 22: *Hyper-Kamiokande layout and options*.  
[^22]: MPS 137 Part 2 Slides, Slide 23: *Hyper-Kamiokande vs Super-Kamiokande*.  
[^23]: MPS 137 Part 2 Slides, Slide 24: *The intermediate detector $\nu\text{PRISM}$ concept*.  
[^24]: MPS 137 Part 2 Slides, Slide 25: *The intermediate detector $\nu\text{PRISM}$ off-axis scanning*.  
[^25]: MPS 137 Part 2 Slides, Slide 26: *Hyper-Kamiokande and DUNE comparison*.  
[^26]: MPS 137 Part 2 Slides, Slide 27: *Deep Underground Neutrino Experiment (DUNE) diagram*.  
[^27]: MPS 137 Part 2 Slides, Slide 28: *DUNE baseline and non-accelerator sources*.  
[^28]: MPS 137 Part 2 Slides, Slide 29: *The DUNE experiment layout*.  
[^29]: MPS 137 Part 2 Slides, Slide 30: *DUNE neutrino beam tunes*.  
[^30]: MPS 137 Part 2 Slides, Slide 31: *DUNE near detector complex (PRISM, SAND, TMS, ND LAr)*.  
[^31]: MPS 137 Part 2 Slides, Slide 32: *DUNE far detector TPC modules*.  
[^32]: MPS 137 Part 2 Slides, Slide 34: *Key features of DUNE (Matter effects and mass hierarchy)*.  
[^33]: MPS 137 Part 2 Slides, Slide 35: *DUNE physics expectations*.  