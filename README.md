<h1 align="center">cargo-criterion</h1>

<div align="center">Criterion-rs Cargo Extension</div>

<div align="center">
    <a href="https://github.com/bheisler/cargo-criterion/blob/master/CHANGELOG.md">Changelog</a>
</div>

<div align="center">
    <a href="https://crates.io/crates/cargo-criterion">
        <img src="https://img.shields.io/crates/v/cargo-criterion.svg" alt="Crates.io">
    </a>
</div>

cargo-criterion is a Plugin for Cargo which handles much of the heavy lifting for analyzing and 
reporting on [Criterion-rs](https://github.com/bheisler/criterion.rs) benchmarks.

## Table of Contents
- [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Quickstart](#quickstart)
  - [Goals](#goals)
  - [Contributing](#contributing)
  - [Compatibility Policy](#compatibility-policy)
  - [Maintenance](#maintenance)
  - [License](#license)

### Features

- __Statistics__: Statistical analysis detects if, and by how much, performance has changed since the last benchmark run
- __Charts__: Uses [gnuplot](http://www.gnuplot.info/) or [plotters](https://crates.io/crates/plotters) to generate detailed graphs of benchmark results
- __Stable-compatible__: Benchmark your code without installing nightly Rust

### Quickstart

This assumes that you already have benchmarks which use Criterion-rs. If not, see [the Criterion-rs Quickstart Guide](https://github.com/bheisler/criterion.rs#quickstart).

First install cargo-criterion:

`cargo install cargo-criterion`

Then you can use it to run your Criterion-rs benchmarks:

`cargo criterion`

### Goals

- cargo-criterion seeks to improve iteration time for Criterion-rs benchmarks. By moving functionality into a separate executable which can be installed once and reused, Criterion-rs can shrink - meaning less code to compile and link into the benchmarks themselves.
- Because cargo-criterion can oversee the whole benchmark process from beginning to end, it's better placed to deliver features that would be difficult to implement in Criterion-rs.

### Contributing

First, thank you for contributing.

One great way to contribute to cargo-criterion is to use it for your own benchmarking needs and report your experiences, file and comment on issues, etc.

Code or documentation improvements in the form of pull requests are also welcome. If you're not
sure what to work on, try checking the 
[Beginner label](https://github.com/bheisler/cargo-criterion/issues?q=is%3Aissue+is%3Aopen+label%3ABeginner).

If your issues or pull requests have no response after a few days, feel free to ping me (@bheisler).

For more details, see the [CONTRIBUTING.md file](https://github.com/bheisler/cargo-criterion/blob/master/CONTRIBUTING.md).

### Compatibility Policy

cargo-criterion supports the last three stable minor releases of Rust. At time of
writing, this means Rust 1.41 or later. Older versions may work, but are not tested or guaranteed.

Currently, the oldest version of Rust believed to work is 1.34. Future versions of cargo-criterion may
break support for such old versions, and this will not be considered a breaking change. If you
require cargo-criterion to work on old versions of Rust, you will need to stick to a
specific patch version of cargo-criterion.

### Maintenance

cargo-criterion was originally developed and is currently maintained by Brook Heisler (@bheisler).

### License

cargo-criterion is dual licensed under the Apache 2.0 license and the MIT license.