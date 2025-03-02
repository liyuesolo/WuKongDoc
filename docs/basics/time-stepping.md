We use variational implicit Euler for dynamic time stepping
$$ 
E_{\mathrm{total}} = E_{\mathrm{inertia}} + E_{\mathrm{elastic}} + E_{\mathrm{external}} + E_{\mathrm{contact}} \ , 
$$
where
$$
E_{\mathrm{inertia}} = \frac{1}{2}(x_t - 2x_{t-1} + x_{t-2})^{T} M (x_t - 2x_{t-1} + x_{t-2})
$$