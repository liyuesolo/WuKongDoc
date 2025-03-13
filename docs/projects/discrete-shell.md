To simulate discrete elastic shells, we use StVK model for in-plane tension and compression, and a hinge-based bending energy that allows for both planar and non-planar rest shape.

Here, we provide the formula used in our implmentation

In plane energy
$$
E_{\mathrm{stretching}} = k_s 
$$

Bending energy

$$
E_{\mathrm{bending}} = k_b L (\theta - \theta_0)^2 \ ,
$$

where $L$ computes the undeformed length of the hinge over the area of the two parallelgram formed by the two adjacent trianlges.

How to compute $k_b$? 
