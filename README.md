# VmaxFuzz: Seed Selection For Variables Indicating The Scale Of Memory Operation

github:

Developed by Cai Chunfang .

## 1) Project 

Out-of-Bound is a kind of dangerous and common vulnerability in programs. The software does not restrict or incorrectly restricts operations within the boundaries of memory that is accessed using an index or pointer. In some complex cases, to trigger the out of bounds errors not only needs to satisfy control flow conditions, but also data conditions. In these cases, the scale of memory operation should exceed the memory boundary or specific range. However, detecting such vulnerability is challenging, as the state-of-the-art fuzzing techniques focus on code coverage but not memory operation and scale, failing to give additional energy to test cases which changed the memory scale. To achieve higher efficiency on detecting this kind of out-of-bound errors with grey-box fuzzing, we introduced memory scale indicating variable, shortly MemsVar, which is the variable that indicates the index, pointer or size of a memory operation in a program. The MemsVar were instrumented to monitor the change of memory operation scale. We then proposed a seed metric for MemsVar. With this metric, test cases which updated the actual range of MemsVar were kept as effective seeds, thus guiding the scale of memory operation to exceed the memory boundary or specific range and triggering memory out-of-bound errors quickly. Finally, based on the proposed seed metric, we designed a gray box fuzzer named Vmaxfuzz, implemented on the basis of AFL.

## 2) The afl-fuzz approach



## 3) Instrumenting programs for use with AFL



## 4) Instrumenting binary-only apps



## 5) Choosing initial test cases



## 7) Interpreting output



## 8) Parallelized fuzzing



## 9) Fuzzer dictionaries



## 10) Crash triage



## 11) Going beyond crashes



## 12) Common-sense risks



## 13) Known limitations & areas for improvement

