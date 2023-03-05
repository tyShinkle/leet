# Javascript Solutions 

### :fist:Brute Force

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

#### Explanation
In this solution we iterate through  and compare every element of our array with every other element of the array. If the indices do not match and the two values add up to our target we return the two indices.

#### Complexity Analysis
Time Complexity: O(n<sup>2</sup>)  
Space Complexity: O(1)

***

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
            return [i, mp.get(diff)]
        }
        
        mp.set(nums[i], i)
    }
};
    
```

#### Explanation

#### Complexity Analysis
Time Complexity: O(n)  
Space Complexity: O(n)
