# FOSUtilities

![Run unit tests](https://github.com/foscomputerservices/FOSUtilities/actions/workflows/ci.yml/badge.svg) ![Swift Package Manager](https://img.shields.io/badge/spm-compatible-brightgreen.svg?style=flat) [![](https://img.shields.io/endpoint?url=https%3A%2F%2Fswiftpackageindex.com%2Fapi%2Fpackages%2Ffoscomputerservices%2FFOSUtilities%2Fbadge%3Ftype%3Dswift-versions)](https://swiftpackageindex.com/foscomputerservices/FOSUtilities) [![](https://img.shields.io/endpoint?url=https%3A%2F%2Fswiftpackageindex.com%2Fapi%2Fpackages%2Ffoscomputerservices%2FFOSUtilities%2Fbadge%3Ftype%3Dplatforms)](https://swiftpackageindex.com/foscomputerservices/FOSUtilities)

There are three libraries provided by the FOSUtilities package:  FOSFoundation, FOSMVVM and FOSTesting.

## Documentation

For guides, articles, and API documentation see the 
[library's documentation on the Web][docs] or in Xcode.

[docs]: https://swiftpackageindex.com/foscomputerservices/FOSUtilities/documentation/fosfoundation

## Alpha Stability Warning

Please note that these libraries are currently a work in progress.  The APIs are rapidly evolving and while the overall architecture is set, breaking changes will occur until 1.0 is released.  The documentation is evolving, but the 'Getting Started' guidance is incomplete.  Nonetheless, the implementations are stable and unit tests are in place to ensure proper code coverage and stability of all publicly-facing APIs.  This warning will remain in place until I feel that these limitations are remedied.  Please log any issues that you might find or suggestions for improvements.

## FOSFoundation

FOSFoundation is a library of protocols, patterns, types and routines that I have found generally useful in my projects.  Support areas include:

- Extensions to **URL** for one-line REST-Style requests
- Extensions to **JSONEncoder** and **JSONDecoder** for single-statement encoding/decoding of **Codables**
    - Along with standardized support for handling various **Date** and **DateTime** styles
        - [ISO 8601](https://w.wiki/8G7)
        - JSON
- Extensions to **Collection** for throttling execution of requests when servers restrict the number of requests per any time period
- Extensions on **String** such as:
    - [CamelCase](https://w.wiki/4GVz) / [snake_case](https://w.wiki/6MmH) conversion
    - Hexadecimal String to/from **UInt64**, **Int64**, **UInt**, and **Int**
    - Cleaning and standardizing user-provided input
    - Generating random and unique **String**s
    - Swift Range support
    - **String** obfuscation/revealing (e.g., [ROT 13/ROT 47](https://w.wiki/8$LR))

For guides, articles, and API documentation see the 
[library's documentation on the Web][docs] or in Xcode.

- [Getting Started with FOS Foundation](https://swiftpackageindex.com/foscomputerservices/FOSUtilities/documentation/fosfoundation/gettingstarted)

## FOSMVVM

FOSMVVM is a library that implements the [Model-View-ViewModel](https://w.wiki/4T5B) pattern for binding SwiftUI projects
to [Vapor](https://docs.vapor.codes) web services.

For guides, articles, and API documentation see the 
[library's documentation on the Web][docs] or in Xcode.

- [Getting Started with FOS MVVM](https://swiftpackageindex.com/foscomputerservices/FOSUtilities/documentation/fosmvvm/gettingstarted)

## FOSTesting

FOSTestingUtilities is a package of testing patterns, types and routines that I have found generally useful in my projects.

For guides, articles, and API documentation see the 
[library's documentation on the Web][docs] or in Xcode.

- [Getting Started with FOS Testing](https://swiftpackageindex.com/foscomputerservices/FOSUtilities/documentation/fostesting/gettingstarted)

## Swift Package Manager

FOSUtilities supports the [Swift Package Manager](https://www.swift.org/package-manager/).  To include FOSUtilities in your project add the following to your Package.swift file:

```swift
.package(url: "git@github.com:foscomputerservices/FOSUtilities.git", branch: "main"),
```

To use one of the libraries, add one or more entry in the dependencies list of a target in your Package.swift file:

```swift
.target(
    name: "MyTarget",
    dependencies: [
        .product(name: "FOSFoundation", package: "FOSUtilities"),
        .product(name: "FOSMVVM", package: "FOSUtilities")
        // ...
    ]
),
.testTarget(
    name: "MyTests",
    dependencies: [
        .byName(name: "MyTarget"),
        .byName(name: "FOSFoundation"),
        .byName(name: "FOSMVVM"),
        .byName(name: "FOSTesting"),
        .product(name: "Testing", package: "swift-testing")
    ]
)
```

## Contributing

All contributions are welcome!  Please see [CONTRIBUTING.md](https://github.com/foscomputerservices/FOSUtilities/blob/main/CONTRIBUTING.md) for more details.

## Maintainers

This project is maintained by [David Hunt](https://www.linkedin.com/in/davidhun/) owner of [FOS Computer Services, LLC](https://www.linkedin.com/company/1856731).

## License

FOSUtilities is under the MIT License.  See the [LICENSE](https://github.com/foscomputerservices/FOSUtilities/blob/main/LICENSE) file for more information.
