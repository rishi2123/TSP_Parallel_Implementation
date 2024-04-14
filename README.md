# Travelling Salesman Problem: Parallel Implementations & Analysis

## Course Project for High Performance Computing

***

### Implementations for Different Paradigms of Parallelization

| **Paradigm** | **Tool/Library** | **Implementation** |
| :---: | :---: | :---: |
| Serial | - | `tsp.cpp` |
| Shared Memory | OpenMP | `tsp_omp.cpp` |
| Message Passing | MPI | `tsp_mpi.cpp` |
| Hybrid | MPI & OpenMP | `tsp_hybrid.cpp` |


Following are the list of commands to compile \& run the codes for the various implementations mentioned above:

### Serial

```bash
$ g++ tsp.cpp -o tsp    # Compile
$ ./tsp <N>             # Run the code for N cities
```

### OpenMP

```bash
$ g++ -fopenmp tsp_omp.cpp -o tsp_omp   # Compile
$ ./tsp_omp <N> <N_TH>                  # Run the code for N cities using N_TH number of OpenMP threads
```

### MPI

```bash
$ mpic++ tsp_mpi.cpp -o tsp_mpi         # Compile
$ mpirun -np <N_PES> ./tsp_mpi <N>      # Run the code for N cities using N_PES number of MPI processes
```

### Hybrid

```bash
$ mpic++ -fopenmp tsp_hybrid.cpp -o tsp_hybrid     # Compile
$ mpirun -np <N_PES> ./tsp_hybrid <N> <N_TH>       # Run the code for N cities using N_PES MPI processes, each with N_TH OpenMP threads
```


***
