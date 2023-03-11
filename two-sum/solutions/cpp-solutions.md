# C++ Solutions 

## :fist: Brute Force

```c++
class Solution {
public:
    //notice we pass the input vector by reference as it is more memory efficient
    vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> answer;

        for(int i=0; i<nums.size(); i++)
        {
            for(int j=i+1; j<nums.size(); j++)
            {
                if(nums[i]+nums[j]==target)
                {
                    answer.insert(answer.end(),{i,j});
                }
            }
        }
        return answer;
    }
};
```

## :stopwatch: Optimization

```c++
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        
        unordered_map<int,int> map;

        for(int i=0; i<nums.size(); i++){
            // note: map.find() defaults to returning map.end if the argument is not found.
            if(map.find(target-nums[i]) != map.end()){
                return {i, map[target-nums[i]]};
            }
            map[nums[i]] = i;
        }
        return{};
    }
};
```
