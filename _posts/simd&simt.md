#What is SIMD and SIMT and why do they exist?

SIMD (single instruction multiple data) is an abstract parallel computing paradigm that usually 
finds its physical implementation in a form of multiple parallel arithmetic units, often called vector lanes, inside the CPU's ALU. 
When we want to add many different numbers together, it is less efficient to do it one by one, and fetch the instruction in each cycle.
The SIMD is a solution to this problem: it exists to improve performance when performing the same operation on multiple data elements, 
by fetching the instruction once and applying it to multiple data points simultaneously.

In the GPU world, the principle of SIMD (applying one instruction to multiple data elements) still holds,
but the hardware implements it differently. Each warp (also called a wave or sub-group) executes a single instruction across all its threads in parallel. 
This execution model is commonly called SIMT (Single Instruction, Multiple Threads) -> essentially SIMD at the thread level, which can be confusing terminology.
