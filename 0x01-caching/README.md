# Caching Algorithms Project

## Overview
This project focuses on implementing and understanding different caching algorithms. It is part of the ALX Backend curriculum and aims to provide hands-on experience with various cache replacement policies.

## Project Details
- **Start Date:** June 25, 2024, 6:00 AM
- **End Date:** June 27, 2024, 6:00 AM
- **Checker Release:** June 25, 2024, 6:00 PM
- **Auto Review:** At the project deadline

## Background Context
In this project, you will learn and implement various caching algorithms. These algorithms are essential for optimizing data retrieval and enhancing system performance by minimizing the time required to access frequently used data.

## Resources
To successfully complete this project, review the following materials:
- Cache replacement policies - FIFO
- Cache replacement policies - LIFO
- Cache replacement policies - LRU
- Cache replacement policies - MRU
- Cache replacement policies - LFU

## Learning Objectives
By the end of this project, you should be able to explain the following without assistance:
- The concept and purpose of a caching system
- The meanings of FIFO, LIFO, LRU, MRU, and LFU
- The limitations of caching systems

## Requirements
### Python Scripts
- All files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7
- All files should end with a new line
- The first line of all files should be `#!/usr/bin/env python3`
- A `README.md` file at the project root is mandatory
- Code must adhere to the `pycodestyle` style (version 2.5)
- All files must be executable
- File lengths will be tested using `wc`
- All modules, classes, and functions must have proper documentation explaining their purpose

## BaseCaching Class
All your classes must inherit from `BaseCaching` defined as follows:

```python
#!/usr/bin/python3
""" BaseCaching module
"""

class BaseCaching():
    """ BaseCaching defines:
      - constants of your caching system
      - where your data are stored (in a dictionary)
    """
    MAX_ITEMS = 4

    def __init__(self):
        """ Initialize
        """
        self.cache_data = {}

    def print_cache(self):
        """ Print the cache
        """
        print("Current cache:")
        for key in sorted(self.cache_data.keys()):
            print("{}: {}".format(key, self.cache_data.get(key)))

    def put(self, key, item):
        """ Add an item in the cache
        """
        raise NotImplementedError("put must be implemented in your cache class")

    def get(self, key):
        """ Get an item by key
        """
        raise NotImplementedError("get must be implemented in your cache class")
```

## Tasks
### Task 0: Basic Dictionary
Create a class `BasicCache` that inherits from `BaseCaching` and implements a basic caching system with no limits.

### Task 1: FIFO Caching
Create a class `FIFOCache` that inherits from `BaseCaching` and implements a FIFO caching system.

### Task 2: LIFO Caching
Create a class `LIFOCache` that inherits from `BaseCaching` and implements a LIFO caching system.

### Task 3: LRU Caching
Create a class `LRUCache` that inherits from `BaseCaching` and implements an LRU caching system.

### Task 4: MRU Caching
Create a class `MRUCache` that inherits from `BaseCaching` and implements an MRU caching system.

## Repository
- **GitHub Repository:** `alx-backend`
- **Directory:** `0x01-caching`

## Authors and Acknowledgements
This project is developed and maintained by the ALX program. All rights reserved © 2024 ALX.
