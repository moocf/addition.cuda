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
# OUTPUT
a = 1, b = 2
a + b = 3 (GPU)
```

See [main.cu] for code, [main.ipynb] for notebook.

[main.cu]: main.cu
[main.ipynb]: https://colab.research.google.com/drive/1kXU6McTQy6oXSt4pplir0x7o8o4HrP0q?usp=sharing


### references

- [CUDA by Example :: Jason Sanders, Edward Kandrot](http://www.mat.unimi.it/users/sansotte/cuda/CUDA_by_Example.pdf)
