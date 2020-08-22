# Benchmark result

* Pull request commit: [`82eccfcbf20c40184fdc1e16ba14825fdcc6d696`](https://github.com/JuliaFolds/LoopRecipes.jl/commit/82eccfcbf20c40184fdc1e16ba14825fdcc6d696)
* Pull request: <https://github.com/JuliaFolds/LoopRecipes.jl/pull/13> (Use VectorizationBase)

# Judge result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmarks:
    - Target: 22 Aug 2020 - 20:28
    - Baseline: 22 Aug 2020 - 20:29
* Package commits:
    - Target: a85c16
    - Baseline: 2bd9b4
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
| `["prefetch", ":n => 16384", ":impl => :folds"]`  |                1.08 (5%) :x: |   1.00 (1%)  |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |                1.07 (5%) :x: |   1.00 (1%)  |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |                1.06 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  |                1.36 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` | 0.71 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |            26606.43 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |            27566.40 (5%) :x: |   1.00 (1%)  |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   | 0.64 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  | 0.58 (5%) :white_check_mark: |   1.00 (1%)  |

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
       #1  2095 MHz       4466 s          0 s       1204 s      22920 s          0 s
       #2  2095 MHz      16981 s          0 s       1630 s      10521 s          0 s
       
  Memory: 6.764881134033203 GB (3158.8125 MB free)
  Uptime: 304.0 sec
  Load Avg:  1.03369140625  0.7470703125  0.3388671875
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
       #1  2095 MHz       9974 s          0 s       1246 s      24746 s          0 s
       #2  2095 MHz      18836 s          0 s       1678 s      16002 s          0 s
       
  Memory: 6.764881134033203 GB (3153.4140625 MB free)
  Uptime: 378.0 sec
  Load Avg:  1.04248046875  0.8212890625  0.39794921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 22 Aug 2020 - 20:28
* Package commit: a85c16
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
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 878.841 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 834.538 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.929 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   1.734 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   4.612 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   4.575 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 135.776 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` |  70.566 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |  26.606 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |  27.566 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   |  64.244 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |  57.538 ns (5%) |         |                  |             |

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
       #1  2095 MHz       4466 s          0 s       1204 s      22920 s          0 s
       #2  2095 MHz      16981 s          0 s       1630 s      10521 s          0 s
       
  Memory: 6.764881134033203 GB (3158.8125 MB free)
  Uptime: 304.0 sec
  Load Avg:  1.03369140625  0.7470703125  0.3388671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/LoopRecipes.jl/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 22 Aug 2020 - 20:29
* Package commit: 2bd9b4
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
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 848.724 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 769.321 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.811 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   1.723 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   4.592 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   4.315 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 100.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` | 100.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |   0.001 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |   0.001 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   | 100.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  | 100.000 ns (5%) |         |                  |             |

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
       #1  2095 MHz       9974 s          0 s       1246 s      24746 s          0 s
       #2  2095 MHz      18836 s          0 s       1678 s      16002 s          0 s
       
  Memory: 6.764881134033203 GB (3153.4140625 MB free)
  Uptime: 378.0 sec
  Load Avg:  1.04248046875  0.8212890625  0.39794921875
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
    CPU MHz:             2095.226
    BogoMIPS:            4190.45
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

