---
layout: home
---

Quantum Kit in Swift framework.

QuKit is a [Swift](https://www.swift.org/) library for interacting with quantum physics,
which makes programming simple things easy, and difficult things possible.
It is inspired by the [Quantum Optics Toolbox for MATLAB](https://qo.phy.auckland.ac.nz/toolbox/), 
the Python framework [QuTiP](https://qutip.org/),
and the [Julia Framework for Open Quantum Dynamics](https://qojulia.org/).

## Usage

Add the following dependency to your Package.swift manifest:

```
.package(url: "https://github.com/iqukit/qukit.git", .branch("main")),
```

Namely,

```
import PackageDescription

let package = Package(
    name: "MyPackage",
    dependencies: [
        .package(url: "https://github.com/iqukit/qukit.git", .branch("main")),
    ],
    targets: [
        .target(
            name: "MyPackage",
            dependencies: ["qukit"]
        ),
        .testTarget(
            name: "MyPackageTests",
            dependencies: ["MyPackage"]
        ),
    ]
)
```
Now you should be able to `import qukit` in the `MyPackage` target.