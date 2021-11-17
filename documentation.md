---
layout: default
title: Documentation
permalink: /documentation/
---

## Usage

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