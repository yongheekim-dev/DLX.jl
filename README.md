# DLX.jl
Dancing Link Algorithem for squares (only works for squares) 

## Installation

```julia
pkg> add https://github.com/yongheekim-dev/DLX.jl.git
```

## Usage
DancingLink sorts sets by square area, then try to fit each square. 
And If sqaure cannot be fit into the 'world`, Trys again with different combination. 
* TODO: Currently if any square cannot fit into the world, it just stops at there. but It should try to fit other suqares if possible.   

``` julia
using DLX

world = (10, 10)
sets = [(2,2), (3,5), (10, 1), (4,2), (1,3), (6,5), (4,4), (2,3), (2,2)]

a = DancingLink(world, sets)
#=
DancingLink - 10×10 Array{Integer,2}:
 1  1  1  1  1  2  2  2  2  4
 1  1  1  1  1  2  2  2  2  4
 1  1  1  1  1  2  2  2  2  4
 1  1  1  1  1  2  2  2  2  4
 1  1  1  1  1  3  3  3  3  4
 1  1  1  1  1  3  3  3  3  4
 5  5  6  6  6  3  3  3  3  4
 5  5  6  6  6  7  7  8  8  4
 5  5  9  9  9  7  7  8  8  4
 5  5  0  0  0  0  0  0  0  4
Members:[(6, 5),(4, 4),(3, 5),(10, 1),(4, 2),(2, 3),(2, 2),(2, 2),(1, 3)]
=#
is_solved(a) #true

```
