# Statistical Methods for Neutrino Oscillation Parameter Estimation & Contour Generation

The primary objective of this document is to guide the reader from fundamental statistical concepts to the practical construction and interpretation of **frequentist confidence regions (exclusion/allowed parameter contours)**.

---

## 1. Neutrino Oscillation Foundations & Event Rates

As established previously, in a simplified two-flavour approximation, the probability that a neutrino of initial flavour $\alpha$ is detected as flavour $\beta$ after travelling a distance $L$ (in km) with energy $E$ (in GeV) is given by[^1]:

$$P_{\alpha \to \beta}(E, L; \mathbf{\psi}) = \sin^2(2\theta) \sin^2\left( 1.27 \, \frac{\Delta m^2 \, [\text{eV}^2] \, L \, [\text{km}]}{E \, [\text{GeV}]} \right)$$

where $\mathbf{\psi} = (\theta, \Delta m^2)$ represents the vector of physical oscillation parameters[^2].

Experimentally, neutrino detectors do not measure the continuous probability function directly, nor do they measure the true incoming neutrino energy $E$ (often denoted $E_{\text{true}}$) with perfect accuracy. Instead, detectors measure final-state particle tracks and energy deposits to compute a **reconstructed energy**, $E_{\text{rec}}$.

The reconstructed energy $E_{\text{rec}}$ is a smeared observation of $E_{\text{true}}$, governed by the detector's energy resolution, thresholds, and missing neutral energy (e.g., escaping neutrons). This relationship is formally bridged by the response matrix $R(E_{\text{rec}}, E_{\text{true}})$, which defines the conditional probability density of observing $E_{\text{rec}}$ given a true incoming energy $E_{\text{true}}$.

Neutrino oscillation parameter estimation relies on observing how the binned histogram of reconstructed energy $E_{\text{rec}}$ is modulated relative to the unoscillated prediction:

1. **Disappearance Mode (e.g., $\nu_\mu \to \nu_\mu$):** The oscillation manifests as a characteristic "dip" or deficit in the event count histogram around the reconstructed energy corresponding to maximum oscillation probability (where $1.27 \Delta m^2 L / E_{\text{true}} \approx \pi / 2$). The **depth** of this dip constrains the mixing angle $\sin^2(2\theta)$, while the **energy position** of the minimum constrains the mass-squared difference $\Delta m^2$.
2. **Appearance Mode (e.g., $\nu_\mu \to \nu_e$):** The signal appears as an excess of events above background in a channel that was originally absent or suppressed in the initial flux.
3. **Near-to-Far Baseline Ratios:** Long-baseline experiments frequently deploy two detectors: a **Near Detector** placed close to the neutrino source (where oscillations have not yet developed) to measure the unoscillated flux and cross-sections, and a **Far Detector** placed at distance $L$ to record the oscillated spectrum[^3]. Comparing event counts bin-by-bin between the Far and Near detectors cancels major correlated systematic uncertainties in the flux and interaction physics.

In an actual experimental detector, the expected number of events $\mu_i$ in reconstructed energy bin $i$ integrates over all true incoming energies $E_{\text{true}}$ weighted by the probability $P_{\alpha \to \beta}(E_{\text{true}}, L; \mathbf{\psi})$ and smeared by $R(E_{\text{rec}}, E_{\text{true}})$:

$$\mu_i(\mathbf{\psi}) = \int_{\text{bin } i} dE_{\text{rec}} \int dE_{\text{true}} \, \Phi(E_{\text{true}}) \, P_{\alpha \to \beta}(E_{\text{true}}, L; \mathbf{\psi}) \, \sigma(E_{\text{true}}) \, R(E_{\text{rec}}, E_{\text{true}}) \, \epsilon(E_{\text{rec}}) + B_i$$

where $\Phi(E_{\text{true}})$ is the initial flux, $\sigma(E_{\text{true}})$ is the interaction cross-section, $\epsilon(E_{\text{rec}})$ is the detection efficiency, and $B_i$ is the expected background contribution.

---

## 2. Monte Carlo Simulations & Event Generation

In a simple physics experiment, you might predict outcome probabilities using a direct formula. However, calculating the expected event count $\mu_i(\mathbf{\psi})$ analytically is practically impossible. A realistic neutrino experiment involves complex, non-linear cross-sections $\sigma(E_{\text{true}})$, complicated detector geometry, and intricate energy loss mechanisms as charged particles track through matter.

To overcome this, experimentalists use **Monte Carlo (MC) simulations**. Named after the famous casino, the Monte Carlo method uses pseudo-random numbers to simulate millions of individual, hypothetical particle interactions one-by-one according to the laws of quantum mechanics and classical physics. By aggregating millions of these simulated events, we build up predicted histograms that can be directly compared with real experimental data.

