Given a sorted array and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.

You may assume no duplicates in the array.

Example 1:

Input: [1,3,5,6], 5
Output: 2

var searchInsert = function(nums, target) {
    if (nums.length < 1) return ;
    if (nums[0] >= target) return 0;
    for (let i = 0, len = nums.length; i < len - 1; ++i) {
        if ((nums[i] - target) * (nums[i + 1] - target) <= 0) return i + 1;
    }
    return nums.length;
};
