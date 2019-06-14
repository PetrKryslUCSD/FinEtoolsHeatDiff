[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![Build Status](https://travis-ci.com/PetrKryslUCSD/FinEtoolsHeatDiff.jl.svg?branch=master)](https://travis-ci.com/PetrKryslUCSD/FinEtoolsHeatDiff.jl)

[![][docs-latest-img]][docs-latest-url]

[docs-latest-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-latest-url]: http://petrkryslucsd.github.io/FinEtoolsHeatDiff.jl/latest/

# FinEtoolsHeatDiff: Linear stress analysis application

`FinEtools` is a package for basic operations on finite element meshes.
`FinEtoolsHeatDiff` is a package using `FinEtools` to solve linear heat conduction (diffusion) problems.

## News

- 06/11/2019: Applications are now separated  out from the `FinEtools` package.

[Past news](oldnews.md)

## How to run

Here is a record of the session to install this package and test it. You should see something similar. The git bash running on Windows 10 was used in this example.

```
PetrKrysl@Spectre MINGW64 /tmp/exp
$ git clone https://github.com/PetrKryslUCSD/FinEtoolsHeatDiff.jl.git
Cloning into 'FinEtoolsHeatDiff.jl'...
remote: Enumerating objects: 111, done.
remote: Counting objects: 100% (111/111), done.
remote: Compressing objects: 100% (70/70), done.
remote: Total 111 (delta 32), reused 103 (delta 27), pack-reused 0
Receiving objects: 100% (111/111), 86.90 KiB | 2.71 MiB/s, done.
Resolving deltas: 100% (32/32), done.

PetrKrysl@Spectre MINGW64 /tmp/exp
$ cd FinEtoolsHeatDiff.jl/

PetrKrysl@Spectre MINGW64 /tmp/exp/FinEtoolsHeatDiff.jl (master)
$ ~/AppData/Local/Julia-1.2.0-rc1/bin/julia.exe
               _
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.2.0-rc1.0 (2019-05-30)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

(v1.2) pkg> activate .; instantiate
[ Info: activating environment at `C:\Users\PETRKR~1\AppData\Local\Temp\exp\FinEtoolsHeatDiff.jl\Project.toml`.
   Cloning default registries into `C:\Users\PetrKrysl\.julia`
   Cloning registry from "https://github.com/JuliaRegistries/General.git"
     Added registry `General` to `C:\Users\PetrKrysl\.julia\registries\General`
   Cloning git-repo `https://github.com/PetrKryslUCSD/FinEtools.jl.git`
  Updating git-repo `https://github.com/PetrKryslUCSD/FinEtools.jl.git`
 Installed Missings ─────────── v0.4.1
 Installed SortingAlgorithms ── v0.3.1
 Installed Arpack ───────────── v0.3.1
 Installed OrderedCollections ─ v1.1.0
 Installed DataStructures ───── v0.15.0
 Installed BinaryProvider ───── v0.5.4
 Installed StatsBase ────────── v0.30.0
  Building Arpack → `C:\Users\PetrKrysl\.julia\packages\Arpack\cu5By\deps\build.log`

(FinEtoolsHeatDiff) pkg> test
   Testing FinEtoolsHeatDiff
 Resolving package versions...
Test Summary:  | Pass  Total
Heat diffusion |   61     61
 43.754623 seconds (120.44 M allocations: 8.151 GiB, 6.38% gc time)
   Testing FinEtoolsHeatDiff tests passed

(FinEtoolsHeatDiff) pkg>
```

The [FinEtools](https://github.com/PetrKryslUCSD/FinEtools.jl) package is
needed. The entire setup of `FinEtoolsHeatDiff` can be performed with
```julia
] activate .; instantiate
```

The package `FinEtoolsHeatDiff` can be tested as
```julia
] activate .; instantiate; test
```

There are a number of examples, which may
be executed as described in the  [conceptual guide to
`FinEtools`](https://petrkryslucsd.github.io/FinEtools.jl/latest).