### Step 1: Simulating Primary Particle Kinematics (Neutrino Generators)

Before a particle enters a detector, its initial interaction must be generated using dedicated event-generation software (such as GENIE[^4] or NEUT).

1. **Sampling Neutrino Energy:** The initial flux $\Phi(E_{\text{true}})$ gives a continuous probability distribution of incoming energies. The simulator uses random sampling techniques (like rejection sampling) to pick a specific energy $E_{\text{true}}$ for individual simulated event $k$.
2. **Applying Conservation Laws:** When the simulated neutrino strikes an atomic nucleus (e.g., carbon or oxygen in a water or liquid argon target), quantum mechanics dictates the target collision outcome. The generator calculates the probability of producing specific outgoing particles (such as muons, pions, or protons) using interaction cross-sections $\sigma(E_{\text{true}})$.
3. **Determining Vectors:** Using standard relativistic momentum and energy conservation ($\sum E_{\text{initial}} = \sum E_{\text{final}}$ and $\sum \mathbf{p}_{\text{initial}} = \sum \mathbf{p}_{\text{final}}$), the simulator calculates the initial direction vectors, velocities, and kinetic energies of all final-state particles emerging from the collision vertex.

### Step 2: Simulating Detector Tracking & Energy Loss (GEANT4)

Once the secondary particles leave the atomic nucleus, they travel through the detector medium. Software toolkits like GEANT4[^5] simulate their transport step-by-step:

1. **Ionisation & Radiation Loss:** Charged particles (like muons or electrons) lose kinetic energy as they pass through matter by knocking electrons off surrounding atoms (ionisation) or emitting radiation. GEANT4 steps each particle forward by a small distance $\Delta x$ and subtracts energy using stopping-power equations (e.g., the Bethe-Bloch formula).
2. **Signal Generation:** The lost energy is converted into detectable signals based on detector technology—for instance, Cherenkov light cones in water, scintillation photons, or drifted ionisation electrons in high-voltage fields.
3. **Detector Geometry:** GEANT4 tracks particles through precise 3D CAD models of the apparatus, accounting for dead regions, structural support walls, and physical boundaries where particles might escape unmeasured.

### Step 3: Software Reconstruction Pipeline

The raw, simulated signals (photon hits, wire charges) pass through the exact same reconstruction code used for real experimental data. The algorithms re-cluster light hits and fit tracks to output a final **reconstructed energy** $E_{\text{rec}}$ for each simulated event.

### Step 4: Event-by-Event Reweighting

Simulating millions of events through full GEANT4 propagation requires enormous computing power. If we want to test a new trial set of oscillation parameters $\mathbf{\psi} = (\sin^2 2\theta, \Delta m^2)$, running the full GEANT4 simulation from scratch for every iteration would be computationally impossible.

Instead, we generate a single, unoscillated Monte Carlo dataset where every simulated event $k$ starts with an initial baseline weight $w_k^{(0)} = 1$. When testing a specific oscillation hypothesis $\mathbf{\psi}$, we simply multiply each event's weight by its calculated oscillation probability based on its known true energy $E_{k, \text{true}}$ and baseline distance $L$:

$$w_k(\mathbf{\psi}) = w_k^{(0)} \cdot P_{\alpha \to \beta}(E_{k, \text{true}}, L; \mathbf{\psi})$$

The total predicted count $\mu_i(\mathbf{\psi})$ in any reconstructed energy bin $i$ is then obtained by summing the weights of all simulated events that fell into that bin:

$$\mu_i(\mathbf{\psi}) = \sum_{k \in \text{bin } i} w_k(\mathbf{\psi})$$

This reweighting technique allows fitting routines to scan thousands of physics parameter combinations in seconds.

---

## 3. Concepts: Goodness-of-Fit & Degrees of Freedom

Before we can use experimental data to estimate unknown physics parameters (like neutrino mixing angles), we need a rigorous way to compare our observed data against theoretical predictions. Two core concepts form the bedrock of this comparison:

### Goodness-of-Fit (GoF)

Suppose you roll a six-sided die 60 times and roll a "6" 18 times instead of the expected 10 times. Is the die biased, or did you just get lucky? A **Goodness-of-Fit (GoF)** test answers this question quantitatively[^6].

1. **The Null Hypothesis ($H_0$):** We start with a baseline assumption called the **null hypothesis**. In particle physics, $H_0$ is usually the statement: **"The Monte Carlo simulation perfectly describes the physical reality, and any observed differences are purely due to random statistical fluctuations."**
2. **The Test Statistic ($t$):** We condense the overall discrepancy between the observed data histogram and the predicted simulation into a single number called a **test statistic** (often denoted $t$ or $\chi^2$). A test statistic of $t = 0$ means absolute identical match, while larger values of $t$ represent increasing disagreement.
3. **Evaluating Discrepancy:** Rather than giving a simple "yes" or "no", a GoF test calculates the mathematical probability of getting a test statistic as large as $t$ (or larger) purely by random chance under $H_0$. If that probability is extremely small, we reject the model hypothesis $H_0$.

