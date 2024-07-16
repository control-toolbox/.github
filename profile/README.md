# Welcome to control-toolbox!

The control-toolbox ecosystem gathers &nbsp;
<a href="https://julialang.org">
 <img src="https://raw.githubusercontent.com/JuliaLang/julia-logo-graphics/master/images/julia.ico" width="16em">
 Julia
</a> &nbsp; packages for mathematical control and applications. 

The root package is [`OptimalControl.jl`](https://github.com/control-toolbox/OptimalControl.jl) which aims to provide tools to modelise and solve optimal control problems by direct and indirect methods.

> [!TIP]
> From the [documentation](http://control-toolbox.org/OptimalControl.jl), you can find tutorials to define and solve optimal control problems with the `OptimalControl.jl` package. 

See also some applications of the `OptimalControl.jl` package:

- [Examples from calculus of variations](https://control-toolbox.org/calculus_of_variations)
- [Optimal control in Medical Resonance Imaging](https://control-toolbox.org/mri)
- [Orbit transfer from space mechanics](https://control-toolbox.org/kepler)

## Documentation

Please visit our [webpage](http://control-toolbox.org) or go directly to the documentation: 

[![Documentation](https://img.shields.io/badge/Documentation-OptimalControl.jl-blue)](http://control-toolbox.org/OptimalControl.jl)

## Installation [©](https://github.com/JuliaSmoothOptimizers/ADNLPModels.jl?tab=readme-ov-file#installation)

To install a package from the control-toolbox ecosystem, it is very simple. To install `OptimalControl.jl` for instance
please <a href="https://docs.julialang.org/en/v1/manual/getting-started/">open
Julia's interactive session (known as REPL)</a> and press <kbd>]</kbd> key in the REPL to use the package mode, then add the package:

```julia
julia> ]
pkg> add OptimalControl
```

> [!NOTE]
> Sometimes the above command can fail due to the default Julia registry ('General') not being installed for some reason.
> You can check that the registry is installed with
> 
> ```shell
> pkg> registry st
> Registry Status 
> [23338594] General (https://github.com/JuliaRegistries/General.git)
> ```
> 
> If the General registry is missing, simply add it
> 
> ```shell
> pkg> registry add General
> ```
> 
> then retry the `add` command.

## Main repositories

The [main repositories](https://github.com/orgs/control-toolbox/repositories?type=all) of the control-toolbox ecosystem are:

* [`CTBase.jl`](https://github.com/control-toolbox/CTBase.jl): fundamentals of the control-toolbox ecosystem
* [`CTDirect.jl`](https://github.com/control-toolbox/CTDirect.jl): direct transcription of an optimal control problem and resolution
* [`CTFlows.jl`](https://github.com/control-toolbox/CTFlows.jl): classical flow, Hamiltonian flow, flow from optimal control problem
* [`OptimalControl.jl`](https://github.com/control-toolbox/OptimalControl.jl): main package

```mermaid
flowchart TD
O(<a href='https://control-toolbox.org/OptimalControl.jl/stable/'>OptimalControl</a>) --> B(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctbase.html'>CTBase</a>)
O --> D(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctdirect.html'>CTDirect</a>)
O --> F(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctflows.html'>CTFlows</a>)
F --> B
D --> B
```

## Extras

* [`bocop`](https://github.com/control-toolbox/bocop): Bocop3, a direct solver for optimal control problem developed in `C++`.
* [Control loss examples](https://github.com/control-toolbox/control-loss): examples of optimal control problems with permanent and regional controls.
* [3D visualisation - averaged Kepler](https://github.com/control-toolbox/averaged_kepler): 3D visualisation of an optimal synthesis from the averaged Kepler problem.
* [Medical Resonance Imaging](https://github.com/control-toolbox/spin): simulations of the bi-saturation problem in MRI.
* [Zermelo navigation problems](https://github.com/control-toolbox/Zermelo): Kepler, Landau and Lindblad Zermelo problems.

## Discussions

We discuss about the control-toolbox ecosystem here:

* [![Github Issues](https://img.shields.io/github/issues-search?color=green&label=open%20issues&query=is%3Aopen%20is%3Aissue%20user%3Acontrol-toolbox%20archived%3Afalse)](https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+)
* [![GitHub Discussions](https://img.shields.io/github/discussions/control-toolbox/control-toolbox.github.io?color=green)](https://github.com/orgs/control-toolbox/discussions)
* [![](https://img.shields.io/badge/wiki-ct-green)](https://github.com/control-toolbox/control-toolbox.github.io/wiki)

## Misc
<img src="https://github.com/control-toolbox/control-toolbox.github.io/blob/main/assets/img/ct-logo.svg" alt="ct logo" width=40> calligraphy by [Alain Hurtig](https://www.alain.les-hurtig.org)
