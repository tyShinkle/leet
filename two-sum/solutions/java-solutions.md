# Java Solutions 

## :fist: Brute Force

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i = 0; i < nums.length; i++){
            for(int j = 0; j < nums.length; j++){
                if(nums[i] + nums[j] == target && i != j)
                {
                    return new int[]{i, j};
                }
            }
        }
        return null;
    }
}
```

## :stopwatch: Optimization

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer,Integer> map = new HashMap<>();
        for(int i = 0; i < nums.length; i++){
            int complement = target - nums[i];
            if(map.containsKey(complement)){
                return new int[]{map.get(complement), i};
            }else{
                map.put(nums[i], i);
            }
        }
        return null;
    }
}
```
