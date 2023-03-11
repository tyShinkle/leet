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
