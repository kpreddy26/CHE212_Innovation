# CHE212 Innovation Project
# Natural Convection Analysis of Enhanced Cylindrical Fins

An experimental study evaluating the thermal performance, temperature distribution, and phase-change material (PCM) dynamics of solid and wax-filled cylindrical aluminum fins under natural convection.

## Project Objectives
* **Compare Performance:** Evaluate and compare the heat transfer profiles of a conventional solid fin and a wax-filled phase-changing material (PCM) fin.
* **Measure Temperature Distribution:** Map spatial temperature gradients along the fin lengths from base to tip using multi-node thermocouple tracking.
* **Calculate Thermal Metrics:** Determine heat transfer rates ($Q_{\text{fin}}$), fin efficiency ($\eta_f$), and fin effectiveness ($\epsilon_f$) to assess system performance.
* **Analyze Transient Dynamics:** Characterize the heating curves, steady-state benchmarks, and cooling rates influenced by latent heat buffering.

## Experimental Specifications
* **Fin Geometry:** Aluminum rods with a length ($L$) of approximately $180\text{ mm}$ and an outer diameter ($d$) of $10\text{ mm}$.
* **Thermal Mediums:** Solid aluminum core versus a hollowed aluminum rod filled with candle wax (Phase Change Material) possessing a melting point of $\sim 55^{\circ}\text{C}$.
* **Heater & Power Supply:** $12\text{V DC}$ Cartridge heating element situated at the fin base, powered by a constant voltage DC supply source.
* **Analytical Instrument System:** Five K-type thermocouples ($\text{T1}$ to $\text{T5}$) paired with an Arduino data logger setup tracking temperatures at regular time intervals ($30\text{ s}$ initially, then every $2\text{ min}$) until a steady state is verified.

## Theoretical Framework
The temperature distribution and steady-state thermal behavior along an extended surface are governed by the classical one-dimensional fin differential equation:

$$\frac{d^{2}\theta}{dx^{2}}-m^{2}\theta=0$$

Where:
* $\theta = T(x) - T_{\infty}$ represents the excess temperature relative to the ambient air ($T_{\infty}$).
* $m = \sqrt{\frac{hP}{kA_c}}$ is the empirical fin parameter computed using a convective heat transfer coefficient ($h$), perimeter ($P$), material thermal conductivity ($k = 205\text{ W/m}\cdot\text{K}$), and cross-sectional area ($A_c$).

Assuming an insulated tip boundary condition ($\frac{d\theta}{dx}\big|_{x=L} = 0$), the absolute temperature distribution profile simplifies to:

$$\frac{\theta(x)}{\theta_b} = \frac{\cosh[m(L-x)]}{\cosh(mL)}$$

The true thermal output dissipated by the fin matrix is evaluated via:

$$Q_{\text{fin}} = \sqrt{hPkA_c} \,\theta_b \tanh(mL)$$

---

## Key Results
* **Fin Efficiency ($\eta_f$):** $\approx 83\%$ for both solid and PCM configurations (independent of filling since it relies on outer geometry and $h$).
* **Fin Effectiveness ($\epsilon_f$):** $\approx 60$ for both models, demonstrating a massive enhancement over an un-finned base plane.
* **Steady-State Base Temperatures ($T_1$):** Solid fin stabilized at $80.7^{\circ}\text{C}$ vs. the wax-filled fin stabilizing at a higher $88.5^{\circ}\text{C}$ due to the higher internal thermal resistance of the core.
* **Latent Heat Transition Block:** The wax-filled fin exhibited a prominent thermal plateau in the $50\text{--}55^{\circ}\text{C}$ range, reflecting latent heat absorption during melting and resulting in a $\sim 13\%$ longer total cooling window.

## Conclusion
The study validates that embedding a Phase Change Material (PCM) inside extended surfaces does not enhance steady-state heat dissipation rates, but instead acts as a powerful distributed thermal buffer. The localized latent energy release suppresses rapid temperature fluctuations and enforces thermal regulation, proving highly valuable for transient load setups such as electronics cooling and battery thermal management.
