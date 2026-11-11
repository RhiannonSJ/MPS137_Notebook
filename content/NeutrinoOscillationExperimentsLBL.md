# Long Baseline Neutrino Oscillation Experiments 

## 1. Classification of Neutrino Oscillation Experiments

Neutrino oscillation experiments measure how the flavour composition of a source of neutrinos changes as it travels over a distance $L$. Experiments fall into two fundamental operational classes:

1. **Disappearance Experiments:** The experiment measures a reduction in the flux of the initial, original neutrino flavour ($\nu_\alpha \rightarrow \nu_\alpha$).
2. **Appearance Experiments:** The experiment measures the emergence of a neutrino flavour different from the initial state ($\nu_\alpha \rightarrow \nu_\beta$ where $\alpha \neq \beta$).

### Energy Threshold Constraints
For low-energy electron (anti)neutrinos ($E_\nu < m_\mu c^2 \approx 105.7\text{ MeV}$), such as those produced by the Sun or nuclear reactors, **only disappearance experiments are kinematically possible**. This is because the incoming neutrino does not possess enough energy to produce a muon ($m_\mu$) or tau ($m_\tau$) lepton via Charged-Current (CC) interactions. For higher-energy neutrinos, combined appearance and disappearance measurements are used to disentangle oscillation mixing angles such as $\theta_{13}$ and $\theta_{23}$.

---

## 2. Neutrino Sources, Production Mechanisms, and Detection

Neutrino experiments rely on different natural and artificial production mechanisms, each yielding distinct energy spectra and sensitivity to different PMNS matrix parameters ($\theta_{12}, \theta_{23}, \theta_{13}$, and $\delta_{\text{CP}}$).

| Source Type | Production Mechanism | Key Interaction / Flavour | Approximate Energy Range | Approximate Baseline ($L$) | Main Parameter Sensitivity | Example Experiments |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Reactor** | $\beta^-$ decay in nuclear reactors | Pure $\bar{\nu}_e$| Few $\text{MeV}$ ($E > 1.8\text{ MeV}$) | Short to Medium ($L \sim \text{m}$ to $\sim 180\text{ km}$) | $\theta_{13}, \theta_{12}$ (depends on $L$) | KamLAND, Daya Bay, RENO, Double Chooz |
| **Solar** | Proton-proton chain & CNO cycle in the Sun ($pp$, $pep$, $hep$, $^{7}\text{Be}$, $^{8}\text{B}$) | Pure $\nu_e$ | Sub-$\text{MeV}$ to $\sim 15\text{ MeV}$ | Earth–Sun distance ($L \sim 1.5 \times 10^8\text{ km}$) | $\theta_{12}, \theta_{13}$ | SAGE, GALLEX, Borexino, SNO |
| **Atmospheric** | Cosmic-ray protons hitting Earth's atmosphere $\rightarrow$ hadron shower ($\pi^\pm, K^\pm$) | $\nu_e, \bar{\nu}_e, \nu_\mu, \bar{\nu}_\mu$ | $\sim 100\text{ MeV}$ to $\text{TeV}$ | $\sim 10\text{ km}$ to $12,700\text{ km}$ (Earth diameter) | $\theta_{23}, \theta_{13}, \delta_{\text{CP}}$ | Super-Kamiokande, IceCube |
| **Accelerator** | High-intensity $p^+$ beam hit on target $\rightarrow$ focused $\pi^\pm/K^\pm$ decay in flight | Primarily $\nu_\mu$ or $\bar{\nu}_\mu$ beam | Hundreds of $\text{MeV}$ to $\text{GeV}$ | Long-baseline ($L \sim 295\text{ km}$ for T2K/HK; $1300\text{ km}$ for DUNE) | $\theta_{23}, \theta_{13}, \delta_{\text{CP}}$ | T2K, Super-K, Hyper-K, NO$\nu$A, MINOS(+), DUNE, SBN |

### Production Details by Flavour
* **$\nu_\mu$ Beams:** Protons are accelerated and fired at a dense target (e.g., graphite), producing charged pions ($\pi^\pm$). Magnetic "horns" focus either positive or negative pions into a parallel beam. The pions decay in flight (e.g., $\pi^+ \rightarrow \mu^+ + \nu_\mu$), producing an almost pure $\nu_\mu$ or $\bar{\nu}_\mu$ beam. The decay of secondary muons ($\mu^\pm \rightarrow e^\pm + \nu_e/{\bar{\nu}_e} + \bar{\nu}_\mu/{\nu}_\mu$) introduces a small intrinsic $\nu_e$ background.
* **$\nu_e$:** Readily available from natural sources (Sun) and nuclear reactors ($\bar{\nu}_e$).
* **$\nu_\tau$:** Tau neutrinos cannot be produced via pion decay due to the high mass of the $\tau$ lepton. Instead, they require the decay of charmed mesons, requiring primary proton beams with energies $\sim 100\times$ higher than those needed for muon neutrinos. $\nu_\tau$ are detected via CC interactions ($ \nu_\tau + N \rightarrow \tau^- + X $), requiring high neutrino energy ($E_\nu > m_\tau c^2$) and ultra-high resolution detectors (such as DONUT) capable of resolving the sub-millimetre "kinked" track of the short-lived $\tau$ lepton.

