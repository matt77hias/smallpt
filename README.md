# smallpt

## About
The Rosetta smallpt project: the same path tracer written in multiple languages

<p align="center"><img src="https://github.com/matt77hias/smallpt/blob/master/res/image.png" ></p>

## Features
**Current languages**:

* [C](https://github.com/matt77hias/c-smallpt)
* [C++](https://github.com/matt77hias/cpp-smallpt)
* [C#](https://github.com/matt77hias/cs-smallpt)
* [CUDA](https://github.com/matt77hias/cu-smallpt)
* [Erlang](https://github.com/matt77hias/erl-smallpt)
* [Java](https://github.com/matt77hias/java-smallpt)
* [J#](https://github.com/matt77hias/jsl-smallpt)
* [Prolog](https://github.com/matt77hias/pl-smallpt)
* [Python 2.7/3.5](https://github.com/matt77hias/py-smallpt)
* [Python 2.7/3.5 + NumPy](https://github.com/matt77hias/numpy-smallpt)
* [Racket](https://github.com/matt77hias/rkt-smallpt)

**Possible future languages**:
* Haskell, J++, JavaScript, TypeScript, Matlab, etc.

## Performance comparison
In order to give a very rough performance comparison, the wall clock time is measured of a single run to generate an image of resolution 512x512 using 64spp. All single process - single threads experiments output the current progression to standard output. All multi process - multi threaded experiments do not output the current progression to standard output (this can change in the future).

**System**:
* OS: Windows 8.1 Pro 64 Bit
* CPU: Intel i7-4770K @ 3,50 GHz (TB @ 3,9 GHz) with 8GB DDR3 @ 1600 MHz
* GPU: NVIDIA GeForce GTX 970 with 4 GB GDDR5

**Note**: the ramdom number generators used, differ between the languages and their implementations.

### Single process - Single threaded

| Programming Language | Compiler/Interpreter | Wall clock (64 spp) |
|----------------------|----------------------|---------------------|
| C                    | MSVC++ 14.0          | 00h 02m 11,16s      |
| C++                  | MSVC++ 14.0          | 00h 01m 41,18s      |
| C#                   | CLR 19.00            | 00h 04m 13,24s      |  
| Erlang               | ERTS/BEAM 8.0        | 01h 00m 36,28s      |
| Java                 | JVM 1.8              | 00h 01m 47,89s      |
| J#                   | CLR 14.00            | 00h 06m 14,62s      |
| Prolog               | SWI-Prolog 7.2.3     |                     |
| Python 2.7           | CPython (Anaconda)   | 08h 24m 40,88s      |
| Python 2.7           | CPython (Canopy)     | 08h 35m 03,19s      |
| Python 2.7           | IronPython           | 06h 32m 11,48s      |
| Python 2.7           | PyPy                 |                     |
| Python 3.5           | CPython (Anaconda)   | 09h 37m 05,13s      |
| Python 3.5           | IronPython           | 06h 36m 59,20s      |
| Python 2.7 + NumPy   | CPython (Anaconda)   | 09h 58m 25,18s      |
| Python 2.7 + NumPy   | CPython (Canopy)     | 10h 43m 04,10s      |
| Python 3.5 + NumPy   | CPython (Anaconda)   | 10h 20m 46,47s      |
| Racket               | DrRacket 6.6         | 00h 13m 39,12s      |

### Multi process - Multi threaded

| Programming Language | Compiler/Interpreter | Wall clock (64 spp) |
|----------------------|----------------------|---------------------|
| C++ + OpenMP         | MSVC++ 14.0          | 00h 00m 30,68s      |
| CUDA                 | MSVC++ 14.0/NVCC 8.0 | 00h 00m 13,95s      |
