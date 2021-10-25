# QuantumControlRegistry

This is a Julia package registry for the [JuliaQuantumControl](https://github.com/JuliaQuantumControl) organization.

It contains packages that are not (or not yet) in the [Julia General Registry](https://github.com/JuliaRegistries/General). This is for development and testing purposes only.

## Using the registry

To use the registry, run

~~~
pkg> registry add https://github.com/JuliaQuantumControl/QuantumControlRegistry.git
~~~

or, using `Pkg`'s API,

~~~
using Pkg
Pkg.Registry.add(RegistrySpec(url="https://github.com/JuliaQuantumControl/QuantumControlRegistry.git"))
~~~

This needs to be done only once per Julia installation.

## Adding a package to the registry

~~~
using LocalRegistry
register("./GRAPELinesearchAnalysis.jl/", registry="QuantumControlRegistry")
~~~

See [the `LocalRegistry` documentation](https://github.com/GunnarFarneback/LocalRegistry.jl#readme) for more details.
