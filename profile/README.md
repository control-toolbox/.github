# Welcome to the control-toolbox ecosystem!

## Documentation

The control-toolbox ecosystem regroups `Julia` packages. The root package is [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl) which aims to provide tools to solve optimal control problems by direct and indirect methods. 

An optimal control problem in general form may be written:
```math
\begin{array}{ll}
\mathrm{minimize} & \displaystyle J(t_0, t_f, x, u, \lambda) = g(t_0, x(t_0), t_f, x(t_f), \lambda) + \int_{t_0}^{t_f} f^{0}(t, x(t), u(t), \lambda) ~\mathrm{d}t \\[0.5em]
\mathrm{subject~to} &  \\[0.5em]
& \dot{x}(t) = f(t, x(t), u(t), \lambda)  \\[1em]
& \xi_l \le \xi(t, u(t), \lambda) \le \xi_u  \\[0.5em]
& \psi_l \le \psi(t, x(t), u(t), \lambda) \le \psi_u  \\[0.5em]
& \phi_l \le \phi(t_0, x(t_0), t_f, x(t_f), \lambda) \le \phi_u
\end{array}
```

The packages [PathFollowing.jl](https://github.com/control-toolbox/PathFollowing.jl) and [HamiltonianFlows.jl](https://github.com/control-toolbox/HamiltonianFlows.jl) are independent and provide respectively path following methods and flows from Hamiltonian functions and systems. 

[![](https://img.shields.io/badge/doc-OptimalControl.jl-blue)](https://control-toolbox.github.io/OptimalControl.jl)
[![](https://img.shields.io/badge/doc-PathFollowing.jl-blue)](https://control-toolbox.github.io/PathFollowing.jl)
[![](https://img.shields.io/badge/doc-HamiltonianFlows.jl-blue)](https://control-toolbox.github.io/HamiltonianFlows.jl)

## Installation

To install a package from the control-toolbox ecosystem, you must add its registry into you `Julia` configuration.
```shell
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.8.2 (2022-09-29)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia> ]
pkg> registry add https://github.com/control-toolbox/ct-registry.git
     Cloning registry from "https://github.com/control-toolbox/ct-registry.git"
       Added registry `ct-registry` to `~/.julia/registries/ct-registry`
```

Then, you can install any package as usual. For instance:
```shell
pkg> add OptimalControl
```

## Discussion

We discuss about the control-toolbox ecosystem here:
[![Github Issues](https://img.shields.io/github/issues-search?color=green&label=open%20issues&query=is%3Aopen%20is%3Aissue%20user%3Acontrol-toolbox%20archived%3Afalse)](https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+)
[![GitHub Discussions](https://img.shields.io/github/discussions/control-toolbox/control-toolbox.github.io?color=green)](https://github.com/orgs/control-toolbox/discussions)
[![](https://img.shields.io/badge/wiki-ct-green)](https://github.com/control-toolbox/control-toolbox.github.io/wiki)

## Setup

The [setup](https://github.com/orgs/control-toolbox/repositories?type=all) of the control-toolbox ecosystem is the following:

* [ct-registry](https://github.com/control-toolbox/ct-registryb): the control-toolbox registry since the packages are not yet available in the [official registry](https://github.com/JuliaRegistries/General).
* [CTBase.jl](https://github.com/control-toolbox/CTBase.jl): fundamentals of the control-toolbox ecosystem
* [CTDirect.jl](https://github.com/control-toolbox/CTDirect.jl): direct transcription of an optimal control problem and resolution
* [CTDirectShooting.jl](https://github.com/control-toolbox/CTDirectShooting.jl): direct shooting transcription of an optimal control problem and resolution
* [CTProblemLibrary.jl](https://github.com/control-toolbox/CTProblemLibrary.jl): library of optimal control problems
* [HamiltonianFlows.jl](https://github.com/control-toolbox/HamiltonianFlows.jl): Hamiltonian flows
* [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl): main package
* [PathFollowing.jl](https://github.com/control-toolbox/PathFollowing.jl): path following methods
