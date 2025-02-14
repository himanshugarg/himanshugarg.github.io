---
categories: python, performance
---
# `@cache` (with `__hash__`)
@cache turned out a superpower, to get that TLE code to pass. Only had to add a `__hash__` for correct cache lookups. Without it, it looked like an unhashable type.

```python
class Less:

    def __init__(self):
        self.nums = []
    
    def add(self, num: int) -> None:
        self.nums.append(num)
    
    def __hash__(self):
        return hash(len(self.nums))

    @cache
    def get(self, k: int) -> int:
        return list(itertools.accumulate(self.nums[-1*k:], operator.mul))[-1]
```



