### Elastic Energies

To simulate discrete elastic shells, we use the StVK model for in-plane tension and compression, along with a hinge-based bending energy suitable for both planar and non-planar rest shapes. Below, we provide the formulas used in our implementation.

In-plane energy
$$
E_{\mathrm{stretching}} = k_s A ((1 - \mu) ||\mathbf{E}||_2 + 
\mu \  \text{tr}(\mathbf{E})^2) \ ,
$$
where $\mathbf{E}$ is the Green strain tensor and $A$ is the undeformed triangle area.

The in-plane stiffness $k_s$ is computed from the shell thickness $h$, Young's modulus $E$, and Poisson's ratio $\mu$, as follows:
$$
k_s = \frac{E h}{1.0 - \mu^2} \ .
$$

Bending energy

$$
E_{\mathrm{bending}} = k_b L (\theta - \theta_0)^2 \ ,
$$

where $L$ represents the undeformed length of the hinge computed from the area of the parallelograms formed by the two adjacent triangles.

The bending stiffness $k_b$ is calculated using:
$$
k_b = \frac{E h^3}{24 (1.0 - \mu^2)} \ .
$$

### Gravity 

The gravitational potential energy per triangle is computed as:
$$
E_{\mathrm{gravity}} = A \rho h g c_y 
$$
where $\rho$ is the density, $g$ is gravitational acceleration, and $c_y$ is the vertical ($y$) position of the triangle centroid.