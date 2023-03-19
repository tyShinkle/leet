# Javascript Solutions 

## :fist:Brute Force

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
 
var twoSum = function(nums, target) {

    for (let i = 0; i < nums.length; i++) {
        for (let j = 0; j < nums.length; j++) {
            if (nums[i] + nums[j] == target && i != j) return [i,j];
        }
    }
    
};
```

## :stopwatch:Optimization

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
 
var twoSum = function(nums, target) {

    let map = new Map();

    for (let i = 0; i < nums.length; i++) {
        let complement = target - nums[i];
        if (map.has(complement)) {
            return [i, map.get(complement)];
        }
        map.set(nums[i], i);
    }
    
};
    
```