### Degrees of Freedom ($\text{ndof}$)

To interpret whether a test statistic value is "large" or "small", we must know how many independent ways the data was free to deviate from the model. This is controlled by the **degrees of freedom** ($\text{ndof}$).

Think of $\text{ndof}$ like solving a system of simultaneous algebraic equations:
* Every independent data bin in your histogram gives you **+1 piece of information** (an independent observation).
* Every parameter you estimate or fit from that same data **uses up 1 degree of freedom** (reducing flexibility).
* Every global constraint you enforce (such as fixing the total number of events to match) also **uses up 1 degree of freedom**.

Formally, the total degrees of freedom is calculated as:

$$\text{ndof} = k - p - c$$

where:
* $k$ is the total number of independent histogram energy bins.
* $p$ is the number of free parameters adjusted during the fit (e.g., fitting both $\theta$ and $\Delta m^2$ gives $p = 2$).
* $c$ is the number of fixed external constraints applied to the dataset.

**Intuitive Example:** Imagine drawing a straight line through data points ($y = mx + c$). You are fitting $p = 2$ parameters (slope $m$ and intercept $c$). If you only have $k = 2$ data points, then $\text{ndof} = 2 - 2 = 0$. The line will fit the points **perfectly** regardless of physics, meaning you have zero degrees of freedom left to test whether a straight line was actually a good theoretical model! You need $k > 2$ points ($\text{ndof} > 0$) to test the model's validity.

In neutrino physics, $\text{ndof}$ determines the specific shape of the reference statistical distribution (such as the $\chi^2_{\text{ndof}}$ curve) used to convert a raw test statistic into a meaningful $p$-value.

---

## 4. Data-MC Compatibility Tests

Before attempting to extract neutrino oscillation parameters from a Far Detector, we must verify that our Monte Carlo simulation accurately models the unoscillated particle interactions at the Near Detector or in control samples. If the baseline simulation fails to match unoscillated data, any inferred oscillation signal will be invalid.

### Pearson's Chi-Squared Test (Binned Data)

In an A-level physics lab, when you measure a line of best fit, you calculate deviations using $\text{residual} = y_i - y_{\text{model}}$. Pearson's $\chi^2$ test applies the same logic to histogram bins[^7]:

$$\chi^2_{\text{Pearson}} = \sum_{i=1}^k \frac{(N_i - \mu_i)^2}{\mu_i}$$

1. **Numerator—Square of Deviations:** For bin $i$, we take the difference between observed counts $N_i$ and expected simulation counts $\mu_i$, then square it $(N_i - \mu_i)^2$. Squaring ensures that positive and negative discrepancies do not cancel each other out.
2. **Denominator—Variance Weighting:** According to Poisson statistics, for a count of $\mu_i$, the natural statistical variance is $\sigma_i^2 = \mu_i$. Dividing by $\mu_i$ scales each bin discrepancy by its expected random variance. A discrepancy of 10 events is huge if you only expected 5 ($\frac{10^2}{5} = 20$), but negligible if you expected 1,000 ($\frac{10^2}{1000} = 0.1$).
3. **Interpretation:** If the simulation is correct, the average contribution from each bin to the sum is roughly $1$. Therefore, a good fit yields an overall $\chi^2_{\text{Pearson}} \approx \text{ndof}$. A ratio $\chi^2 / \text{ndof} \gg 1$ signals significant data-MC disagreement.
4. **Condition:** This approximation assumes Gaussian-like bin fluctuations, which requires $N_i, \mu_i \gtrsim 5$ events per bin.

### Kolmogorov-Smirnov (K-S) Test (Unbinned & Shape Comparison)

Grouping continuous data into histogram bins discards information about where particles fell **inside** each bin. The Kolmogorov-Smirnov (K-S) test avoids binning entirely by comparing **Cumulative Frequency Curves**[^8].

1. **Empirical CDF ($F_N(x)$):** Sort the $N$ observed neutrino energies in ascending order. Plot the step-wise cumulative fraction of events from $0.0$ to $1.0$.
2. **Theoretical CDF ($F_0(x)$):** Integrate the continuous simulation density function to form its cumulative probability curve from $0.0$ to $1.0$.
3. **K-S Statistic ($D$):** Find the point along the energy axis $x$ where the vertical distance between the two cumulative curves is largest:

$$D = \sup_x |F_N(x) - F_0(x)|$$

