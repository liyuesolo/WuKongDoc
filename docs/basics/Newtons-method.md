We use Newton's method for simulation. All projects contains the following functions which are used for minimizing simulation objective using Newton's method.

```cpp

    // compute total energy
    T computeTotalEnergy();

    // compute system residual i.e. the negative gradient of the total energy
    T computeResidual(VectorXT& residual);

    // compute the second derivative of the total energy
    void buildSystemMatrix(StiffnessMatrix& K);

    // Newton step with line search
    T lineSearchNewton(const VectorXT& residual);

    // solve a linear system of equations Kdu = f
    bool linearSolve(StiffnessMatrix& K, const VectorXT& residual,
                     VectorXT& du);
```