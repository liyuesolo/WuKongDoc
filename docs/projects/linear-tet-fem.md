### Elastic Energy

WuKong implements StVK and Neohookean energy models

\begin{equation}
    E_{\mathrm{StVK}} = V \  \frac{\lambda}{2}||\mathrm{E}||^2 + \mu \text{tr}(\mathbf{E}) \ ,
\end{equation}

\begin{equation}
    E_{\mathrm{NH}} = V \  \frac{\mu}{2}( \text{tr}(\mathbf{F}^T)\mathbf{F} - 3.0 - 2.0 \log(\det(\mathbf{F}))) + \frac{\lambda}{2} \log(\det(\mathbf{F}))^2
\end{equation}

where $\mathbf{F}$ is the deformation gradient, $\mathbf{E}$ is Green strain, $\lambda$ and $\mu$ are Lame parameters, and $V$ is the undeformed volume.