---

## 3. Detector Technologies and Event Signatures

To distinguish between neutrino flavours, detectors identify the charged lepton produced in Charged-Current (CC) interactions ($\nu_\ell + N \rightarrow \ell^- + X$).

1. **Water Cherenkov Detectors (e.g., Super-Kamiokande):**

   **Muon ($\nu_\mu$ signature):** A heavy muon travels at relativistic speeds through water without scattering much, producing a **sharp, well-defined Cherenkov light ring**.
   
   **Electron ($\nu_e$ signature):** A light electron undergoes multiple Coulomb scattering and pair-production/bremsstrahlung, creating an electromagnetic shower. This results in a **fuzzy, diffuse-edged ring**.
2. **Liquid Argon Time Projection Chambers (LArTPCs) (e.g., DUNE, SBN):**
   
   **Muon ($\nu_\mu$ signature):** Displays a single, long, sharp continuous ionizing track.
   
   **Electron ($\nu_e$ signature):** Displays an initial single track that rapidly branches into an electromagnetic shower pattern.

---

## 4. Current-Generation Experiment: T2K

The **T2K (Tokai to Kamioka)** experiment in Japan is a second-generation long-baseline neutrino oscillation experiment [^1].

### Core Parameters & Setup
* **Baseline ($L$):** $295\text{ km}$ from J-PARC (Tokai) to Super-Kamiokande (Kamioka).
* **Off-Axis Technique:** The beam is directed $2.5^\circ$ off-axis relative to the far detector. This off-axis geometry narrows the energy spectrum of the neutrino beam, peaking precisely at $\sim 0.6\text{ GeV}$, which matches the oscillation maximum for $L = 295\text{ km}$ while suppressing high-energy backgrounds.
* **Primary Physics Goals:** Precise measurement of $\theta_{13}$ (first established via $\nu_e$ appearance), refining $\theta_{23}$, and probing the CP-violating phase $\delta_{\text{CP}}$.

### Beam Production and Magnet System
1. 30 GeV protons from the J-PARC Main Ring hit a graphite rod target, generating charged pions ($\pi^\pm$).
2. Three magnetic horns focus $\pi^+$ (for neutrino mode) or $\pi^-$ (for antineutrino mode) into a $110\text{ m}$ decay volume where they decay to $\mu^+ + \nu_\mu$ or $\mu^- + \bar{\nu}_\mu$.

### Detector Suite
* **INGRID (Interactive Neutrino GRID):** On-axis near detector ($280\text{ m}$ from target). Its cross-shaped structure of alternating iron/lead absorbers and plastic scintillators monitors beam center symmetry and flux daily via $\nu_\mu$ interactions [^1].
* **ND280:** Off-axis near detector ($280\text{ m}$ from target). Placed inside a $0.2\text{ T}$ recycled UA1 magnet, it uses Time Projection Chambers (TPCs), Fine-Grain Detectors (FGDs), Electromagnetic Calorimeters (ECALs), and recently a Super Fine-Grain Detector (SFGD) [^2].
  * *Role:* Measures intrinsic $\nu_e$ background and characterizes neutral-current $\pi^0$ production cross-sections (since a single photon from $\pi^0 \rightarrow \gamma\gamma$ can fake a $\nu_e$ electron ring in Super-K).
* **Super-Kamiokande (Far Detector):** A $50\text{ kton}$ water Cherenkov detector situated under Mt. Ikeno-Yama ($1000\text{ m}$ rock cover / $2700\text{ m}$ water equivalent) [^1].
  * *Inner Detector (ID):* Instrumented with $\sim 11,000$ inward-facing $50\text{ cm}$ Photomultiplier Tubes (PMTs).
  * *Outer Detector (OD):* Instrumented with $\sim 2,000$ outward-facing $20\text{ cm}$ PMTs serving as an active veto for cosmic rays.
  * *Water Quality:* Highly purified through RO, UV, and ultra-filtration systems to minimize light absorption and radioactive backgrounds (e.g., Radon).

### Oscillation Results in T2K
* **$\nu_\mu / \bar{\nu}_\mu$ Disappearance:** A sharp drop in muon events around $E_\nu \sim 0.6\text{ GeV}$ constrains $\theta_{23}$ and $|\Delta m^2_{32}|$.
* **$\nu_e / \bar{\nu}_e$ Appearance:** Direct observation of $e$-like Cherenkov rings in a predominantly $\nu_\mu$ beam provided primary evidence for non-zero $\theta_{13}$ and initial constraints on $\delta_{\text{CP}}$.

---

## 5. Next-Generation Experiment: Hyper-Kamiokande

