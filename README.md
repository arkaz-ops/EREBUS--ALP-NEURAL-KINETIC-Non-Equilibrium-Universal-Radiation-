# EREBUS--ALP-NEURAL-KINETIC-Non-Equilibrium-Universal-Radiation-
A high-precision numerical framework for solving non-equilibrium ALP cosmology. Implements exact momentum-dependent Boltzmann equations for lepton/photon couplings, calibrated against Planck, ACT, and DESI DR2 datasets
EREBUS-ALP: NEURAL-KINETIC Framework
​Advanced Numerical Solver for Non-Equilibrium Axion-Like Particle (ALP) Cosmology
​ Technical Synopsis
​EREBUS-ALP is a high-fidelity scientific framework designed to solve the momentum-dependent Boltzmann Equation for light Axion-Like Particles (ALPs) coupled to the Standard Model (SM) leptons and photons.
​The core sub-system, NEURAL-KINETIC, moves beyond the standard "Fluid Approximation" (thermal equilibrium) by implementing an exact treatment of non-thermal phase-space distributions. This allows for precise mapping of spectral distortions in the Cosmic Microwave Background (CMB) and Big Bang Nucleosynthesis (BBN) observables.
​ Key Scientific Novelties
​Exact Phase-Space Mapping: Implementation of non-thermal distributions obtained by solving the collision integral C[f] without prior assumptions of a thermal spectrum.
​Prior Sensitivity Optimization: Optimized for MCMC analysis by sampling over \Delta N_{eff} rather than \log_{10} f_a, ensuring data-driven constraints (Planck + ACT + SPT + DESI DR2).
​UV-Dominated Production: Specialized solvers for Primakoff production at initial temperatures T_{in} \geq 10^3 GeV.
​Multi-Channel Coupling: Dedicated modules for Electron (e), Muon (\mu), and Tau (\tau) decay and scattering channels.
​ Mathematical Foundation
​The framework solves the generalized 2 \to 2 collision integral as defined in high-energy kinetic theory:

C[f_1, f_2, f_3] = \frac{1}{2E_k} \int d\Pi_1 d\Pi_2 d\Pi_3 (2\pi)^4 \delta^{(4)}(P_1 + P_2 - P_3 - K) |M|^2 f_1 f_2 (1 \mp f_3)
Where |M|^2 is the channel-specific Matrix Element, consistently propagated into cosmological observables using vectorized momentum grids.

Cosmological Bounds & Forecasts
The engine is calibrated against state-of-the-art cosmological data, providing 95% CL limits:
ALP-Lepton Constraints: f_a > 1.63 \times 10^6 GeV (e), 9.41 \times 10^6 GeV (\mu), 8.06 \times 10^4 GeV (\tau).
ALP-Photon Coupling: g_{a\gamma} < 1.98 \times 10^{-8} GeV$^{-1}$.
Next-Gen Sensitivity: Pre-configured for LiteBIRD, Simons Observatory, and CMB-HD benchmarks, targeting \Delta N_{eff} \simeq 0.01 - 0.03.
 Implementation Details
Language: Python 3.10+
Dependencies: NumPy, SciPy (Quadrature & ODE solvers), Matplotlib.
Core Logic: Sovereign Non-thermal Offset (SNO) algorithm for high-momentum convergence.
This framework represents a robust treatment of ALP cosmology for high-precision CMB measurements, ensuring theoretical uncertainties remain under controlled numerical thresholds.