Because $D$ measures maximum vertical separation, it is sensitive purely to the **shape** of the distribution (e.g., shifts in energy scale or peak positions) without being biased by chosen histogram bin boundaries.

### $p$-values & Gaussian Signatures ($\sigma$)

Once a test statistic $t_{\text{obs}}$ (such as $\chi^2_{\text{Pearson}}$ or $D$) is calculated from experimental data, we determine its **$p$-value**:

$$p = P(t \ge t_{\text{obs}} \mid H_0) = \int_{t_{\text{obs}}}^\infty f(t \mid H_0) \, dt$$

In simple terms, the $p$-value is the area under the theoretical probability density curve $f(t \mid H_0)$ from $t_{\text{obs}}$ out to infinity.

| Threshold | Equivalent $p$-value | Interpretation in Particle Physics |
| :--- | :--- | :--- |
| **$1\sigma$ ($z = 1.0$)** | $0.317$ ($31.7\%$) | Typical random fluctuation; excellent data-MC agreement. |
| **$2\sigma$ ($z = 2.0$)** | $0.0455$ ($4.55\%$) | Slight tension; standard cutoff ($p < 0.05$) to reject compatibility. |
| **$3\sigma$ ($z = 3.0$)** | $0.0027$ ($0.27\%$) | **Evidence:** Strong indication that MC simulation is missing physics or systematic calibration. |
| **$5\sigma$ ($z = 5.0$)** | $2.87 \times 10^{-7}$ | **Discovery:** Mathematical certainty of a new effect or complete model breakdown. |

If $p < 0.05$ ($2\sigma$), we reject the null hypothesis $H_0$ and must refine detector response or interaction models before proceeding to neutrino oscillation fits.

---

## 5. Statistical Likelihoods & Fitting Distributions

Because neutrinos interact so weakly with matter, particle detectors often record very small numbers of events—sometimes just 0, 1, or 2 counts in high-energy histogram bins. In this low-statistics regime, the Gaussian assumption of Pearson's $\chi^2$ fails, and we must construct fits using **Poisson statistics**.

### Binned Poisson Likelihood

The probability of observing exactly $N_i$ discrete counts in bin $i$, when expecting a theoretical average rate of $\mu_i(\mathbf{\psi})$, is given by the standard Poisson probability mass function (PMF):

$$P(N_i \mid \mu_i(\mathbf{\psi})) = \frac{\mu_i(\mathbf{\psi})^{N_i} e^{-\mu_i(\mathbf{\psi})}}{N_i!}$$

Assuming each histogram energy bin is statistically independent, the joint probability of observing an entire experimental dataset across all $k$ bins is the product of their individual probabilities. This total joint probability is called the **Likelihood function**, $\mathcal{L}(\mathbf{\psi})$:

$$\mathcal{L}(\mathbf{\psi}) = \prod_{i=1}^k \frac{\mu_i(\mathbf{\psi})^{N_i} e^{-\mu_i(\mathbf{\psi})}}{N_i!}$$

### The Negative Log-Likelihood (NLL)

In practice, multiplying dozens of tiny probabilities together produces numbers extremely close to zero, causing computational rounding errors (underflow). Furthermore, differentiating products is algebraically difficult.

To solve this, we take the natural logarithm ($\ln$) of the likelihood function. Using logarithmic laws ($\ln(ab) = \ln a + \ln b$ and $\ln(a^b) = b \ln a$), multiplication converts into simple addition:

$$\ln \mathcal{L}(\mathbf{\psi}) = \sum_{i=1}^k \left[ N_i \ln \mu_i(\mathbf{\psi}) - \mu_i(\mathbf{\psi}) - \ln(N_i!) \right]$$

Because numerical optimization algorithms are designed to find the **minimum** of a function rather than its maximum, we multiply by $-1$ to define the **Negative Log-Likelihood (NLL)**:

$$-\ln \mathcal{L}(\mathbf{\psi}) = \sum_{i=1}^k \left[ \mu_i(\mathbf{\psi}) - N_i \ln \mu_i(\mathbf{\psi}) + \ln(N_i!) \right]$$

The trial parameters $\mathbf{\psi} = (\sin^2 2\theta, \Delta m^2)$ that **minimise** the NLL represent the **Maximum Likelihood Estimate (MLE)**—the physics values that make our observed experimental data most probable.

### Cash Statistic / Poisson Chi-Square ($\chi^2_{\text{Poisson}}$)

While the NLL allows parameter estimation, its raw numerical value is not easily interpretable as a Goodness-of-Fit test because the term $\sum \ln(N_i!)$ acts as an offset.

To construct a test statistic that behaves like a standard $\chi^2$, we form a **Likelihood Ratio** relative to the "saturated model"—an ideal, perfect hypothesis where the prediction in every bin matches the data exactly ($\mu_i = N_i$)[^9].