**Hyper-Kamiokande (Hyper-K)** is the flagship successor to T2K, featuring an upgraded beam intensity and a massive new far detector [^3].

### Key Upgrades
* **Far Detector Target Mass:** A giant cylindrical water Cherenkov tank containing **$258\text{ kton}$** of ultrapure water ($\sim 5\times$ larger target volume than Super-K) [^3].
* **Photosensors:** High-efficiency PMTs with doubled quantum efficiency and better timing resolution compared to SK.
* **Intermediate Detector ($\nu\text{PRISM}$):** Placed at $1\text{--}2\text{ km}$ from the target. The detector moves vertically inside a deep shaft, scanning across different off-axis angles ($1.0^\circ$ to $4.0^\circ$) [^3].
  * *Purpose:* By taking data at varying off-axis angles, $\nu\text{PRISM}$ can construct a customized, energy-dependent neutrino flux matching the oscillated spectrum at Hyper-K, dramatically reducing systematic errors on cross-sections.

---

## 6. Next-Generation Experiment: DUNE

The **Deep Underground Neutrino Experiment (DUNE)** is an international long-baseline experiment based in the United States [^4].

### Experimental Architecture
* **Baseline ($L$):** $1300\text{ km}$ (800 miles), sending neutrinos through the Earth from Fermilab (Illinois) to the Sanford Underground Research Facility (SURF, South Dakota) [^4].
* **Beam:** An on-axis, **broad-band** high-energy beam produced by the PIP-II proton accelerator at Fermilab. The beam spectrum can be adjusted (e.g., Low Energy "LE" tune) to optimize sensitivity to $\delta_{\text{CP}}$ [^5].
* **Far Detector:** Underground liquid argon TPCs (LArTPCs) modular system consisting of four $17\text{ kton}$ modules (both horizontal-drift and vertical-drift designs) [^4].

### Scientific Capabilities & Complementarity with Hyper-K
1. **Matter Effects and Mass Hierarchy:** Because DUNE has a long baseline ($1300\text{ km}$) through Earth's mantle, electron neutrinos experience coherent forward scattering with electrons in terrestrial matter. This modifies the oscillation probability in a way sensitive to the sign of $\Delta m^2_{31}$, allowing DUNE to definitively resolve the **neutrino mass ordering** (Normal: $m_3 > m_2 > m_1$ vs. Inverted: $m_2 > m_1 > m_3$).
2. **CP Violation Phase ($\delta_{\text{CP}}$):** Broad-band beam energy coverage allows DUNE to measure multiple oscillation nodes, disentangling CP violation effects from matter effects.
3. **Non-Accelerator Physics:** Search for proton decay, detection of atmospheric neutrinos, and sensitivity to galactic supernova neutrinos (DUNE is sensitive primarily to $\nu_e + ^{40}\text{Ar} \rightarrow e^- + ^{40}\text{K}^*$, whereas Hyper-K is sensitive to $\bar{\nu}_e + p \rightarrow e^+ + n$ via inverse beta decay).

## Comparison Summary: Hyper-K vs. DUNE

| Parameter / Feature | Hyper-Kamiokande (HK) | Deep Underground Neutrino Experiment (DUNE) |
| :--- | :--- | :--- |
| **Location** | Japan (J-PARC $\rightarrow$ Tochibora) | USA (Fermilab $\rightarrow$ SURF) |
| **Baseline ($L$)** | $295\text{ km}$ | $1300\text{ km}$ |
| **Beam Configuration** | Off-axis ($2.5^\circ$), Narrow-band | On-axis, Broad-band |
| **Far Detector Technology** | Water Cherenkov ($258\text{ kton}$) | Liquid Argon TPC ($4 \times 17\text{ kton}$) |
| **Supernova Sensitivity** | Primary sensitivity to $\bar{\nu}_e$ (IBD) | Primary sensitivity to $\nu_e$ ($\text{Ar}$-CC) |
| **Matter Effects** | Modest | Dominant (determines mass hierarchy cleanly) |

[^1]: K. Abe et al. (T2K Collaboration), "Overview of the T2K long baseline neutrino oscillation experiment," *Nucl. Instrum. Meth. A* 659 (2011) 106-135; arXiv:0910.4211.
[^2]: H. Kobayashi et al. (T2K Collaboration), "Upgrade and Cross-Section Measurement Status of the T2K ND280 Near Detector," *Proc. Neutrino Conferences*.
[^3]: K. Abe et al. (Hyper-Kamiokande Collaboration), "Hyper-Kamiokande Design Report," arXiv:1805.04163 (2018).
[^4]: B. Abi et al. (DUNE Collaboration), "Deep Underground Neutrino Experiment (DUNE), Far Detector Technical Design Report," *JINST* 15 (2020) T08008; arXiv:2002.03005.
[^5]: A. Abed Abud et al. (DUNE Collaboration), "Snowmass Neutrino Frontier: DUNE Physics Program," arXiv:2203.06100 (2022).