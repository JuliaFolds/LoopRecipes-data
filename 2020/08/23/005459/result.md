# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/LoopRecipes.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Aug 2020 - 00:53
    - Baseline: 23 Aug 2020 - 00:54
* Package commits:
    - Target: a71aeb
    - Baseline: 3d1720
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
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 0.77 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` | 0.64 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   | 0.38 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  | 0.38 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   | 0.62 (5%) :white_check_mark: |   1.00 (1%)  |
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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      14398 s          0 s        952 s       6529 s          0 s
       #2  2800 MHz       6332 s          0 s       1009 s      15119 s          0 s
       
  Memory: 7.7900238037109375 GB (6130.26953125 MB free)
  Uptime: 228.0 sec
  Load Avg:  1.03857421875  0.55908203125  0.22900390625
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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      15977 s          0 s        977 s      11860 s          0 s
       #2  2800 MHz      11682 s          0 s       1046 s      16673 s          0 s
       
  Memory: 7.7900238037109375 GB (6104.90625 MB free)
  Uptime: 297.0 sec
  Load Avg:  1.009765625  0.65380859375  0.28857421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 0:53
* Package commit: a71aeb
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
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 768.324 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 882.709 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.952 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   2.288 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   8.594 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   7.928 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 108.705 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` |  66.816 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |  21.113 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |  29.014 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   |  57.984 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |  52.279 ns (5%) |         |                  |             |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      14398 s          0 s        952 s       6529 s          0 s
       #2  2800 MHz       6332 s          0 s       1009 s      15119 s          0 s
       
  Memory: 7.7900238037109375 GB (6130.26953125 MB free)
  Uptime: 228.0 sec
  Load Avg:  1.03857421875  0.55908203125  0.22900390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/LoopRecipes.jl*

## Job Properties
* Time of benchmark: 23 Aug 2020 - 0:54
* Package commit: 3d1720
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
| `["prefetch", ":n => 16384", ":impl => :base"]`   | 734.735 μs (5%) |         |                  |             |
| `["prefetch", ":n => 16384", ":impl => :folds"]`  | 878.708 μs (5%) |         |  511.98 KiB (1%) |       16384 |
| `["prefetch", ":n => 32768", ":impl => :base"]`   |   1.867 ms (5%) |         |                  |             |
| `["prefetch", ":n => 32768", ":impl => :folds"]`  |   2.276 ms (5%) |         | 1023.98 KiB (1%) |       32768 |
| `["prefetch", ":n => 65536", ":impl => :base"]`   |   8.202 ms (5%) |         |                  |             |
| `["prefetch", ":n => 65536", ":impl => :folds"]`  |   7.698 ms (5%) |         |    2.00 MiB (1%) |       65536 |
| `["sparse_dot", ":n => 1024", ":impl => :base"]`  | 142.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 1024", ":impl => :folds"]` | 104.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :base"]`   |  55.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 256", ":impl => :folds"]`  |  77.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :base"]`   |  93.000 ns (5%) |         |                  |             |
| `["sparse_dot", ":n => 512", ":impl => :folds"]`  |  90.000 ns (5%) |         |                  |             |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      15977 s          0 s        977 s      11860 s          0 s
       #2  2800 MHz      11682 s          0 s       1046 s      16673 s          0 s
       
  Memory: 7.7900238037109375 GB (6104.90625 MB free)
  Uptime: 297.0 sec
  Load Avg:  1.009765625  0.65380859375  0.28857421875
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

    Architecture:          x86_64
    CPU op-mode(s):        32-bit, 64-bit
    Byte Order:            Little Endian
    CPU(s):                2
    On-line CPU(s) list:   0,1
    Thread(s) per core:    2
    Core(s) per socket:    1
    Socket(s):             1
    NUMA node(s):          1
    Vendor ID:             GenuineIntel
    CPU family:            6
    Model:                 85
    Model name:            Intel(R) Xeon(R) CPU
    Stepping:              7
    CPU MHz:               2800.174
    BogoMIPS:              5600.34
    Hypervisor vendor:     KVM
    Virtualization type:   full
    L1d cache:             32K
    L1i cache:             32K
    L2 cache:              1024K
    L3 cache:              33792K
    NUMA node0 CPU(s):     0,1
    Flags:                 fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single ssbd ibrs ibpb stibp ibrs_enhanced fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt clwb avx512cd avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves arat avx512_vnni arch_capabilities
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU                                       |
| Vendor             | :Intel                                                     |
| Architecture       | :Skylake                                                   |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00      |
| Cores              | 1 physical cores, 2 logical cores (on executing CPU)       |
|                    | Hyperthreading detected                                    |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 33792) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 46 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, KVM                                                   |

