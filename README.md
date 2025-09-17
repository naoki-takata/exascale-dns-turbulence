# Exascale DNS: Turbulence Direct Numerical Simulation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-1.9+-red.svg)](https://pytorch.org/)

## Overview

This project implements a 2D Direct Numerical Simulation (DNS) of turbulence using the pseudo-spectral method in Python. Designed for educational and research purposes, it simulates the Navier-Stokes equations to study turbulent flow phenomena with a focus on exascale-ready computational techniques. The code runs on Google Colab with GPU support, offering a scalable foundation for understanding turbulence physics and numerical methods.

### Key Features
- Visualization of vorticity fields and energy spectra
- Adjustable Reynolds number (Re)
- GPU acceleration with PyTorch
- Educational code structure optimized for learning

### Target Audience
- Beginners in fluid dynamics
- Students
- Researchers interested in computational fluid dynamics (CFD) and exascale computing

### License
MIT License (open-source, freely modifiable)

## What You Can Learn

### Fluid Dynamics Basics
- Understanding turbulence, vorticity, and Reynolds number
- Energy cascades (e.g., 2D reverse cascade $E(k) \sim k^{-3}$)
- Physical phenomena in 2D turbulence

### Numerical Methods
- Pseudo-spectral method implementation
- Runge-Kutta 4th-order time integration
- Fourier transform applications

### Programming Skills
- Python experience (NumPy, SciPy, Matplotlib, PyTorch)
- GPU parallelization techniques

### Exascale Computing
- Scalability concepts
- Preparation for 3D DNS ($10^{12}$ grid points)

### Data Analysis
- Energy spectrum analysis
- Turbulent structure visualization

## Installation

### Clone the Repository
```bash
git clone https://github.com/yourusername/exascale-dns-turbulence.git
cd exascale-dns-turbulence
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Required Packages
- numpy
- scipy
- matplotlib
- torch

## Usage

### Running on Google Colab
1. Open `dns_turbulence.ipynb` in Google Colab
2. Enable GPU: Runtime > Change runtime type > Select GPU
3. Run all cells to execute turbulence simulation and visualization

### Parameter Adjustment
- `nu`: Adjust Reynolds number (Re = 1/nu)
- `Nx, Ny`: Change grid resolution
- `n_steps`: Number of simulation steps
- `dt`: Time step size

## Results and Analysis

### Vorticity Field
- Displays the evolution of vorticity (e.g., Step 900, Re ≈ 10,000)
- Shows complex vortex interactions and fine-scale structures
- Visualizes characteristic turbulent patterns

### Energy Spectrum
- Plots $E(k)$ vs. $k$ (log-log scale)
- Reveals $k^{-3}$ slope typical of 2D turbulence
- Shows energy dissipation at high wavenumbers due to resolution limits (128×128 grid)

### Physical Insights
- Demonstrates energy reverse cascade in 2D
- Contrasts with 3D Kolmogorov $k^{-5/3}$ law

## Real-World Applications

This DNS technique is applied in various fields:

### Aerospace
- Optimizing aircraft aerodynamics and reducing jet noise (NASA, JAXA)

### Weather Forecasting
- Improving typhoon and rainfall predictions (ECMWF)

### Automotive
- Enhancing vehicle fuel efficiency (Toyota, Tesla)

### Ocean Engineering
- Designing offshore wind turbines (Hywind)

### Medical Engineering
- Analyzing blood flow for stent design (NIH)

### Industrial Processes
- Optimizing chemical reactors (BASF)

### Disaster Mitigation
- Simulating floods and tsunamis (Japan's NIED)

Exascale computing enables high-Reynolds number (10^6+) simulations, bridging small-scale turbulence to global-scale models.
## Limitations and Future Work

### Current Limitations
- **2D Limitation**: Lacks 3D vortex stretching; requires 3D extension with increased grid size and MPI
- **Resolution**: 128×128 grid insufficient for Re = 10,000; consider 256×256 or de-aliasing
- **Computational Efficiency**: Optimization needed for larger-scale simulations

### Future Enhancements
- Add forcing terms
- Compute enstrophy spectrum
- Integrate with AI for real-time prediction
- Extend to 3D DNS

## Contributing

Feel free to fork this repository, modify the code, and submit pull requests. We welcome documentation additions and extensions to 3D DNS for exascale applications. For issues, please use the GitHub Issues tab.

## Acknowledgments

Inspired by advancements in exascale computing and turbulence research. Thanks to the open-source community for tools like PyTorch and Colab.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
