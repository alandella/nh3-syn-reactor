# NH3 Synthesis Reactor

## General Overview
This project models a one-dimensional, pseudo-homogeneous plug flow reactor (PFR) for ammonia synthesis. The primary code lives in a Jupyter notebook that gathers thermodynamic properties, reaction kinetics, and data for industrial catalysts.

## Repository Structure
- **docs/** – reference material, including a Kellogg patent for industrial context
- **source/** – contains the `nh3_reactor.ipynb` notebook, which runs the simulation

## Key Components of the Notebook
- **Imports and dependencies**: NumPy, SciPy (`optimize` and `integrate`), Matplotlib, and CoolProp for physical properties
- **`calc_rct_model` function**: formulates material, energy, and momentum balances, returning derivatives with respect to reactor volume
- **`calc_rct` function**: integrates the equations along the reactor volume with `scipy.integrate.odeint`, yielding conversion, temperature, and pressure profiles

## Suggestions for Further Learning
1. **SciPy ODE solving & optimization** – explore `odeint` and functions in `scipy.optimize` (e.g., `brenth`, `minimize_scalar`) to understand how the reactor equations are solved
2. **CoolProp and thermodynamic properties** – study how the library computes molar masses, heat capacities, and viscosities
3. **Code organization** – consider breaking the notebook into reusable Python modules and adding automated tests
4. **Chemical engineering fundamentals** – revisit mass and energy balances, ammonia kinetics, and transport phenomena to extend the model (e.g., to 2-D or 3-D reactors or more detailed heat transfer)

## Contributing and Improvements

*Contributing and redistributing the code is free!*

You may choose to modify and improve it to your liking. 

## Authors

* **Andrea Giuseppe Landella** - [alandella](https://github.com/alandella)

## License

This project is licensed under The MIT License - see the [LICENSE.md](https://github.com/alandella/nh3-syn-reactor/blob/main/LICENSE) file for details.
