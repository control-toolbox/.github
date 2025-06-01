# Welcome to control-toolbox!

The control-toolbox ecosystem gathers &nbsp;
<a href="https://julialang.org">
 <img src="https://raw.githubusercontent.com/JuliaLang/julia-logo-graphics/master/images/julia.ico" width="16em">
 Julia
</a> &nbsp; packages for mathematical control and applications. 

The root package is [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl) which aims to provide tools to model and solve optimal control problems with ordinary differential equations by direct and indirect methods.

## Documentation

To learn how to define and solve optimal control problems in Julia, please refer to the documentation of **OptimalControl.jl**:

[![Doc](https://img.shields.io/badge/Doc-OptimalControl.jl-blue)](http://control-toolbox.org/OptimalControl.jl)

The documentation provides:

- step-by-step examples of basic optimal control problems;
- guides on problem definition, solver initialization, solution plotting, and Hamiltonian flow computation;
- tutorials on combining direct and indirect methods, and working with discretized problems;
- real-world applications in calculus of variations, MRI, space mechanics, and more;
- a collection of benchmark problems, modeled in OptimalControl and JuMP, to test and compare solvers.

## Installation [©](https://github.com/JuliaSmoothOptimizers/ADNLPModels.jl?tab=readme-ov-file#installation)

To install **OptimalControl.jl** please <a href="https://docs.julialang.org/en/v1/manual/getting-started/">open
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

The control-toolbox [repositories](https://github.com/orgs/control-toolbox/repositories?type=all) include:

* [OptimalControl.jl](https://github.com/control-toolbox/OptimalControl.jl): main package
* [CTBase.jl](https://github.com/control-toolbox/CTBase.jl): fundamentals of the control-toolbox ecosystem
* [CTDirect.jl](https://github.com/control-toolbox/CTDirect.jl): direct transcription of an optimal control problem and resolution
* [CTFlows.jl](https://github.com/control-toolbox/CTFlows.jl): classical flow, Hamiltonian flow, flow from optimal control problem
* [CTModels.jl](https://github.com/control-toolbox/CTModels.jl): models of optimal control problem, solution
* [CTParser.jl](https://github.com/control-toolbox/CTParser.jl): parser to define an optimal control problem with an abstract syntax

```mermaid
flowchart TD
B(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-ctbase.html'>CTBase</a>)
M(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-ctmodels.html'>CTModels</a>)
P(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-ctparser.html'>CTParser</a>)
O(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-optimalcontrol.html'>OptimalControl</a>)
D(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-ctdirect.html'>CTDirect</a>)
F(<a href='https://control-toolbox.org/OptimalControl.jl/stable/dev-ctflows.html'>CTFlows</a>)
O --> D
O --> M
O --> F
O --> P
F --> M
O --> B
F --> B
D --> B
D --> M
P --> M
P --> B
M --> B
```

## Contributing

[issue-url]: https://github.com/issues?q=is%3Aopen%20is%3Aissue%20user%3Acontrol-toolbox%20archived%3Afalse%20-repo%3Acontrol-toolbox%2Fbocop
[first-good-issue-url]: https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Acontrol-toolbox+archived%3Afalse+-repo%3Acontrol-toolbox%2Fbocop+label%3A"good+first+issue"

Any contributions are welcomed, check out [how to contribute to a Github project](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project). 
If it is your first contribution, you can also check [this first contribution tutorial](https://github.com/firstcontributions/first-contributions).
You can find first good issues (if any 🙂) [here][first-good-issue-url] and the list of control-toolbox issues at the [control-toolbox list of issues][issue-url].

For any package, if you think you found a bug or if you have a feature request or suggestion, feel free to open an issue.
Before opening a pull request, start an issue or a discussion on the topic, please.
If you want to ask a question, feel free to start a [discussion](https://github.com/orgs/control-toolbox/discussions).

>[!NOTE]
> If you want to add an application or a package to the control-toolbox ecosystem, please follow this [set up tutorial](https://github.com/control-toolbox/CTApp.jl/discussions/9).

## Citing us

If you use the package OptimalControl.jl in your work, please [cite us](https://github.com/control-toolbox/OptimalControl.jl?tab=readme-ov-file#citing-us).

## Misc

- <img src="https://github.com/control-toolbox/control-toolbox.github.io/blob/main/assets/img/ct-logo.svg" alt="ct logo" width=40> calligraphy by [Alain Hurtig](https://www.alain.les-hurtig.org)
- [bocop](https://github.com/control-toolbox/bocop): Bocop3, a direct solver for optimal control problem developed in `C++`
- [control-toolbox wiki](https://github.com/control-toolbox/control-toolbox.github.io/wiki)
