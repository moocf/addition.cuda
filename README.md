Addition is the process of calculating the total of two or more
numbers or amounts.

```c
The kernel recieves 3 arguments, the first being global address (GPU) of
where it must store the result. This has to be done because the kernel cant
return any value. The arguments it recieves are managed by CUDA driver and
possibly stored in constant memory (right?). A kernel supports all common
operators along with various math functions.
```

```c
1. Integers "a", "b" are defined in host memory (CPU).
2. Memory for storing their sum is allocated on device memory (GPU).
3. Sum is computed by the kernel, with one thread (async).
4. Wait for kernel to complete, then copy the sum to host memory (cHost).
5. Free the space we had occupied (we are good people).
```

```bash
$ nvcc -std=c++17 -Xcompiler -O3 main.cu
$ ./a.out

# a = 1, b = 2
# a + b = 3 (GPU)
```

See [main.cu] for code.

[main.cu]: main.cu

<br>
<br>


## References

- [CUDA by Example :: Jason Sanders, Edward Kandrot](https://gist.github.com/wolfram77/72c51e494eaaea1c21a9c4021ad0f320)

![](https://ga-beacon.deno.dev/G-G1E8HNDZYY:v51jklKGTLmC3LAZ4rJbIQ/github.com/moocf/addition.cuda)
