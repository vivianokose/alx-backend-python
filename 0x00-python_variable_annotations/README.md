# 0x00. Python - Variable Annotations

## Table of Contents

- [Introduction](#introduction)
- [Learning Objectives](#learning-objectives)
- [Requirements](#requirements)
- [Project Structure](#project-structure)
- [Tasks](#tasks)
  - [Task 0: Basic Annotations](#task-0-basic-annotations)
  - [Task 1: Floor Function](#task-1-floor-function)
  - [Task 2: Concatenate Function](#task-2-concatenate-function)
  - [Task 3: Nested Function Annotations](#task-3-nested-function-annotations)
- [Usage](#usage)
- [Testing](#testing)

## Introduction

This module focuses on variable annotations in Python. Variable annotations provide a way to add type hints to Python code, which can improve code readability and maintainability. Type hints are not enforced at runtime but can be used by static type checkers, IDEs, and other tools to catch potential type-related errors.

## Learning Objectives

By the end of this module, you should be able to:
- Understand the basics of type annotations in Python.
- Use variable annotations for different data types.
- Annotate function parameters and return types.
- Use type hints with complex data structures such as lists and dictionaries.

## Requirements

- Python 3.6 or higher.
- A code editor or IDE that supports Python type hints (e.g., PyCharm, VSCode).

## Project Structure

```
0x00-python-variable_annotations/
│
├── README.md
├── 0-basic_annotations.py
├── 1-floor.py
├── 2-concatenate.py
├── 3-nested_annotations.py
├── tests/
│   ├── test_0-basic_annotations.py
│   ├── test_1-floor.py
│   ├── test_2-concatenate.py
│   └── test_3-nested_annotations.py
└── requirements.txt
```

## Tasks

### Task 0: Basic Annotations

Create a script named `0-basic_annotations.py` that includes examples of basic variable annotations.

```python
# 0-basic_annotations.py

a: int = 5
pi: float = 3.14
is_valid: bool = True
name: str = "ALX"
```

### Task 1: Floor Function

Write a function `floor` in the file `1-floor.py` that takes a float `n` as argument and returns the floor of the float.

```python
# 1-floor.py

import math

def floor(n: float) -> int:
    return math.floor(n)
```

### Task 2: Concatenate Function

Write a function `concatenate` in the file `2-concatenate.py` that takes two strings `str1` and `str2` as arguments and returns their concatenation.

```python
# 2-concatenate.py

def concatenate(str1: str, str2: str) -> str:
    return str1 + str2
```

### Task 3: Nested Function Annotations

Write a function `nested` in the file `3-nested_annotations.py` that demonstrates the use of type hints with complex data structures.

```python
# 3-nested_annotations.py

from typing import List, Tuple, Dict

def nested() -> Tuple[List[int], Dict[str, float]]:
    return ([1, 2, 3], {"pi": 3.14, "e": 2.71})
```

## Usage

To use the scripts in this module, navigate to the module directory and run the script using Python. For example:

```sh
cd 0x00-python-variable_annotations
python 0-basic_annotations.py
```

## Testing

To run the tests for the tasks, navigate to the module directory and use a testing framework like `unittest` or `pytest`. For example:

```sh
pytest tests/test_0-basic_annotations.py
