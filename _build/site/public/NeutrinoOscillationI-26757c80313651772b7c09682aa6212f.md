# Physics of Neutrino Oscillations and Future Frontiers

*Based on MPS 137: Frontiers of Physics – Part 2 (University of Sheffield)*

## 1. Physics of Neutrino Oscillations

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

The unitary **Pontecorvo-Maki-Nakagawa-Sakata (PMNS)** matrix $U$ rotates between bases \[1,2\]:

$$
\vert{}\nu_\alpha\rangle = \sum_{k=1}^3 U_{\alpha k}^* \vert{}\nu_k\rangle \quad \Longleftrightarrow \quad \vert{}\nu_k\rangle = \sum_{\alpha} U_{\alpha k} \vert{}\nu_\alpha\rangle
$$

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

$$
U = \begin{pmatrix} 1 & 0 & 0 \\ 0 & c_{23} & s_{23} \\ 0 & -s_{23} & c_{23} \end{pmatrix} \begin{pmatrix} c_{13} & 0 & s_{13}e^{-i\delta_{CP}} \\ 0 & 1 & 0 \\ -s_{13}e^{i\delta_{CP}} & 0 & c_{13} \end{pmatrix} \begin{pmatrix} c_{12} & s_{12} & 0 \\ -s_{12} & c_{12} & 0 \\ 0 & 0 & 1 \end{pmatrix}
$$

*(where $c_{ij} = \cos\theta_{ij}$ and $s_{ij} = \sin\theta_{ij}$)*

#### Non-Trivial Mass Superposition

Because mixing angles are large ($\theta_{12} \approx 33.7^\circ, \theta_{23} \approx 49.1^\circ, \theta_{13} \approx 8.5^\circ$), individual flavour states are spread significantly across mass states. For instance, the muon neutrino state $\vert{}\nu_\mu\rangle = U_{\mu 1}^* \vert{}\nu_1\rangle + U_{\mu 2}^* \vert{}\nu_2\rangle + U_{\mu 3}^* \vert{}\nu_3\rangle$ has fractional contents:

$$
0.236 < \vert{}U_{\mu 1}^*\vert{} < 0.507, \quad 0.458 < \vert{}U_{\mu 2}^*\vert{} < 0.691, \quad 0.630 < \vert{}U_{\mu 3}^*\vert{} < 0.779
$$

Thus, there is no single "mass of a muon neutrino."

## 2. Quantum Mechanical Propagation and Probability Derivation

### Wavefunction Evolution in Space

Each mass eigenstate $\vert{}\nu_k\rangle$ evolves as a plane wave:

$$
\vert{}\nu_k(x)\rangle = e^{-i \frac{m_k^2 x}{2E}} \vert{}\nu_k(0)\rangle
$$

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

$$
P_{\alpha \rightarrow \beta}(L/E) = \sum_{k,j=1}^3 U_{\alpha k}^* U_{\beta k} U_{\alpha j} U_{\beta j}^* \exp\left( -i \frac{\Delta m_{kj}^2 L}{2E} \right)
$$

where $\Delta m_{kj}^2 \equiv m_k^2 - m_j^2$.

## 3. Experimental Measurement Regimes and $L/E$ Optimization

To measure specific parameters ($\Delta m_{ij}^2, \theta_{ij}$), an experiment must match its baseline distance $L$ and energy $E$ to the scale of the mass splitting:

$$
\left\vert{} \Delta m^2 \right\vert{} \sim \frac{E}{L}
$$

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

## 4. Experimental Setups: Near/Far Detectors vs. Flux Modeling

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

## 5. Summary of Key Knowledge Confirmed by 20th Century Physics

By the end of the 20th century, neutrino experiments confirmed four fundamental pillars:

1. **Three Flavour Eigenstates:** $\nu_e, \nu_\mu, \nu_\tau$.
2. **Neutrino Oscillations:** Neutrinos dynamically switch flavour in transit.
3. **Non-Zero Neutrino Mass:** Oscillations require $\Delta m_{ij}^2 \neq 0$, proving at least two neutrino mass states are non-zero.
4. **Chiral Suppression:** Right-handed neutrinos (and left-handed antineutrinos) do not participate in Standard Model weak interactions.

## 6. Open Questions at the End of the 20th Century

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

## References

\[1\] Pontecorvo, B. (1957). "Inverse Beta Processes and Non-conservation of Lepton Charge". *JETP*, 7, 172.

\[2\] Maki, Z., Nakagawa, M., & Sakata, S. (1962). "Remarks on the Unified Model of Elementary Particles". *Progress of Theoretical Physics*, 28(5), 870–880.