By defining $\chi^2_{\text{Poisson}}(\mathbf{\psi}) \equiv 2 \left[ \ln \mathcal{L}(\text{perfect}) - \ln \mathcal{L}(\mathbf{\psi}) \right]$, the $\ln(N_i!)$ terms cancel out completely, yielding the **Baker-Cousins statistic**:

$$\chi^2_{\text{Poisson}}(\mathbf{\psi}) = 2 \sum_{i=1}^k \left[ \mu_i(\mathbf{\psi}) - N_i + N_i \ln \left(\frac{N_i}{\mu_i(\mathbf{\psi})}\right) \right]$$

1. **Perfect Match:** If predicted counts equal observed counts ($\mu_i = N_i$) in every bin, then $\ln(1) = 0$ and $\mu_i - N_i = 0$, giving $\chi^2_{\text{Poisson}} = 0$.
2. **Zero-Count Bins:** If a bin observes zero events ($N_i = 0$), the expression simplifies cleanly to $2 \mu_i(\mathbf{\psi})$ using the limit $\lim_{N_i \to 0} N_i \ln(N_i) = 0$.
3. **High-Statistics Limit:** For large counts ($N_i \gg 1$), we can write $\mu_i = N_i (1 + \delta)$ with $\delta \ll 1$. Applying the Taylor series expansion $\ln(1 + \delta) \approx \delta - \frac{\delta^2}{2}$ demonstrates that $\chi^2_{\text{Poisson}}$ converges exactly to Pearson's $\chi^2_{\text{Pearson}} = \sum \frac{(N_i - \mu_i)^2}{\mu_i}$.

---

## 6. Systematic Uncertainties & Nuisance Parameters

In an ideal A-level physics lab, every measurement error is purely **random noise**—repeating an experiment 10,000 times would make the average value converge perfectly to the true physical value ($\sigma_{\bar{x}} = \sigma / \sqrt{N}$).

In real-world particle physics, however, experiments are dominated by **systematic uncertainties**. These are non-random calibration offsets, flux uncertainties, or theoretical assumptions that shift your entire data distribution in a systematic way.

### Defining Nuisance Parameters ($\mathbf{\eta}$)

When extracting fundamental physics parameters of interest $\mathbf{\psi} = (\sin^2 2\theta, \Delta m^2)$, our predictions also depend on auxiliary experimental parameters that we do not care about directly, but cannot ignore. We call these **nuisance parameters**, denoted $\mathbf{\eta} = (\eta_1, \eta_2, \dots, \eta_m)$.

Typical examples in a neutrino experiment include:
* **Neutrino Flux Normalisation ($\eta_{\text{flux}}$):** The overall intensity of the particle beam might be uncertain by $\pm 5\%$.
* **Detector Energy Scale ($\eta_{\text{scale}}$):** The calibration factor converting light/charge hits into GeV might be off by $\pm 2\%$, shifting energy bins left or right.
* **Cross-Section Uncertainty ($\eta_{\sigma}$):** Theoretical models predicting how neutrinos scatter off atomic nuclei carry uncertainties.

If a systematic parameter shifts away from its baseline value ($\eta_j \neq \hat{\eta}_j$), it modifies the expected event count in every bin $\mu_i(\mathbf{\psi}, \mathbf{\eta})$.

### Penalty Terms (Chi-Squared Priors)

We rarely start an experiment completely ignorant of our apparatus. Prior calibration experiments (e.g., testing the detector in a beam line at CERN) constrain how far nuisance parameters are likely to deviate.

To incorporate this prior knowledge into our fit, we add a quadratic **penalty term** (also called a Gaussian constraint or prior) to the total test statistic:

$$\chi^2_{\text{total}}(\mathbf{\psi}, \mathbf{\eta}) = \chi^2_{\text{data}}(\mathbf{\psi}, \mathbf{\eta}) + \sum_{j=1}^m \frac{(\eta_j - \hat{\eta}_j)^2}{\sigma_{\eta_j}^2}$$

1. **Data Match Term ($\chi^2_{\text{data}}$):** Measures how well the predicted spectrum matches the observed histogram (using the Poisson formula from Section 5).
2. **Penalty Term ($\sum \frac{(\eta_j - \hat{\eta}_j)^2}{\sigma_{\eta_j}^2}$):** Penalises the fit if it tries to pull systematic parameter $\eta_j$ far away from its nominal central value $\hat{\eta}_j$, scaled by its external calibration uncertainty $\sigma_{\eta_j}$.

