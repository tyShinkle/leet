# Python Solutions 
## :fist: Brute Force

```python
def twoSum(nums:List[int], target:int) -> List[int]:

    for i in range(len(nums)):
        for j in range(i + 1, len(nums)):
            if nums[i] + nums[j] == target:
                return [i, j]
```

## :stopwatch: Optimizations

```python
  def twoSum(nums:List[int], target:int) -> List[int]:
  
      sums = []
      hashTable = {}
  
      for i in range(len(nums)):
          complement = target - nums[i]
          if complement in hashTable:
              return [hashTable[complement], i]
          hashTable[nums[i]] = i
```
