**28. 实现strStr()**

 - 题目要求：
给定一个 haystack 字符串和一个 needle 字符串，在 haystack 字符串中找出 needle 字符串出现的第一个位置 (从0开始)。如果不存在，则返回  -1。

 - 示例：
```
输入: haystack = "hello", needle = "ll"
输出: 2

输入: haystack = "aaaaa", needle = "bba"
输出: -1
```


 - 分析：
 不断刷新头尾位置进行与needle比较，结束的标志是起始位置+needle长度>haystack.
```
class Solution:
    def strStr(self, haystack, needle):
        if needle not in haystack:
            return -1
        Nelenth= len(needle)
        Halengh =len(haystack)
        sta = 0
        i =0
        while sta+Nelenth<=Halengh:
            if haystack[sta:sta+Nelenth] == needle:
                i =i+1
                return sta
            sta = sta +1
```