# 0x02. Python - Async Comprehension

![img](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2019/12/ee85b9f67c384e29525b.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20240319%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240319T104139Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=6d3d31fc6da59b88bd17fae605585e5cc96ea3808b5c08cfdf992eb9df17629c)

This project contains tasks for learning:

+ How to write an asynchronous generator
+ How to use async comprehensions
+ How to type-annotate generators

### Resources

- [PEP 530 – Asynchronous Comprehensions](https://peps.python.org/pep-0530/)
- [What’s New in Python: Asynchronous Comprehensions / Generators](https://www.blog.pythonlibrary.org/2017/02/14/whats-new-in-python-asynchronous-comprehensions-generators/)
- [Type-hints for generators](https://stackoverflow.com/questions/42531143/how-to-type-hint-a-generator-in-python-3)

### Tasks

0. **Async Generator**<br/>[0-async_generator.py](0-async_generator.py) contains an asynchronous coroutine called `async_generator` that takes no arguments and meets the following requirements:
  + The coroutine will loop 10 times, each time asynchronously wait 1 second, then yield a random number between 0 and 10.
  + Use the `random` module

  1. **Async Comprehensions**<br/>[1-async_comprehension.py](1-async_comprehension.py) contains a script that meets the following requirements:
  + Import `async_generator` from the previous task and then write a coroutine called `async_comprehension` that takes no arguments.
  + The coroutine will collect 10 random numbers using an async comprehensing over `async_generator`, then return the 10 random numbers.

2. **Run time for four parallel comprehensions**<br/>[2-measure_runtime.py](2-measure_runtime.py) contains a script that meets the following requirements:
  + Import `async_comprehension` from the previous file and write a `measure_runtime` coroutine that will execute `async_comprehension` four times in parallel using `asyncio.gather`.
  + `measure_runtime` should measure the total runtime and return it.
