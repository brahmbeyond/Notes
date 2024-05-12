# PARALLELISM IN UNIPROCESSOR 


![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/8f4b430c-36ed-4756-8e30-0f6bcc8d3c00)

![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/56a9d180-ec25-4b70-bcb6-22e111151ed8)


![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/9e391d7b-b684-4686-87db-7cd68f43e45b)

![image](https://github.com/brahmbeyond/Notes-App/assets/65112908/7c57acf7-09c3-41b0-b4bd-bf3cd7a6c68f)

----
## 2. Parallelism and Pipelining within CPU
**Parallelism within CPU:**

1. **Parallel Adders:**
   - Imagine you have two numbers that you want to add together, but they're really long (like hundreds or thousands of bits).
   - Parallel adders are like super-fast calculators inside the CPU that can add these long numbers really quickly.
   - They work by breaking down the addition into smaller chunks and processing them simultaneously, or in parallel.
   - There are different techniques for building parallel adders, such as carry-lookahead and carry-save, which make the addition process even faster.

2. **Multiplication Recoding:**
   - When you multiply two numbers, it can sometimes involve complex calculations.
   - To make this process simpler and faster, the multiplier (the number you're multiplying by) can be changed or "recoded" in a way that makes the calculation easier.
   - This helps speed up the multiplication process inside the CPU.

**Pipelining within CPU:**

1. **Instruction Execution Phases:**
   - When the CPU carries out instructions (like adding numbers or multiplying), it goes through different phases or steps.
   - Pipelining is a technique where these phases are overlapped. Instead of waiting for one instruction to finish completely before starting the next one, the CPU starts processing multiple instructions at the same time.
   - This helps improve the overall speed of instruction execution.

2. **Techniques to Overcome Overlapping:**
   - Sometimes, when instructions are processed in parallel, they might overlap in a way that causes problems.
   - To avoid these problems, techniques like instruction prefetch and data buffers are used.
   - Instruction prefetch means fetching the next instructions ahead of time so they're ready to go when needed.
   - Data buffers are like temporary storage areas where data can be held temporarily to prevent conflicts or confusion during processing.

In simple terms, parallelism and pipelining in the CPU are about making calculations and executing instructions faster by doing things simultaneously and efficiently. It's like having multiple workers in a factory who can do different parts of a job at the same time, speeding up the production process.
----

## 3. Overlapped CPU and I/O Operation

Certainly! Let's simplify this:

**Overlapped CPU and I/O Operation:**

1. **I/O Controllers or I/O Processors:**
   - When your computer needs to do something like read from a disk or send data to a printer, it's called an Input/Output (I/O) operation.
   - Normally, the CPU (the brain of the computer) would have to wait for these I/O operations to finish before it can do anything else.
   - But to save time, we can use special helpers called I/O controllers or I/O processors. These are like assistants that handle the I/O tasks separately from the CPU.
   - So, while the CPU is busy with its own tasks, these helpers can take care of the I/O operations simultaneously.

2. **Direct Memory Access (DMA):**
   - Sometimes, when transferring data between an I/O device (like a hard drive or a network card) and the main memory (where all the data is stored), we can use a shortcut called Direct Memory Access (DMA).
   - Instead of the CPU having to oversee every single byte of data transfer, DMA allows the I/O device to directly access the main memory and transfer data without bothering the CPU.
   - This frees up the CPU to focus on other tasks while the data transfer happens in the background, making everything faster and more efficient.

In simple terms, when your computer needs to do things like read from a disk or send data to a printer, it doesn't have to stop everything else it's doing. Special helpers called I/O controllers or I/O processors can handle these tasks separately, while Direct Memory Access (DMA) lets devices transfer data directly to and from memory without bothering the CPU. This helps everything run smoother and faster!

----------

## 4. Use Hierarchical Memory System

**Using a Hierarchical Memory System:**

1. **Speed Difference Between CPU and Memory:**
   - CPUs are super fast at processing information, but there's a problem: the memory they use to store and retrieve data isn't as quick.
   - This speed difference means the CPU often has to wait for data to be fetched from memory, which slows down overall performance.

2. **Hierarchical Memory System:**
   - To tackle this issue, we use a hierarchical memory system, which is like having different levels of memory arranged in layers, with each layer being faster but smaller than the one below it.
   - At the top of this hierarchy is the CPU's registers. These are tiny, super-fast memory locations built directly into the CPU.
   - Just below that is the cache memory. Cache memory is still very fast and is used to store data and instructions that the CPU is likely to need soon. It acts as a buffer between the CPU and the main memory.
   - The main memory comes next. This is larger but slower than cache memory. It holds the programs and data that are currently being used by the CPU.
   - Finally, at the bottom of the hierarchy, we have other types of storage like hard drives or solid-state drives (SSDs). These are much slower than main memory but can store a lot more data.

By organizing memory in this hierarchical way, we ensure that the CPU can quickly access the data it needs most often from the fastest memory locations, while still having access to larger storage when necessary. This helps to bridge the speed gap between the CPU and memory, improving overall performance.

------
## 5. Balancing of Subsystem Bandwidth
