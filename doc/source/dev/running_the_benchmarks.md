# Running the benchmarks

This document outlines how to setup and run the benchmarks using [asv](https://asv.readthedocs.io/en/v0.6.1/).

## Running the benchmarks

To run the benchmarks with ``asv``, simply enter:

```shell
asv run
```

## Viewing the results

There are two steps to viewing the results locally. The results need to be published and the launched in a local web browser.

To publish the results use:

```shell
asv publish
```

And then to view the results:

```shell
asv preview
```

This will launch a local web browser from which you can view the results

## Dry runs

One common use case is to use ``asv`` in development, there are several useful flags that should be used:

```shell
asv --python=same --quick --dry-run
```

We are adding three flags, these flags are:

1. `--python=same` uses the same environment as your development environment (saves time to avoid building environments)
2. `--quick` only runs the benchmarks once
3. `--dry-run` to not save the results of the benchmarks

These can be useful for getting quick feedback during development, but should not be used as anything other than a rough guide.