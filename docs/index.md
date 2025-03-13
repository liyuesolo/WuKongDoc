![GitHub](https://img.shields.io/github/license/liyuesolo/Wukong2024?style=flat-square)
![Travis (.com)](https://img.shields.io/travis/com/liyuesolo/Wukong2024?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/liyuesolo/Wukong2024?style=flat-square)

# WuKong Simulation

WuKong is an extremely light-weight and modular simulation codebase for different type of discretizations commonly used in computer graphics.

## Why WuKong
The code might not be the most efficient or best-written, as it’s a research codebase developed by an individual. So, why WuKong? The computer graphics community is incredible and champions open-source development. Many projects showcased at Siggraph can be reproduced by those new to graphics. However, for a beginner—or someone from a different field who just wants to see a wobbly sphere moving on the screen—a full-fledged Siggraph codebase might be overkill. In fact, it often requires significant effort to strip away all the advanced features to achieve a basic implementation.

WuKong offers a solution by providing minimal code for simulating some of the most fundamental models in graphics. Another common challenge is compilation. Many codebases are designed to simulate a wide range of phenomena, meaning you may need to compile all the relevant libraries. Although a proper CMake setup can simplify this process, integrating such simulations into another project, like in reinforcement learning, benefits from having fewer dependencies. With this goal in mind, each project in WuKong is self-contained. To compile a single project, you don’t have to compile everything else, and you can simply extract the subfolder without worrying about breaking dependencies.

## WuKong Projects

WuKong support simulation of 

[Discrete Elastic Shell](./projects/discrete-shell.md).

[Discrete Elastic Rods](./projects/discrete-shell.md).

[Linear Tetrahedral Finite Elements](./projects/discrete-shell.md).

[Quadratic Tetrahedral Finite Elements](./projects/discrete-shell.md).

[Differentiable Geodesic Distance](./projects/discrete-shell.md).

[Eulerian-on-Lagrangian Rods](./projects/discrete-shell.md).

## How to Compile
We provide a docker image for you to run our code on an arbirary Linux machine. Please check out the [Docker](./projects/docker.md) section to see how to set it up.

## Simulation Basics
WuKong implements optimization-based Newton solver with backtracking line search. To reduce the learning curve of adapting different simulation projects. All projects follow identical pipeline with major functions with the same names. You can find more information in [Newton's Method](./projects/Newtons-method.md) and [Time Stepping](./projects/time-stepping.md)

## Create YOUR Project
We prepare a simple script to generate a new project in the Project folder that runs with a viewer. Please refer to [New Project](./projects/new-project.md) to learn more.

---
Author: [Yue Li](https://liyuesolo.github.io/)

If WuKong contributes to an academic publication, cite it as:
```bib
@misc{wukong,
  title = {WuKong},
  author = {Yue Li and others},
  note = {https://github.com/liyuesolo/Wukong2024},
  year = {2024}
}
```
Development of this software was funded in part by the European Research Council (ERC) under the European Union’s Horizon 2020 research and innovation program (grant agreement No. 866480), and the Swiss National Science Foundation through SNF project grant 200021\_200644. Our implementation benefits from discussion and references from Juan Montes, Simon Dünser and Jonas Zehder.