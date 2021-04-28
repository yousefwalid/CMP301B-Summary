# Introduction

A program performance is affected by:

- Algorithm
- Programming Language, Compiler, Architecture...
- Processor and Memory 
- I/O system

## Eight great ideas in Computer Architecture

1. Design for Moore's law
    - We need to anticipiate where the technology will be when the design finishes, instead of where it starts.
2. Use Abstraction to simplify design
    - Use abstraction to hide low level details to simplify models at a higher level
3. Make the common case fast
    - Making common case faster will better enhance the performance
4. Performance via Parallelism
    - Use parallelism to enhance your performance
5. Performance via Pipelining
    - Use pipelining (parallelism on the level of instructions) to enhance performance
6. Performance via Prediction
    - It is better to predict and be right sometimes than to do nothing at all
7. Hierarchy of memories
    - Use different level of memories with different speeds
8. Dependability via Redundancy
    - Add redundant components to make system realiable

# Performance

When measuring CPUs' performance, we are concerned with:
- Reponse time
  - How long does it take for the job to run?
- Throughput
  - How many jobs can the machine run at the same time?

## Execution Time

- $ET$: Execution time
- $IC$: Instruction count for a program
- $CPI$: Cycles per instruction
- $CR$: Cycles per second
- $CT$: Cycle time

---

- $\text{Perf}_X = \dfrac{1}{\text{ET}_X}$
- $\dfrac{\text{Perf}_X}{\text{Perf}_Y} = n$, X is n times faster than Y
- $ET = \dfrac{IC * CPI}{CR}$
- $CR = \dfrac{1}{CT}$
- $\text{\# Cycles} = CPI * IC$
- $CT = \dfrac{ET}{\text{\# Cycles}}$
- $\text{Speed up} = \dfrac{\text{Perf}_{new}}{\text{Perf}_{old}} = \dfrac{\text{ET}_{old}}{\text{ET}_{new}}$ 
- $\text{Percentage of Speed Improved} = (\dfrac{Perf_{new}}{Perf_{old}} - 1) * 100 = (\dfrac{ET_{old} - ET_{new}}{ET_{new}}) * 100$
- $\text{Percentage of improvement / Reduction of ET} = (1 - \dfrac{ET_{new}}{ET_{old}}) * 100$
- $\text{Total time after improvement (Amadahl's Law)} = \text{unaffected time} + \dfrac{\text{time that could be improved}}{\text{amount of partial speedup}}$


**Note**: changing the cycle time often changes the
number of cycles required for various instructions
## Components Analysis
Which component affects what?

![](assets/perf_components_analysis.png)

## Pitfalls

1. Using a subset of the performance equation as a performance measure
2. Expecting the improvement of overall performance by the same ratio of improvement of one aspect

