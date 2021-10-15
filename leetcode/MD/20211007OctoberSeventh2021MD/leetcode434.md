# leetcode434.字符串中单词数

### 完成情况
Data: October 7,2021 11:00AM  
剩余时间：8:19.5  
通过测试用例：完全通过  
提交错误次数：一次
第一次：忽略了全是空格字符的特殊情况  

### 个人解题思路
读到单词末尾记一次数
首先遍历到第一个不是空字符的字符作为字符串开头  
从开头往后读，读到空字符则计数segments+1  
再继续跳过空字符，保证下次一定是以字母开头  
如果末尾是空字符，则输出segments  
如果末尾不是空字符，少计算一次，输出segments+1  

### 题解解题思路
记录全部单词的数量相当于记录全部单词前缀的个数  
满足单词前缀的条件：1.在字符串第一个字符，且该字符不是空字符  
                  2.不在字符串第一个字符，但该字符前一个字符是空字符，且该字符不是空字符  

## 复杂度分析
个人解题与题解解题均是遍历一遍，且不占用额外空间  
时间复杂度：O(n)  
空间复杂度：O(1)  