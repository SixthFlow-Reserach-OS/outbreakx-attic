# SEIR Model Simulator

## Overview
A robust implementation of the SEIR (Susceptible-Exposed-Infectious-Recovered) epidemiological model for simulating infectious disease dynamics. This mathematical model uses coupled differential equations to track disease progression through population compartments, providing insights into epidemic patterns and intervention effectiveness.

## Features
- Advanced SEIR compartmental modeling
- Customizable epidemiological parameters
- Real-time visualization of disease dynamics
- Detailed population compartment tracking (S, E, I, R)
- CSV export of simulation results
- Parameter sensitivity analysis
- Basic reproduction number (R0) calculation

## Requirements
- Python 3.7+
- Dependencies:
  - NumPy >= 1.20.0
  - SciPy >= 1.7.0
  - Matplotlib >= 3.4.0
  - Pandas >= 1.3.0

## Installation
```bash
# Clone the repository
git clone https://github.com/username/seir-simulator.git
cd seir-simulator

# Create and activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Quick Start
```python
from seir_model import SEIRModel

# Initialize the model with parameters
model = SEIRModel(
    beta=0.3,    # Infection rate
    sigma=0.2,   # Incubation rate (1/latent period)
    gamma=0.1,   # Recovery rate (1/infectious period)
    N=10000,     # Total population size
    E0=100       # Initial exposed population
)

# Run simulation
results = model.simulate(days=100)
model.plot_results()
```

## Model Parameters
| Parameter | Description | Typical Range |
|-----------|-------------|---------------|
| β (beta)  | Infection rate | 0.2 - 0.5 |
| σ (sigma) | Incubation rate | 0.1 - 0.3 |
| γ (gamma) | Recovery rate | 0.05 - 0.2 |
| N         | Population size | Any positive integer |

## Output
The simulation provides:
- Interactive time-series plots of all compartments
- CSV export of daily counts
- Basic reproduction number (R0) estimates
- Peak infection timing and magnitude
- Epidemic duration estimates

## Documentation
Detailed documentation is available in the `/docs` directory:
- [Model Mathematics](docs/model.md)
- [API Reference](docs/api.md)
- [Examples](docs/examples.md)

## Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request