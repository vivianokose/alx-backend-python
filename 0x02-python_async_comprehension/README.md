# 0x02. Python - Async Comprehension

## 📋 Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Requirements](#requirements)
4. [Project Structure](#project-structure)
5. [Tasks](#tasks)
6. [Usage](#usage)
7. [References](#references)

## 🌟 Introduction
This project explores asynchronous programming in Python using asynchronous comprehensions. Asynchronous comprehensions allow for more efficient handling of asynchronous operations, such as I/O-bound tasks, by enabling the concurrent execution of code.

## 🎯 Objectives
- Understand the concept of asynchronous comprehensions.
- Implement asynchronous generator functions.
- Use `async for` with comprehensions.

## 📋 Requirements
- Python 3.7+
- `asyncio` module
- Basic understanding of asynchronous programming in Python.

## 🗂️ Project Structure
```
.
├── 0-async_generator.py       # Defines an asynchronous generator function
├── 1-async_comprehension.py   # Implements an async comprehension to collect data from the generator
├── 2-measure_runtime.py       # Measures the runtime of the async comprehension
└── README.md                  # This README file
```

## 📚 Tasks

### Task 0: Async Generator
File: `0-async_generator.py`

🔹 **Description:** Create an asynchronous generator that yields a random number between 0 and 10, 10 times, with a 1-second delay between each yield.

```python
import asyncio
import random

async def async_generator():
    for _ in range(10):
        await asyncio.sleep(1)
        yield random.uniform(0, 10)
```

### Task 1: Async Comprehension
File: `1-async_comprehension.py`

🔹 **Description:** Create an async comprehension that collects 10 random numbers using the `async_generator`.

```python
from typing import List

async def async_comprehension() -> List[float]:
    return [number async for number in async_generator()]
```

### Task 2: Measure Runtime
File: `2-measure_runtime.py`

🔹 **Description:** Create a function that measures the total runtime of executing the `async_comprehension` function four times in parallel.

```python
import time

async def measure_runtime():
    start_time = time.time()
    await asyncio.gather(*(async_comprehension() for _ in range(4)))
    total_time = time.time() - start_time
    return total_time
```

## 🚀 Usage

### Running the Code
1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Run the tasks:**
   - Task 0: `python3 0-async_generator.py`
   - Task 1: `python3 1-async_comprehension.py`
   - Task 2: `python3 2-measure_runtime.py`

### Example
To measure the runtime of the async comprehension:
```bash
python3 2-measure_runtime.py
```

## 📚 References
- [Python Official Documentation](https://docs.python.org/3/library/asyncio.html)
- [PEP 530 – Asynchronous Comprehensions](https://www.python.org/dev/peps/pep-0530/)
- [Real Python – Async IO in Python: A Complete Walkthrough](https://realpython.com/async-io-python/)

Feel free to reach out for any questions or contributions! 🚀
