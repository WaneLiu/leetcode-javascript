leetcode-9. Palindrome Number <br>
====
Description: determine whether an integer is a palindrome. Do this without extra space. <br>
---
    解题思路：
    *将数字转换成字符串，并把字符串切割成单个的character数组 str_arr
    *分别用i与j指向数组的首尾，然后i、j相向移动并比较，直到出现元素不等返回false,最后返回true
    /**
      * @param {number} x
     * @return {boolean}
     */
    var isPalindrome = function(x) {
        let str = x.toString();// number=>str
        let str_arr = str.split("");//将字符串切割成character数组
        let i = 0,
            j = str_arr.length - 1;
        while ( i < j) {
            if (str_arr[i++] !== str_arr[j--]) {
                return false;
            }

        }
        return true;
    };
---
![](http://www.baidu.com/img/bdlogo.gif)  
