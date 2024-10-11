# A repo to explore vectorization

## What is vectorization?

[Stackoverflow answer](https://stackoverflow.com/questions/1422149/what-is-vectorization)

- Modern CPUs have vector or SIMD (Single Instruction, Multiple Data)
instruction sets, which apply the same operation to two, four or more pieces of
data simultaneously (in one CPU instruction).

- "Vectorization" (simplified) is the process of rewriting a loop so that
instead of processing a single element of an array N times, it processes (say) 4
elements of the array simultaneously N/4 times.

## Info on CPUs

Linux:
```bash
lscpu
```

MacOs:
```bash
sysctl -a | grep machdep.cpu
```

### Apple M1

The M1 supports Neon (128-bit) SIMD instructions. It does not support SVE SIMD instructions.

## NumPy

Using NumPy in Python enforces all elements in arrays to be of the _same type_
(in contrast with Python lists which can have arbitrary types). As a result
NumPy can call optimized C functions under the hood. 

## References

- https://towardsdatascience.com/how-to-make-your-pandas-loop-71-803-times-faster-805030df4f06
