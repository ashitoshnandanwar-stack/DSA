# Day 1

Problem 1
```
A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and
removing all non-alphanumeric characters, it reads the same forward and backward.
Alphanumeric characters include letters and numbers.

Given a string s, return true if it is a palindrome, or false otherwise.
Example 1:
Input: s = "A man, a plan, a canal: Panama"
Output: true
Explanation: "amanaplanacanalpanama" is a palindrome.

Example 2:
Input: s = "race a car"
Output: false
Explanation: "raceacar" is not a palindrome.

Example 3:
Input: s = " "
Output: true
Explanation: s is an empty string "" after removing non-alphanumeric characters.
Since an empty string reads the same forward and backward, it is a palindrome.

solution => 
class Solution {
    public boolean isPalindrome(String s)
    {
       int i = 0;
       int j = s.length() - 1;

       while(i<j)
       {
        char left = s.charAt(i);
        char right = s.charAt(j);

        if(!Character.isLetterOrDigit(left))
        {
            i = i+1;
            continue;
        }

        if(!Character.isLetterOrDigit(right))
        {
            j = j - 1;
            continue;
        }

        if(Character.toLowerCase(left) != Character.toLowerCase(right))
        {
            return false;
        }

        i++;
        j--;
       }
       return true;
    }
}
```
**<hr>**

Problem 2
```
Write a function that reverses a string. The input string is given as an array of characters s.
You must do this by modifying the input array in-place with O(1) extra memory.

Example 1:
Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]

Example 2:
Input: s = ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]

Solution =>
class Solution {
    public void reverseString(char[] s) 
    {
       int i = 0;
       int j = s.length - 1;

       while(i<j)
       {
        char temp = s[i];
        s[i] = s[j];
        s[j] = temp;

        i++;
        j--;
       }
    }
}
```

**<hr>**

Problem 3
```
Given an integer array nums sorted in non-decreasing order,
return an array of the squares of each number sorted in non-decreasing order.

Example 1:
Input: nums = [-4,-1,0,3,10]
Output: [0,1,9,16,100]
Explanation: After squaring, the array becomes [16,1,0,9,100].
After sorting, it becomes [0,1,9,16,100].

Example 2:
Input: nums = [-7,-3,2,3,11]
Output: [4,9,9,49,121]

Solution =>
class Solution 
{
    public int[] sortedSquares(int[] nums) 
    {
       int[] res = new int[nums.length];
       int k = nums.length - 1;
       int i = 0;
       int j = nums.length - 1;

       while(i<=j)
       {
        if(Math.abs(nums[i]) > Math.abs(nums[j]))
        {
            res[k] = nums[i] * nums[i];
            i++;
        }
        else
        {
            res[k] = nums[j] * nums[j];
            j--;
        }
        k--;
       }
       return res;
    }
}
```

**<hr>**

Problem 4
```
Given a string s, return true if the s can be palindrome after deleting at most one character from it.

Example 1:
Input: s = "aba"
Output: true

Example 2:
Input: s = "abca"
Output: true
Explanation: You could delete the character 'c'.

Example 3:
Input: s = "abc"
Output: false

solution =>
class Solution {
    public boolean palindromeHelper(int i, int j, String s)
    {
        while(i<j)
        {
            if(s.charAt(i) != s.charAt(j))
            {
                return false;
            }
            i++;
            j--;
        }
        return true;
    }
    public boolean validPalindrome(String s) 
    {
        int i = 0;
        int j = s.length - 1;

        while(i<j)
        {
            char left = s.charAt(i);
            char right = s.charAt(j);

            if(left != right)
            {
                return palindromeHelper(i+1, j, s) ||  palindromeHelper(i, j-1, s);
            }
            else
            {
                left = left + 1;
                right = right - 1;
            }
        }
    }
}
```
**<hr>**

# Day 2

Problem 1
```

