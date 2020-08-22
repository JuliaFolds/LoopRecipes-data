# Benchmark result

* Pull request commit: [`2a2b91b631d474598ca1d938a53bd65c8abbeca0`](https://github.com/JuliaFolds/LoopRecipes.jl/commit/2a2b91b631d474598ca1d938a53bd65c8abbeca0)
* Pull request: <https://github.com/JuliaFolds/LoopRecipes.jl/pull/13> (Use VectorizationBase)

# Judge result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Aug 2020 - 20:16
    - Baseline: 22 Aug 2020 - 20:17
* Package commits:
    - Target: 6f0ceb
    - Baseline: c49b41
* Julia commits:
    - Target: 96786e
    - Baseline: 96786e
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: None
    - Baseline: None

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                | time ratio                   | memory ratio |
|---------------------------------------------------|------------------------------|--------------|
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |                1.09 (5%) :x: |   1.00 (1%)  |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |                1.13 (5%) :x: |   1.00 (1%)  |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |                1.44 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  |                1.33 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` |            63394.52 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |            26983.95 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |            29320.28 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   | 0.64 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |            51824.24 (5%) :x: |   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["prefetch", ":n => 16384"]`
- `["prefetch", ":n => 32768"]`
- `["prefetch", ":n => 65536"]`
- `["sparse_dot", ":n => 1024"]`
- `["sparse_dot", ":n => 256"]`
- `["sparse_dot", ":n => 512"]`

## Julia versioninfo

### Target
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10754 s          0 s       1351 s       9809 s          0 s
       #2  2095 MHz       8661 s          0 s       1306 s      12725 s          0 s
       
  Memory: 6.764881134033203 GB (3154.296875 MB free)
  Uptime: 241.0 sec
  Load Avg:  1.10986328125  0.7900390625  0.35009765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      11580 s          0 s       1382 s      15855 s          0 s
       #2  2095 MHz      14725 s          0 s       1351 s      13518 s          0 s
       
  Memory: 6.764881134033203 GB (3160.1796875 MB free)
  Uptime: 310.0 sec
  Load Avg:  1.03515625  0.833984375  0.396484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 22 Aug 2020 - 20:16
* Package commit: 6f0ceb
* Julia commit: 96786e
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                | time            | GC time | memory           | allocations |
|---------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 697.916 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 673.815 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.534 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   1.554 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   4.411 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   5.497 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 132.960 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` |  63.395 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |  26.984 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |  29.320 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   |  64.278 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |  51.824 ns (5%) |         |                  |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["prefetch", ":n => 16384"]`
- `["prefetch", ":n => 32768"]`
- `["prefetch", ":n => 65536"]`
- `["sparse_dot", ":n => 1024"]`
- `["sparse_dot", ":n => 256"]`
- `["sparse_dot", ":n => 512"]`

## Julia versioninfo
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      10754 s          0 s       1351 s       9809 s          0 s
       #2  2095 MHz       8661 s          0 s       1306 s      12725 s          0 s
       
  Memory: 6.764881134033203 GB (3154.296875 MB free)
  Uptime: 241.0 sec
  Load Avg:  1.10986328125  0.7900390625  0.35009765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 22 Aug 2020 - 20:17
* Package commit: c49b41
* Julia commit: 96786e
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                | time            | GC time | memory           | allocations |
|---------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 728.057 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 666.248 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.548 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   1.430 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   3.892 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   3.822 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 100.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` |   0.001 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |   0.001 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |   0.001 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   | 100.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |   0.001 ns (5%) |         |                  |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["prefetch", ":n => 16384"]`
- `["prefetch", ":n => 32768"]`
- `["prefetch", ":n => 65536"]`
- `["sparse_dot", ":n => 1024"]`
- `["sparse_dot", ":n => 256"]`
- `["sparse_dot", ":n => 512"]`

## Julia versioninfo
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      11580 s          0 s       1382 s      15855 s          0 s
       #2  2095 MHz      14725 s          0 s       1351 s      13518 s          0 s
       
  Memory: 6.764881134033203 GB (3160.1796875 MB free)
  Uptime: 310.0 sec
  Load Avg:  1.03515625  0.833984375  0.396484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.210
    BogoMIPS:            4190.42
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

