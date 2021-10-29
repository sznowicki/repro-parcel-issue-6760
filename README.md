# Repro repo for Parcel issue with importing svg with base64 png

This is a repro repo for [parcel-bundler issue #6760](https://github.com/parcel-bundler/parcel/issues/6760).

You can reproduce the issue on master branch. On RC branch build works just fine.

## Benchmarks
OS: macOS 12.0.1 (also happens on macOS 11.6)

- `master` branch build time: on my machine, with this exact SVG it seems like it takes forever, killed after several minutes
- `rc` branch build time: 2.69s.

Also worth noting killing that hanged process is not possible with simple `ctr + c`. One must go to the activities app and force kill it.
