# Explanation and Analysis of Two-Sum Algorithms

## :fist:Brute Force

```javascript
function(nums, target){
  for(i=0; i<nums.length; i++){
    for(j=0; j<nums.length; j++){
      if(nums[i]+nums[j]==target && i!=j) return [i,j];
    }
  }
}
```

### Explanation
In this solution we iterate through  and compare every element of our array with every other element of the array. If the indices do not match and the two values add up to our target we return the two indices.

### Complexity Analysis
#### Time Complexity: O(n<sup>2</sup>) 

We arrive at a time complexity of O(n<sup>2</sup>) because the number of comparisons our algorithm requires scales according to the input *n*, by a factor of *n*<sup>2</sup>.  

#### Space Complexity: O(1)

The only data structures our algorithm requires is an array of length 2 and two iterators (*i*, *j*). Therefore the space complexity is constant or O(1).

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
This algorithm creates a hash map where each element of our array is the key and the index of said element is the value for said key. We then iterate over our array and obtain the necessary integer which will sum to our target with the integer currently being iterated upon. If the integer obtained is a key in our hash map we will then return the current index for our array and the index (or value) of the key which will sum to our target. 
#### Complexity Analysis
Time Complexity: O(n)  
Space Complexity: O(n)
