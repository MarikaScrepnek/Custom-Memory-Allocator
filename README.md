# Custom Memory Allocator

**Custom Memory Allocator** is a C-based project that implements a custom dynamic memory manager similar to `malloc()` and `free()`.  
It demonstrates **heap management, memory allocation strategies, and memory optimization techniques**.

## Highlights

- **Custom Memory Allocation:** Implements `alloc()` and `dealloc()` without using `malloc()`.  
- **Allocation Strategies:** Supports **First-Fit, Best-Fit, and Worst-Fit** algorithms for choosing free blocks.  
- **Heap Management:** Uses `sbrk()` to manage heap memory and grow it in fixed increments.  
- **Coalescing Free Blocks:** Merges contiguous free blocks to reduce fragmentation.  
- **Allocator Configuration:** `allocopt()` sets strategy and heap limits; `allocinfo()` provides memory statistics.  

## Tech Stack

- **Language:** C  
- **Build System:** CMake  
- **Debugging Tools:** CGDB, Valgrind, sanitizers  

## Project Structure

```
src/ # Source code (allocator and test cases)

include/ # Header files

CMakeLists.txt # Build configuration

.gitignore # Clean build ignores

README.md # Project documentation
```


## Getting Started

```bash
git clone https://github.com/marikascrepnek/custom-memory-allocator.git
cd custom-memory-allocator
mkdir build && cd build
cmake ..
make
./main  # Runs test cases
```

## Skills Demonstrated

- Implementing low-level memory management in C
- Writing custom allocation strategies (First-Fit, Best-Fit, Worst-Fit)
- Using system calls (sbrk) to manage heap memory
- Coalescing free memory blocks to reduce fragmentation
- Debugging memory issues with CGDB, Valgrind, and sanitizers
- Building and linking C projects with CMake
