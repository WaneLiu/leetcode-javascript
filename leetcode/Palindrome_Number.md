leetcode-9. Palindrome Number <br>
====
Description: determine whether an integer is a palindrome. Do this without extra space. <br>
---
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
