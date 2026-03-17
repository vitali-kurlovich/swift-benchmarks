# swift-benchmarks


The swift-benchmarks package lets you easily create simple Swift benchmarks to measure the execution time of your code.

This README provides a quick overview of the Benchmarks package. For more detailed information, please [see the documentation](https://vitali-kurlovich.github.io/swift-benchmarks/documentation/benchmarks)


## Adding dependencies and getting started

There are just a few steps required to get started benchmarking:
1. Add a dependency to the project
2. Add benchmarks executable target
3. Run `swift run -c release` or `swift run` if you want to measure time in debug mode

## The detailed steps:
### Step 1: Add a package dependency to the **Package.swift**
Update your **Package.swift**, add the [swift-benchmarks](https://github.com/vitali-kurlovich/swift-benchmarks) and [swift-argument-parser](https://github.com/apple/swift-argument-parser) dependencies to your package:
```swift
 dependencies: [
        .package(url: "https://github.com/vitali-kurlovich/swift-benchmarks", from: "0.3.0"),
        .package(url: "https://github.com/apple/swift-argument-parser.git", from: "1.7.0"),
    ],
```

### Step 2: Add an executable target dependency to the **Package.swift**
 - Create a folder for the benchmarks source code (example: folder **'MyBenchmarks'** in the root of your module)
 - Add executable target and dependencies:
```swift
.executableTarget(
            name: "MyBenchmarks",
            dependencies: [
                .product(name: "ArgumentParser", package: "swift-argument-parser"),
                .product(name: "Benchmarks", package: "swift-benchmarks"),
            ],
            path: "MyBenchmarks"
        ),
```

### Step 3: Run benchmarks
 - Open the Terminal
 - Change directory to your project dir
 - Run `swift run -c release` or `swift run` if you want to measure time in debug mode


## Example

You can find an example of benchmarks in [BenchmarksCLI](https://github.com/vitali-kurlovich/swift-benchmarks/tree/main/BenchmarksCLI)

![CL](https://vitali-kurlovich.github.io/static-content/benchmarks/benchmarkcl.avif)
