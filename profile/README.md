# Welcome to control-toolbox!

The control-toolbox ecosystem gathers `Julia` packages for mathematical control and applications. The root package is [`OptimalControl.jl`](https://github.com/control-toolbox/OptimalControl.jl) which aims to provide tools to solve optimal control problems by direct and indirect methods.

[![doc OptimalControl.jl](https://img.shields.io/badge/doc-OptimalControl.jl-blue)](http://control-toolbox.org/docs/optimalcontrol)

## Installation

To install a package from the control-toolbox ecosystem, you must add its registry into your `Julia` configuration.

Start `Julia`:

```shell
>> julia
```

Then, add `ct-registry` to the list of known registries:

```shell
julia> ]
pkg> registry add https://github.com/control-toolbox/ct-registry.git
```

Finally, you can install any package as usual. For instance:

```shell
pkg> add OptimalControl
```

## Getting started

To solve your first optimal control problem using `OptimalControl.jl` package, please visit our [basic example tutorial](https://control-toolbox.org/docs/optimalcontrol/stable/tutorial-basic-example.html) or just copy-paste the following piece of code!

```julia
using OptimalControl
@def ocp begin
    t ∈ [ 0, 1 ], time
    x ∈ R², state
    u ∈ R, control
    x(0) == [-1, 0]
    x(1) == [0, 0]
    ẋ(t) == [x₁(t), u(t)]
    ∫( 0.5u(t)^2 ) → min
end
sol = solve(ocp)
plot(sol, size=(600, 450))
```

You should obtain this:

<img width="600" alt="sol-basic-example" src="https://github.com/control-toolbox/.github/assets/66357348/95b86ad4-abf5-4e70-8fd4-ace324daf983">


## Main repositories

The [main repositories](https://github.com/orgs/control-toolbox/repositories?type=all) of the control-toolbox ecosystem are:

* [`ct-registry`](https://github.com/control-toolbox/ct-registry): the control-toolbox registry since the packages are not yet available in the [official registry](https://github.com/JuliaRegistries/General)
* [`CTBase.jl`](https://github.com/control-toolbox/CTBase.jl): fundamentals of the control-toolbox ecosystem
* [`CTDirect.jl`](https://github.com/control-toolbox/CTDirect.jl): direct transcription of an optimal control problem and resolution
* [`CTDirectShooting.jl`](https://github.com/control-toolbox/CTDirectShooting.jl): direct shooting transcription of an optimal control problem and resolution
* [`CTFlows.jl`](https://github.com/control-toolbox/CTFlows.jl): classical flow, Hamiltonian flow, flow from optimal control problem
* [`CTProblems.jl`](https://github.com/control-toolbox/CTProblems.jl): library of optimal control problems
* [`OptimalControl.jl`](https://github.com/control-toolbox/OptimalControl.jl): main package

## Extras

* [`bocop`](https://github.com/control-toolbox/bocop): Bocop3, a direct solver for optimal control problem developed in `C++`

## Discussions

We discuss about the control-toolbox ecosystem here:

* [![Github Issues](https://img.shields.io/github/issues-search?color=green&label=open%20issues&query=is%3Aopen%20is%3Aissue%20user%3Acontrol-toolbox%20archived%3Afalse)](https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+)
* [![GitHub Discussions](https://img.shields.io/github/discussions/control-toolbox/control-toolbox.github.io?color=green)](https://github.com/orgs/control-toolbox/discussions)
* [![](https://img.shields.io/badge/wiki-ct-green)](https://github.com/control-toolbox/control-toolbox.github.io/wiki)
