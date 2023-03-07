# Javascript Solutions 

## :fist:Brute Force

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
 
var twoSum = function(nums, target) {
    for(let i = 0; i < nums.length; i++){
        for(let j=0; j < nums.length; j++){
            if(nums[i]+nums[j]==target && i!=j) return [i,j];
        }
    }
};
```

### :stopwatch:Optimization

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
 
var twoSum = function(nums, target) {
    let mp = new Map()
    for (let i = 0; i < nums.length; i++) {
        let diff = target - nums[i]
        if (mp.has(diff)) {
            return [i, mp.get(diff)];
        }
        mp.set(nums[i], i);
    }
};
    
```

