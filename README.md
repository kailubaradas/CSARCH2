# CSARCH2

**Project Overview**
This project is a cache simulation system designed for CSARCH2, implementing an 8-way Set-Associative Cache with the Most Recently Used (MRU) replacement policy. The simulator allows users to analyze different memory access patterns and observe cache performance through a graphical user interface (GUI).

**Features**

* GUI-Based Cache Simulation using Tkinter
*  Configurable Memory Size (Minimum 1024 memory blocks)
* Supports 3 Test Cases: Sequential, Random, and Mid-Repeat
* Displays Simulation Logs, Cache Snapshot, and Performance Metrics
* Implements MRU Replacement Policy

**How to Run the Simulation**

 1. Installation

Ensure you have Python 3 installed. If not, download it from python.org. Install required dependencies:

pip install tkinter

 2. Running the GUI

Clone this repository:

git clone https://github.com/your-repo/cache-simulator.git
cd cache-simulator

3. Run the simulation script:

python3 CSARCH2_Simulation.py

Select a test case (Sequential, Random, or Mid-Repeat) and click Run Simulation.


**Test Case Analysis**

1. Sequential Access (Expected High Hit Rate)

* Pattern: Accesses memory in a strict sequence (0,1,2...63), repeated 4 times.
* Performance: High hit rate because previously loaded blocks remain in cache.
* Best-case scenario for cache utilization.

2. Random Access (Expected Low Hit Rate)

The **random test case** simulates **unpredictable memory access patterns**, where the cache accesses **128 randomly generated memory blocks**. The cache is **8-way set associative** with the **Most Recently Used (MRU) replacement policy**.  

* Pattern: Accesses 128 random memory blocks across 2048 total blocks.
* Performance: High miss rate because random blocks are rarely reused.
* Worst-case scenario for caching. MRU policy frequently replaces blocks before they are reused.

_takeaways_
* In random access, memory blocks are chosen unpredictably so blocks stored in the cache **are rarely reused** before being evicted.  
* MRU replacement fails because it removes recently used blocks, which might still be needed.
* The average memory access time is extremely high because almost every access requires slow main memory retrieval.
* A different cache policy (like LRU) or a larger cache size could improve performance slightly, but random access will always be inefficient.  

3. Mid-Repeat Access (Expected Medium Hit Rate)

* Pattern: Alternates between a small repeating sequence and a new sequence.
* Performance: Moderate hit rate, better than random but worse than sequential.
* Some reuse helps cache performance, but MRU still causes unnecessary evictions.


**Demo Video**

📌 https://drive.google.com/file/d/1iUsR9FO7nTqhrW2qUCjv81EIETWt4t5f/view?usp=sharing

**Contributors**

Group 7 - CSARCH2


Arucan, Oliver
Baradas, Kailu
Mustapha, Michael
Ordinario, Karl

