Given a sorted array and a target value, return the index if the target is found. If not, return the index where it would be<br>if it were inserted in order.<br>

You may assume no duplicates in the array.<br>

Example 1:<br>

Input: [1,3,5,6], 5<br>
Output: 2<br>

var searchInsert = function(nums, target) {<br>
    if (nums.length < 1) return ;<br>
    if (nums[0] >= target) return 0;<br>
    for (let i = 0, len = nums.length; i < len - 1; ++i) {<br>
        if ((nums[i] - target) * (nums[i + 1] - target) <= 0) return i + 1;<br>
    }<br>
    return nums.length;<br>
};<br>
