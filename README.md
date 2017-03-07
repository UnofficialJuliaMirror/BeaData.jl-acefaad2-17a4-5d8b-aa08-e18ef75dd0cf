# BeaData

*A Julia interface for retrieving data from the U.S. Bureau of Economic Analysis (BEA)
Data API.*

|**Documentation** | **Package Evaluator** | **Build Status** |
|:----------------:|:---------------------:|:----------------:|
| [![][docs-stable-img]][docs-stable-url] [![][docs-latest-img]][docs-latest-url] | [![][pkg-0.4-img]][pkg-0.4-url][![][pkg-0.5-img]][pkg-0.5-url] | [![][travis-img]][travis-url] |

## Installation

At the Julia REPL:

```julia
    Pkg.add("BeaData")
```
## Usage

See the [package documentation][docs-stable-url].

A valid registration key is required to use the BEA's API. A key can be obtained by registering [here](http://www.bea.gov/API/signup/index.cfm).

For now, the package only retrieves full tables from the standard National
Income and Product Accounts (NIPA) (i.e., no downloads of single data series or
    from other datasets such as the International Transactions Accounts).


## Known Issue
All requests by BeaData.jl to the BEA API currently throw an `HTTP Parser Exception`,
though this does not prevent the requested query from being completed successfully
as long as valid arguments are provided to the functions.  This is not a client-side issue, caused instead by an extra space character returned by the BEA server's response (thanks to  [@quinnj](https://github.com/quinnj) - Jacob Quinn - for figuring this out).  This will be fixed in a future update.

## Disclaimer
BeaData is not affiliated with, officially maintained, or otherwise supported by the Bureau of Economic Analysis.

[docs-latest-img]: https://img.shields.io/badge/docs-latest-blue.svg
[docs-latest-url]: https://stephenbnicar.github.io/BeaData.jl/latest

[docs-stable-img]: https://img.shields.io/badge/docs-stable-blue.svg
[docs-stable-url]: https://stephenbnicar.github.io/BeaData.jl/stable

[travis-img]: https://travis-ci.org/stephenbnicar/BeaData.jl.svg?branch=master
[travis-url]: https://travis-ci.org/stephenbnicar/BeaData.jl

[pkg-0.4-img]: http://pkg.julialang.org/badges/BeaData_0.4.svg
[pkg-0.4-url]: http://pkg.julialang.org/?pkg=BeaData
[pkg-0.5-img]: http://pkg.julialang.org/badges/BeaData_0.5.svg
[pkg-0.5-url]: http://pkg.julialang.org/?pkg=BeaData
