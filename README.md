# Heroku buildpack for SWIG

A legacy buildpack that downloads the bundled **SWIG 2.0.5** archive and installs it into an application's `.jp_vendor/swig` directory.

## How it works

`bin/compile` downloads `swig.tar.gz` from this repository, extracts it, and exports `PATH`, `SWIG_LIB`, and `SWIG_FEATURES` for later build steps. The remaining buildpack entry points are in `bin/detect` and `bin/release`.

## Compatibility

This is an older buildpack. Compatibility with current Heroku stacks has not been established. Review the bundled binary, download verification, platform assumptions, and SWIG version before using it in a build pipeline.

To inspect shell syntax without installing anything:

```sh
bash -n bin/compile
bash -n bin/detect
bash -n bin/release
```

See [SECURITY.md](SECURITY.md) for private vulnerability reports.
