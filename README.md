# Feather SQL Database

An abstract sql-database component for Feather CMS.

## Getting started

⚠️ This repository is a work in progress, things can break until it reaches v1.0.0. 

Use at your own risk.

### Adding the dependency

To add a dependency on the package, declare it in your `Package.swift`:

```swift
.package(url: "https://github.com/feather-framework/feather-sql-database.git", .upToNextMinor(from: "0.2.0")),
```

and to your application target, add `FeatherSQLDatabase` to your dependencies:

```swift
.product(name: "FeatherSQLDatabase", package: "feather-sql-database")
```

Example `Package.swift` file with `FeatherSQLDatabase` as a dependency:

```swift
// swift-tools-version:5.9
import PackageDescription

let package = Package(
    name: "my-application",
    dependencies: [
        .package(url: "https://github.com/feather-framework/feather-sql-database.git", .upToNextMinor(from: "0.2.0")),
    ],
    targets: [
        .target(name: "MyApplication", dependencies: [
            .product(name: "FeatherSQLDatabase", package: "feather-sql-database")
        ]),
        .testTarget(name: "MyApplicationTests", dependencies: [
            .target(name: "MyApplication"),
        ]),
    ]
)
```

