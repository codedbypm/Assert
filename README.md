<p align="center">
    <img src="logo.png" width="300" max-width="50%" alt="Assert" />
</p>

<p align="center">
    <a href="https://swift.org/package-manager">
        <img src="https://img.shields.io/badge/spm-compatible-brightgreen.svg?style=flat" alt="Swift Package Manager" />
    </a>
    <a href="https://twitter.com/johnsundell">
        <img src="https://img.shields.io/badge/contact-@johnsundell-blue.svg?style=flat" alt="Twitter: @johnsundell" />
    </a>
</p>

This repo contains a collection of assertion functions that you can use in your tests, as a complement to the assertions provided by `XCTest`, or other testing frameworks. This collection will likely grow over time, and you are more than welcome to contribute your own custom assertion functions as a pull request! :rocket:

## What's in the box?

Here is what you can currently assert using the functions that `Assert` provides:

#### That an expression threw a given error:

```swift
assert(try myFunction(), throwsError: MyError.anError)
```

#### That a closure threw a given error:

```swift
assertErrorThrown(MyError.anError) {
    try myFunction()
}
```

#### That a closure didn't throw an error:

```swift
assertNoErrorThrown {
    try myFunction()
}
```

## Usage

You can either use `Assert` through the Swift Package Manager, by adding the following `dependency` to your `Package.swift` file:

```swift
.Package(url: "https://github.com/johnsundell/assert", majorVersion: 1)
```

Or, you can simply clone the repo, and drag the file `Sources/Assert.swift` into your Xcode project and add it to your test target.

## Questions or feedback?

Feel free to [open an issue](https://github.com/JohnSundell/Assert/issues/new), or find me [@johnsundell on Twitter](https://twitter.com/johnsundell).
