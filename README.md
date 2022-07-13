[<img src="https://assets.signaloid.io/add-to-signaloid-cloud-logo-dark-v6.png#gh-dark-mode-only" alt="[Add to signaloid.io]" height="30">](https://signaloid.io/repositories?connect=https://github.com/signaloid/Signaloid-Demo-Basic-Schlieren#gh-dark-mode-only)
[<img src="https://assets.signaloid.io/add-to-signaloid-cloud-logo-light-v6.png#gh-light-mode-only" alt="[Add to signaloid.io]" height="30">](https://signaloid.io/repositories?connect=https://github.com/signaloid/Signaloid-Demo-Basic-Schlieren#gh-light-mode-only)

# MICRO Benchmark: `schlieren`

Benchmark from Tsoutsouras et al. MICRO paper.[^0]

The benchmark computes the result of expression `(A+B)/(A-B)`, where `A` and `B` are variables with associated distributional information.

## Arguments

```
schlieren -a <samples file for A> -b <samples file for B>
	-a <samples file for A>: set to `input-a.txt` by default
	-b <samples file for B>: set to `input-b.txt` by default
```

## Inputs

The samples are stored in a text file.
The first line of the file is the number of samples that follow.

The `inputs` directory contains subdirectories with the input datasets to this benchmark.
Each subdirectory contains 2 files, one for each input variable.
The file were generated with the following parameters:

| folder       | # samples | A distribution | B distribution |
|--------------|----------:|---------------:|---------------:|
| `gaussian-1` |      5000 |  Gauss( 5, 10) |  Gauss(-5, 10) |
| `gaussian-2` |      5000 |   Gauss(10, 1) |   Gauss( 5, 1) |
| `test`       |       100 |   Gauss(10, 1) |   Gauss( 0, 1) |
| `laplace-1`  |      5000 | Laplace(5, 10) | Laplace(-5,10) |
| `laplace-2`  |      5000 | Laplace(10, 1) | Laplace( 5, 1) |
| `uniform`    |      5000 | Uniform(20,25) | Uniform( 5,10) |


[^0]: Vasileios Tsoutsouras, Orestis Kaparounakis, Bilgesu Arif Bilgin, Chatura Samarakoon, James Timothy Meech, Jan Heck, Phillip Stanley-Marbell: The Laplace Microarchitecture for Tracking Data Uncertainty and Its Implementation in a RISC-V Processor. MICRO 2021: 1254-1269
