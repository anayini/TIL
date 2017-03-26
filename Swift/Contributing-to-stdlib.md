## Useful Commands

##### How to Rebuild stdlib only:
1. cd into `./build/Ninja-BUILDSCHEME/swift-<ARCHITECTURE>`
2. run `ninja swift-stdlib`

Note: GYB files are regenerated during a build automatically by CMAKE if their contents change.

##### How to Run Tests:

`./swift/utils/build-script -t` runs everything and the kitchen sink (not recommended if just doing stdlib changes)

`./llvm/utils/lit/lit.py -sv ./swift/test/stdlib` runs all tests under the ‘stdlib’ subdirectory.
