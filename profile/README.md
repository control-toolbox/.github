# Welcome to control-toolbox!

The control-toolbox ecosystem gathers &nbsp;
<a href="https://julialang.org">
 <img src="https://raw.githubusercontent.com/JuliaLang/julia-logo-graphics/master/images/julia.ico" width="16em">
 Julia
</a> &nbsp; packages for mathematical control and applications. 

The root package is [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl) which aims to provide tools to modelise and solve optimal control problems with ordinary differential equations by direct and indirect methods.

> [!TIP]
> From the [documentation](http://control-toolbox.org/OptimalControl.jl), you can find tutorials to define and solve optimal control problems with OptimalControl.jl. 

See also some applications of [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl):

- [Examples from calculus of variations](https://control-toolbox.org/calculus_of_variations)
- [Optimal control in Medical Resonance Imaging](https://control-toolbox.org/medical_resonance_imaging)
- [Orbit transfer from space mechanics](https://control-toolbox.org/kepler)
- ... and more

[![Documentation](https://img.shields.io/badge/Documentation-OptimalControl.jl-blue)](http://control-toolbox.org/OptimalControl.jl)

## Installation [©](https://github.com/JuliaSmoothOptimizers/ADNLPModels.jl?tab=readme-ov-file#installation)

To install [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl) please <a href="https://docs.julialang.org/en/v1/manual/getting-started/">open
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

The control-toolbox [hierarchy](https://github.com/orgs/control-toolbox/repositories?type=all) includes:

* [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl): main package
* [CTBase.jl](https://github.com/control-toolbox/CTBase.jl): fundamentals of the control-toolbox ecosystem
* [CTDirect.jl](https://github.com/control-toolbox/CTDirect.jl): direct transcription of an optimal control problem and resolution
* [CTFlows.jl](https://github.com/control-toolbox/CTFlows.jl): classical flow, Hamiltonian flow, flow from optimal control problem


```mermaid
flowchart TD
O(<a href='https://control-toolbox.org/OptimalControl.jl/stable/'>OptimalControl</a>) --> B(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctbase.html'>CTBase</a>)
O --> D(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctdirect.html'>CTDirect</a>)
O --> F(<a href='https://control-toolbox.org/OptimalControl.jl/stable/api-ctflows.html'>CTFlows</a>)
F --> B
D --> B
```

## Extras

* [bocop](https://github.com/control-toolbox/bocop): Bocop3, a direct solver for optimal control problem developed in `C++`.
* [Control loss examples](https://github.com/control-toolbox/control-loss): examples of optimal control problems with permanent and regional controls.
* [3D visualisation - averaged Kepler](https://github.com/control-toolbox/averaged_kepler): 3D visualisation of an optimal synthesis from the averaged Kepler problem.
* [Spin control](https://github.com/control-toolbox/spin): simulations of the bi-saturation problem in MRI.
* [Zermelo navigation problems](https://github.com/control-toolbox/Zermelo): Kepler, Landau and Lindblad Zermelo problems.

## Discussions

We discuss about the control-toolbox ecosystem here:

* [![Github Issues](https://img.shields.io/github/issues-search?color=green&label=open%20issues&query=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+-repo%3Acontrol-toolbox%2Fbocop+)](https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+-repo%3Acontrol-toolbox%2Fbocop+)
* [![GitHub Discussions](https://img.shields.io/github/discussions/control-toolbox/control-toolbox.github.io?color=green)](https://github.com/orgs/control-toolbox/discussions)
* [![](https://img.shields.io/badge/wiki-ct-green)](https://github.com/control-toolbox/control-toolbox.github.io/wiki)

## Misc
<img src="https://github.com/control-toolbox/control-toolbox.github.io/blob/main/assets/img/ct-logo.svg" alt="ct logo" width=40> calligraphy by [Alain Hurtig](https://www.alain.les-hurtig.org)
