"""
These are the learning from the book  - Effective Python
"""


Index:

1. Pythonic Thinking
        - Know the diff between bytes, str and unicode
        - write helper functions instead of complex equations
        - using slice sequences
        - avoid start,end stride on a single slice
        - use list comprehension instead of map/filter
        - avoid more than two expressions in a list comprehension
        - prefer enumerate over range
        - use zip to iterate over iterators in parallel
        - avoid else block after for/while loop
        - make use of try/except/else/finally paradigm       
2. Functions
        - use exceptions over returning None
        - Understanding how closures interact with variable scopes
        - Consider generators instead of returning lists
        - be defennsive when iterating over arguments
        - reduce variable noise with variable positional arguments
        - provide optional behavior with keywork arguments
        - use docstring, None to specify dynamic default arguments
        - enforce clarity with keyword only arguments
3. Classes and Inheritence
        - use helper classes over dictionaries/tuples
        - accept functions for simple interfaces instead of classes
        - use @classmethod polymorphism to construct object genericly
        - intialize parent class with super
        - use multiple inherintance only for mix-in utility classes
        - prefer public attributes over private ones
4. Metaclass and Attributes
        - use plain attributes instead of get/set
        - consider @property instead of refactoring attributes
        - use descriptors for reusable @property methods
        - use __getattr__, __getattribute__ for lazy attributrs
        - validate subclasses with metaclasses
        - register class existance with metaclasses
        - annotate class attributes with metaclasses
5. Concurrency and Parallelism
        - use subprocess to manage child process
        - threads for blocking I/O, avoid for parallelism
        - use locks to prevent data races in threads
        - use queues to co-ordinate work between threads
        - co-routines to run many functions concurrently
        - concurrent.futures for true parallelism
6. Built-in Modules
        - define function decorators with functools.wraps
        - use contextlib and with statements to re-use try/finally
        - make pickle reliable with copyreg
        - use datetime instead of local clocks
        - built-in ds and algo        
7. Collaboration
        - write docstring for every function, class and module
        - use packages to organize modules and classes
        - define root exception to insulate caller from APIs [security]
        - Breaking circular dependency
        - use virtual environments
8. Prouduction
        - module scoped code for depolyment configuirations
        - repr strings for debugging output
        - test everything with unittest
        - iterative debugging with pdb
        - profile before optimizing
        - tracemalloc to understand memory allocation and leaks