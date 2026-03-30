# Problem


## Code (C++)
```cpp
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int n = nums.size();
        for(int pass = 0; pass < n; pass++) {
            for(int i = 0; i < n - 1; i++) {
                if(nums[i] == 0) {
                    swap(nums[i], nums[i + 1]);
                }
            }
        }
    }
};