**The Spring Analogy:** Think of a penalty term like Hooke's Law ($E_p = \frac{1}{2} k x^2$). The fitting routine is free to "stretch" a nuisance parameter to make the data fit better, but the spring pulls back with a quadratic restoring force. A shift of $1\sigma$ adds $+1.0$ to $\chi^2_{\text{total}}$, while a shift of $3\sigma$ adds a heavy penalty of $+9.0$.

When systematic parameters are correlated (e.g., shifting energy scale in one bin affects adjacent bins), the individual sum expands into a **Covariance Matrix** $\mathbf{V}$, yielding the full matrix penalty term[^10]:

$$\chi^2_{\text{total}}(\mathbf{\psi}, \mathbf{\eta}) = \chi^2_{\text{data}}(\mathbf{\psi}, \mathbf{\eta}) + (\mathbf{\eta} - \hat{\mathbf{\eta}})^T \mathbf{V}^{-1} (\mathbf{\eta} - \hat{\mathbf{\eta}})$$

### Profile Likelihood Formulation

Our goal is to draw a 2D contour for physics parameters $\mathbf{\psi}$, but our total function $\chi^2_{\text{total}}(\mathbf{\psi}, \mathbf{\eta})$ lives in a high-dimensional space (often 2 physics parameters + 50 nuisance parameters!).

To reduce this complex space down to the physics parameters of interest, we use a technique called **profiling**:

$$\chi^2_{\text{profile}}(\mathbf{\psi}) = \min_{\mathbf{\eta}} \chi^2_{\text{total}}(\mathbf{\psi}, \mathbf{\eta})$$

**How Profiling Works Step-by-Step:**
1. Fix the physics parameters to a specific grid point—say, $\mathbf{\psi}_0 = (\sin^2 2\theta = 0.85, \Delta m^2 = 2.4 \times 10^{-3} \text{ eV}^2)$.
2. Hold $\mathbf{\psi}_0$ constant, and let an automated optimization algorithm adjust all $m$ nuisance parameters $\mathbf{\eta}$ simultaneously until it finds the combination $\hat{\mathbf{\eta}}_{\text{best}}$ that **minimises** $\chi^2_{\text{total}}$.
3. Record that minimum value as $\chi^2_{\text{profile}}(\mathbf{\psi}_0)$.
4. Repeat this minimisation for every point across the 2D physics grid.

**Intuitive Visualization:** Imagine looking at a 3D mountain range where height represents $\chi^2$, the x-axis is physics parameter $\theta$, and the y-axis is nuisance parameter $\eta$. Profiling means walking along the x-axis ($\theta$) and looking along the y-axis ($\eta$) to find the **lowest valley point** at each position. You project the floor of the valley onto a 2D curve, ensuring your physics measurements automatically absorb the worst-case impact of systematic uncertainties!

---

## 7. Constructing & Interpreting Exclusion & Allowed Regions

In experimental physics, single number estimates (e.g., $\sin^2 2\theta = 0.86$) are meaningless without an uncertainty boundary. We present our results as **confidence regions** (2D closed loops called contours) on a parameter grid of $\Delta m^2$ vs $\sin^2 2\theta$.

A **$90\%$ Confidence Region** means that if we were to repeat the exact same experiment 100 times under identical conditions, our constructed contour loops would enclose the true, fundamental physical parameter values in approximately 90 of those 100 trials.

### Wilks' Theorem Approximation

In introductory statistics, a $1\sigma$ ($68.3\%$) confidence interval for a 1D Gaussian variable is found by moving outward from the minimum until the squared error increases by $\Delta \chi^2 = z^2 = 1.0^2 = 1.0$.

Wilks' Theorem[^11] extends this simple idea to multi-dimensional fits. It states that if you have a large dataset, the test statistic:

$$\Delta \chi^2(\mathbf{\psi}) = \chi^2_{\text{profile}}(\mathbf{\psi}) - \chi^2_{\text{profile}}(\hat{\mathbf{\psi}}_{\text{best}})$$

forms a multidimensional parabolic surface around the global best-fit point $\hat{\mathbf{\psi}}_{\text{best}}$.

To draw a contour boundary at a target Confidence Level (CL), we simply slice this 3D paraboloid at a constant height $\Delta \chi^2_{\text{crit}}$:

* **1D Fit ($d=1$, e.g., fitting only $\theta$):**
  * $68.27\% \text{ CL } (1\sigma)$: $\Delta \chi^2 \le 1.00$
  * $90.00\% \text{ CL}$: $\Delta \chi^2 \le 2.71$
  * $95.45\% \text{ CL } (2\sigma)$: $\Delta \chi^2 \le 3.84$
* **2D Fit ($d=2$, fitting both $\sin^2 2\theta$ and $\Delta m^2$):**
  * $68.27\% \text{ CL } (1\sigma)$: $\Delta \chi^2 \le 2.30$
  * $90.00\% \text{ CL}$: $\Delta \chi^2 \le 4.61$
  * $95.45\% \text{ CL } (2\sigma)$: $\Delta \chi^2 \le 6.18$

