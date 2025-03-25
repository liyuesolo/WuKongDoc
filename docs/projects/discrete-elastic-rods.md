To allow for sparse energy Hessian, we adopt the time-parallel transport strategy proposed by Bergou et al., where for each rod segment, in addition to the twist angle, we further track a reference twist with respect to the reference frame.

The stretching energy is fairly straightforward and can be computed as
\begin{equation}
E_{\mathrm{stretch}} = \frac{1}{2} k_s \sum_{i=0}^{N}\frac{1}{L_i}(l_i - L_i)^2
\end{equation}

To compute the bending and twisting energy for two adjacent segments,
\begin{equation}
E_{\mathrm{bend}} = \frac{1}{2} \sum_{i=1}^{N} \frac{1}{L_{vi}} (\boldsymbol{\kappa}_i - \tilde{\boldsymbol{\kappa}}_i)^{T} \mathbf{B} (\boldsymbol{\kappa} - \tilde{\boldsymbol{\kappa}}_i) \ ,
\end{equation}
where $\boldsymbol{\kappa}$ is the material curvature and $\mathbf{b}$ is a constant diagonal stiffness matrix. Here, $L_{vi}$ is the Voronoi edge length computed from the two adjacent edges, i.e. $L_{vi} = \frac{1}{2}(|\mathbf{x}_i - \mathbf{x}_j| + |\mathbf{x}_i - \mathbf{x}_k|)$

To compute $\boldsymbol{\kappa}$, we first compute the curvature binormal from the two tangent vectors of the two adjacent edges for vertex $i$ following
$\kappa\mathbf{b}_i = \frac{2\mathbf{t}_{i1} \times \mathbf{t}_{i2}}{1 + \mathbf{t}_{i1} \cdot \mathbf{t}_{i2}} \ .

We then compute the discrete material curvature using curvature binormal and the adapted frames following

\begin{equation}
    \boldsymbol{\kappa}_i = [\kappa \mathbf{b}_i \cdot \frac{ \mathbf{b}_{i1} + \mathbf{b}_{i2}}{2}, \kappa \mathbf{b}_i \cdot \frac{ \mathbf{n}_{i1} + \mathbf{n}_{i2}}{2}]^{T} \ ,
\end{equation}

where $\mathbf{b}$ and $\mathbf{n}$ are the normal and binormal vectors of the adapted frame. The adapted frames are computed using parallel transport.
\begin{equation}
    E_{\mathrm{twsit}}  =  \frac{1}{2} k_t \sum_{i=1}^{N} \frac{1}{L_i}(m_i - \tilde{m}_i)^2
\end{equation}

The twist for a given vertex $i$ can be computed as
\begin{equation}
    m_i  = \theta_{i2} - \theta_{i1} + \bar{m_i} + \theta_i \ ,
\end{equation}
where $\theta_{i1}$ and $\theta_{i2}$ are the rest angle for the two segments connected to vertex $i$. Furthermore, $\bar{m_i}$ and $\theta_i$ are the reference twist and the change of the reference twist.