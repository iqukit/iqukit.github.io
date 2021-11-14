# QuKit

Quantum Kit in Swift framework.

[![Build Status](https://github.com/iqukit/qukit/workflows/Swift/badge.svg)](https://github.com/iqukit/qukit.GA/actions?query=workflow%3ASwift)
[![GitHub forks](https://img.shields.io/github/forks/iqukit/qukit.svg?style=social&label=Fork&maxAge=2592000)](https://GitHub.com/iqukit/qukit/network/)
[![GitHub stars](https://img.shields.io/github/stars/iqukit/qukit.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/iqukit/qukit/stargazers/)
[![GitHub followers](https://img.shields.io/github/followers/iqukit.svg?style=social&label=Follow&maxAge=2592000)](https://github.com/iqukit?tab=followers)

## Swift Package Manager

Add the following dependency to your Package.swift manifest:

```
.package(url: "https://github.com/pvieito/PythonKit.git", .branch("main")),
```

Namely,

```
import PackageDescription

let package = Package(
    name: "MyPackage",
    dependencies: [
        .package(url: "https://github.com/pvieito/PythonKit.git", .branch("main")),
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