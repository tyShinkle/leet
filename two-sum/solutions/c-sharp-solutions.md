# C# Solutions

## :fist: Brute Force

```c#
public class Solution {
    public int[] TwoSum (int[] nums, int target) {
        for (int i = 0; i < nums.Length; i++) {
            for (int j = i + 1; j < nums.Length; j++) {
                if(nums[i] + nums[j] == target) return new int[]{i, j};
            }
        }
        return Array.Empty<int>();
    }
}
```

## :stopwatch: Optimization

```c#
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
    Dictionary<int, int> map = new Dictionary<int, int>();
    for (int i = 0; i < nums.Length; i++) {
        int complement = target - nums[i];
        if (map.ContainsKey(complement)) {
            return new int[] {map[complement],i};
        }
        map[nums[i]] = i;
    }
    throw new Exception("No two sum solution");
    }
}
```
