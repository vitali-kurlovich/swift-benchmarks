# Benchmarks


The Benchmarks package lets you easily create simple Swift benchmarks to measure the execution time of your code.

This README provides a quick overview of the Benchmarks package. For more detailed information, please [see the documentation](https://vitali-kurlovich.github.io/Benchmarks/documentation/benchmarks)


## Adding dependencies and getting started

There are just a few steps required to get started benchmarking:
1. Add a dependency to the project
2. Add benchmarks executable targets
3. Run `swift run -c release` or `swift run` if you want to measure time in debug mode

## The detailed steps:
### Step 1: Add a package dependency to Package.swift
Update your Package.swift, add the [Benchmarks](https://github.com/vitali-kurlovich/Benchmarks) dependency to your package:
```swift
 dependencies: [
        .package(url: "https://github.com/vitali-kurlovich/Benchmarks", from: "0.3.0"),
    ],
```



![CL](https://vitali-kurlovich.github.io/static-content/benchmarks/benchmarkcl.avif)
