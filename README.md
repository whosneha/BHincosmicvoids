# Black Holes in Cosmic Voids: Plotting and Analysis

This repository provides a set of Python tools for studying black holes in cosmic voids, based on the paper **Black Holes in Cosmic Voids** by Lustosa et al. (2025). The goal of this project is to allow users to test and explore the physical concepts presented in the paper, including the mass accumulation, horizon formation, Hawking temperature, entropy, and the effect of various parameters on the black hole's environment within cosmic voids.

The tool allows for the computation and visualization of key physical quantities related to black holes and cosmic filaments. It uses theoretical models for density profiles, mass accumulation, and horizon formation in voids to generate insightful plots that reiterate the key points from the paper. Users can modify parameters, visualize data, and experiment with different conditions in a flexible and accessible way.

## Paper Reference

This tool is based on the paper:

**Lustosa et al. (2025), Black Holes in Cosmic Voids**. The models used in this project are directly inspired by the theoretical concepts presented in this paper, which explores black holes' behavior in the underdense regions of the universe, particularly focusing on cosmic voids. The paper discusses the formation of black holes in these regions, their associated thermodynamics, and the effects of various parameters on the formation of black hole horizons.


## Features
- **Mass Function**: Computes the mass within a given radius for a cosmic void using an analytic density profile.
- **Horizon Condition Function**: Plots the horizon formation function based on mass and radius.
- **Hawking Temperature**: Plots the Hawking temperature at different radii, demonstrating the effect of cosmic void properties on black hole physics.
- **Black Hole Entropy**: Calculates the entropy associated with black holes as a function of the horizon radius.

## Plots
The tool allows users to generate various plots based on the theoretical model. These plots are useful for exploring the physical concepts discussed in the paper and testing different assumptions.

### 1. **'temp' and 'entropy'**
- **What it shows**: These plots display the **Hawking temperature** and **entropy** of a black hole as a function of its radius for different contrast parameter values ($$\delta_c$$).
- **Purpose**: This helps to visualize how the temperature and entropy of black holes change as a function of their size, which is critical for understanding the thermodynamics of black holes in cosmic voids.

### 2. **'density'**
- **What it shows**: This plot shows the **density profile** $
ho(r)$ for multiple values of the contrast parameter ($\delta_c$). A dashed line represents the baseline density $
ho_0$.
- **Purpose**: It illustrates how density changes with radius, as well as how different values of $\delta_c$ affect the density profile in cosmic voids.

### 3. **'f_fixed_mass'**
- **What it shows**: This plot represents the **horizon condition function** $$f(r) = 1 - $\frac{2M}{r}$ for a fixed mass $M$ (e.g., $M = 10$).
- **Purpose**: It helps to understand where the horizon might form, given a specific mass, and is useful for studying potential regions of horizon formation.

### 4. **'critical_mass'**
- **What it shows**: This plot shows the **mass required** to form a horizon at each radius, specifically plotting $M(r)$ such that $f(r) = 0$.
- **Purpose**: This is crucial for understanding the conditions under which a black hole’s event horizon forms, based on the mass distribution in the cosmic void.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/black-holes-in-cosmic-voids.git
   cd black-holes-in-cosmic-voids
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the `main()` function with different parameters to generate plots. For example:

   ```python
   main(plots=('temp', 'density'))
   ```

   This will generate plots of Hawking temperature and density profiles for different $$\delta_c$$ values.

4. Modify the parameters in the `main()` function to test different physical setups, such as adjusting the scale radius $$r_s$$, virial radius $$r_v$$, contrast parameter $$\delta_c$$, and the mass for horizon formation.


## Example Usage

Here’s an example usage of the `main()` function to plot Hawking temperature and density profiles:

```python
# Basic usage for Hawking temperature and density profiles:
main(plots=('temp', 'density'))

# Mass horizon function for fixed M = 10:
main(plots=('f_fixed_mass',), r_s=80, r_v=100, rho_o=3e-5,
     delta_c_values=[-0.90, -0.95, -0.99], r_range=(0.1, 80), r_points=300)

# Plot critical mass required to form horizons at different radii:
main(plots=('critical_mass',), r_s=80, r_v=100, rho_o=3e-5,
     delta_c_values=[-0.90], r_range=(0.1, 150))
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

We hope this tool helps you explore and understand the fascinating phenomena of black holes in cosmic voids. Feel free to contribute, modify, and extend the code as needed for your research!
