leetcode-35. Search Insert Position <br>
====
Description: . <br>
---
    /**
     * @param {number[]} nums
     * @param {number} target
     * @return {number}
     */
    var searchInsert = function(nums, target) {
        if (nums.length < 1) return ;
        if (nums[0] >= target) return 0;
        for (let i = 0, len = nums.length; i < len - 1; ++i) {
            if ((nums[i] - target) * (nums[i + 1] - target) <= 0) return i + 1;
        }
        return nums.length;
    };
---
