We use variational implicit Euler for dynamic time stepping and solve for end-of-time-step position $\mathbf{x}_t$
$$ 
E_{\mathrm{total}} = E_{\mathrm{inertia}} + E_{\mathrm{elastic}} + E_{\mathrm{external}} + E_{\mathrm{contact}} \ , 
$$
where the inertial energy is computed as
$$
E_{\mathrm{inertia}} = \frac{1}{2} (x_t - 2_{t-1} + x_{t-2})^{T} \mathbf{M} (x_t - 2x_{t-1} + x_{t-2}) \ .
$$

The energy corresponding to constant external forces $\mathbf{f}$ is simply
$E_{\mathrm{external}} = \mathbf{f}^{T} \mathbf{x}_t \ .$

The formula for elastic energy can be found in the [projects](../projects).

We use the contact potential from [IPC](https://ipctk.xyz/).