**The Topographic Map Analogy:** Think of $\Delta \chi^2(\mathbf{\psi})$ as a bowl-shaped landscape where the global minimum is the deepest point at height zero. Drawing a $90\%$ allowed contour is like flooding the bowl with water up to a height of $4.61$ units—the shoreline where water meets land defines your $90\%$ confidence boundary!

### Limits of Wilks' Theorem in Neutrino Physics

Wilks' theorem is an **asymptotic approximation**. It assumes the likelihood surface is a smooth, unbounded parabola. In neutrino oscillation searches, Wilks' theorem fails for three physics reasons:

1. **Physical Boundaries:** Quantum mechanics restricts mixing angles to $0 \le \sin^2(2\theta) \le 1$. If the true mixing angle is near maximum mixing ($\sin^2 2\theta \approx 1.0$), statistical noise cannot push the best-fit point above $1.0$. This "wall" truncates the parabola, making standard $\Delta \chi^2$ cutoffs incorrect.
2. **Non-linear Oscillations:** Neutrino probabilities depend on $\sin^2(1.27 \Delta m^2 L / E)$. Because of the sine-squared term, changing $\Delta m^2$ causes periodic, highly non-linear wiggles rather than a smooth parabola.
3. **Low Event Counts:** High-energy or appearance bins often contain zero or very few events, violating Gaussian normality.

Under these conditions, standard Wilks' cutoffs lead to **coverage problems**—a nominal $90\%$ contour might actually only cover the true value $80\%$ of the time (under-coverage) or $98\%$ of the time (over-coverage).

### The Feldman-Cousins Unified Approach

To restore exact statistical coverage near physical boundaries or in low-statistics searches, **Feldman and Cousins**[^12] introduced a method that replaces fixed Wilks' cutoffs (like $4.61$) with custom critical values $(\Delta \chi^2)_{\text{crit}}(\mathbf{\psi}_0)$ calculated specifically for every single point in physics parameter space.

#### Step-by-Step Feldman-Cousins Algorithm:

1. **Define Observed Difference:** At a specific grid point $\mathbf{\psi}_0 = (\sin^2 2\theta_0, \Delta m^2_0)$, compute the observed profile test statistic relative to the physical global minimum:

   $$\Delta \chi^2_{\text{obs}}(\mathbf{\psi}_0) = \chi^2_{\text{profile}}(\mathbf{\psi}_0) - \chi^2_{\text{profile}}(\hat{\mathbf{\psi}}_{\text{best}})$$

2. **Generate "Toy" Pseudo-Experiments (Monte Carlo Sampling):**
   Assuming $\mathbf{\psi}_0$ is the absolute truth, generate $N_{\text{toy}} \approx 10,000$ synthetic experimental datasets. For each bin $i$, sample a random integer from a Poisson distribution centered on the model prediction:

   $$N_{i, \text{toy}} \sim \text{Poisson}(\mu_i(\mathbf{\psi}_0, \hat{\mathbf{\eta}}_0))$$

   Vary systematic nuisance parameters according to their Gaussian calibration uncertainties.

3. **Fit Each Toy Dataset:**
   For each simulated toy dataset $m$:
   * Fit the toy data holding physics parameters fixed at $\mathbf{\psi}_0$ to find $\chi^2_{\text{profile}, m}(\mathbf{\psi}_0)$.
   * Fit the toy data allowing physics parameters to float freely across the physical domain ($0 \le \sin^2 2\theta \le 1$) to find its own best-fit minimum $\chi^2_{\text{profile}, m}(\hat{\mathbf{\psi}}_{\text{best}, m})$.
   * Calculate the toy test statistic:

     $$\Delta \chi^2_m(\mathbf{\psi}_0) = \chi^2_{\text{profile}, m}(\mathbf{\psi}_0) - \chi^2_{\text{profile}, m}(\hat{\mathbf{\psi}}_{\text{best}, m})$$

