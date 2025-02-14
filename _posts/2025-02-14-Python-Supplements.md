---
categories: python, performance
---
![Iodine Pills](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f1/Iodine_pills.jpg/1280px-Iodine_pills.jpg)
Image Courtesy: Wikipedia
# `@cache`
[`@cache`](https://docs.python.org/3/library/functools.html) turned out a superpower, to get that TLE code to pass. Only had to add a [`__hash__`](https://docs.python.org/3.9/reference/datamodel.html#object.__hash__) for correct cache lookups. Without it, it looked like an `Unhashable type`.

```python
class Less:

    def __init__(self):
        self.nums = []
    
    def add(self, num: int) -> None:
        self.nums.append(num)
    
    def __hash__(self):  # <<<<<<<<
        return hash(len(self.nums))

    @cache               # <<<<<<<<
    def get(self, k: int) -> int:
        return list(itertools.accumulate(self.nums[-1*k:], operator.mul))[-1]
```

# `bisect`
Another hack for getting the TLE to pass. Used the `find_gt` example from [`bisect`](https://docs.python.org/3/library/bisect.html) to replace multiple linear list lookups by `O(lg(n))`

```python
class Less:
    def minOperations(self, nums: List[int], k: int) -> int:
        nums.sort()
        ...
        while True:
            if nums[0] >= k:
                return operations

            x, y = nums[:2]
            z = min(x, y) * 2 + max(x, y)
            if len(nums) == 2 or z < nums[0]:
                nums[1] = z
                nums.pop(0)
            else:
                i = bisect.bisect_right(nums, z) # <<<<<<<<
                nums.insert(i, z)
                nums.pop(0)
                nums.pop(0)

            operations = operations+1
```

