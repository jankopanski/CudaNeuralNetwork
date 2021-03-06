# CudaNeuralNetwork
This project is a Fully Connected Neural Network implemented purely in CUDA C.

The neural netrok was trained on [BelgiumTS Dataset](https://btsd.ethz.ch/shareddata/) and used for traffic signs classification.

The purpose of this implementation is to gain a peak performance on a single GeForce GTX 1080 Ti card. It achieves 12.42 times speedup in compartion to 8 core CPU implementation.

### CUDA optimizations
- Matrix multiptications, transpositions and reductions performed in shared memory
- Grid-stride loop technique
- Minimization of data transfer between CPU and GPU
- Constant memory utilization
- Streams and asynchronous kernels
- Grid and block sizes optimized per kernel for GTX 1080 Ti
- Pragma unrolling

### Profiling results
![](./img/nvvp2.png)
![](./img/nvvp1.png)