4. **Determine Custom Critical Cutoff:**
   Sort the 10,000 generated $\Delta \chi^2_m(\mathbf{\psi}_0)$ values in ascending order. Find the $90\text{th}$ percentile value (the 9,000th entry). This value is the custom critical threshold, $(\Delta \chi^2)_{\text{crit}}^{90\%}(\mathbf{\psi}_0)$.
   * Far from boundaries, $(\Delta \chi^2)_{\text{crit}}^{90\%} \approx 4.61$ (matching Wilks' Theorem).
   * Near physical boundaries ($\sin^2 2\theta \approx 1$), $(\Delta \chi^2)_{\text{crit}}^{90\%}$ can drop significantly (e.g., to $2.1$ or $3.0$).

5. **Construct the Final Contour Boundary:**
   Compare the real experimental result $\Delta \chi^2_{\text{obs}}(\mathbf{\psi}_0)$ against the custom cutoff $(\Delta \chi^2)_{\text{crit}}^{90\%}(\mathbf{\psi}_0)$:

   $$\text{If } \Delta \chi^2_{\text{obs}}(\mathbf{\psi}_0) \le (\Delta \chi^2)_{\text{crit}}^{90\%}(\mathbf{\psi}_0) \implies \mathbf{\psi}_0 \text{ is ALLOWED at } 90\% \text{ CL}$$

   $$\text{If } \Delta \chi^2_{\text{obs}}(\mathbf{\psi}_0) > (\Delta \chi^2)_{\text{crit}}^{90\%}(\mathbf{\psi}_0) \implies \mathbf{\psi}_0 \text{ is EXCLUDED at } 90\% \text{ CL}$$

Repeating this decision rule for every point across the 2D grid traces out the exact boundary line of the allowed parameter region.

---

## 8. Summary Workflow: Zero to Contour

| Step | Task & Statistical Tool |
| :--- | :--- |
| **1. Simulation** | Generate MC templates using GENIE + GEANT4. Apply reweighting for $\mathbf{\psi} = (\sin^2 2\theta, \Delta m^2)$. |
| **2. Validation** | Compare MC with calibration data using Pearson $\chi^2$ and K-S tests. |
| **3. Fit Model** | Define Poisson NLL $\chi^2_{\text{Poisson}}(\mathbf{\psi}, \mathbf{\eta})$ with systematic constraint terms. |
| **4. Minimisation** | Profile over nuisance parameters $\mathbf{\eta}$ to compute $\chi^2_{\text{profile}}(\mathbf{\psi})$ across a 2D grid. |
| **5. Critical Value** | Perform Feldman-Cousins toy sampling to compute $(\Delta \chi^2)_{\text{crit}}(\mathbf{\psi})$ for every grid point. |
| **6. Plot Contour** | Interpolate the threshold boundary $\Delta \chi^2_{\text{obs}}(\mathbf{\psi}) = (\Delta \chi^2)_{\text{crit}}(\mathbf{\psi})$ to draw confidence limits. |

---

## Footnotes

[^1]: B. Pontecorvo, "Neutrino Experiments and the Problem of Conservation of Leptonic Charge," *Zh. Eksp. Teor. Fiz.* **53**, 1717 (1967).
[^2]: Workman et al. (Particle Data Group), "Review of Particle Physics," *Prog. Theor. Exp. Phys.* **2022**, 083C01 (2022).
[^3]: K. Abe et al. (T2K Collaboration), "Constraint on the Matter-Antimatter Symmetry-Violating Phase in Neutrino Oscillations," *Nature* **580**, 339–344 (2020).
[^4]: C. Andreopoulos et al., "The GENIE Physics Model Root-based Event Generator," *Nucl. Instrum. Meth. A* **614**, 87–104 (2010).
[^5]: S. Agostinelli et al. (GEANT4 Collaboration), "GEANT4—a simulation toolkit," *Nucl. Instrum. Meth. A* **506**, 250–303 (2003).
[^6]: F. James, *Statistical Methods in Experimental Physics*, 2nd ed. (World Scientific, 2006).
[^7]: K. Pearson, "On the criterion that a given system of deviations from the probable in the case of a correlated variable is such that it can be reasonably supposed to have arisen from random sampling," *Philos. Mag.* **50**, 157–175 (1900).
[^8]: A. Kolmogorov, "Sulla determinazione empirica di una legge di distributione," *G. Ist. Ital. Attuari* **4**, 83–91 (1933).
[^9]: S. Baker and R. D. Cousins, "Clarification of the Use of Chi-Square and Likelihood Functions in Fits to Histograms," *Nucl. Instrum. Meth.* **221**, 437–442 (1984).
[^10]: G. Cowan, K. Cranmer, E. Gross, and O. Vitells, "Asymptotic formulae for likelihood-based tests of new physics," *Eur. Phys. J. C* **71**, 1554 (2011).
[^11]: S. S. Wilks, "The Large-Sample Distribution of the Likelihood Ratio for Testing Composite Hypotheses," *Ann. Math. Statist.* **9**, 60–62 (1938).
[^12]: G. J. Feldman and R. D. Cousins, "A Unified approach to the classical statistical analysis of small signals," *Phys. Rev. D* **57**, 3873–3889 (1998).
```

I have converted the entire document into clean Markdown. All LaTeX math notation has been mapped to standard `$ ... $` for inline math and `$$ ... $$` for display equations, and all citations have been converted to native Markdown footnotes (`[^1]`).