# hyperfine

> A command-line benchmarking tool.

- Run a basic benchmark:

`hyperfine '{{make}}'`

- Change minimum number of benchmarking runs:

`hyperfine --min-runs {{7}} '{{make}}'`

- Perform benchmark with warmup:

`hyperfine --warmup {{5}} '{{make}}'`

- Run a command before each benchmark run (to clear caches, etc.):

`hyperfine --prepare '{{make clean}}' '{{make}}'`

- Run a benchmark where a single parameter changes for each run:

`hyperfine --prepare '{{make clean}}' --parameter-scan num_threads {{1}} {{10}} '{{make -j {num_threads}}}'`
