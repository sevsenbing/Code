## Remove Element
##### 2018年02月05日21:49:39
##### 已有经验的有效利用
***
### 题目
>Given an array and a value, remove all instances of that value in place and return the new length.
The order of elements can be changed. It doesn’t matter what you leave beyond the new length.  
给定一个数组和一个值，移除该值的所有实例并返回新的长度。 元素的顺序可以改变。无论你离开新的长度，都没有关系。

### 分析
尽管题目的要求不是那么清楚，但由于做过更为麻烦的删除重复元素的题目，按照原来的思路顺顺利利地写了出来。  
思路见[26题](https://github.com/Wanakiki/Code/blob/master/26.%20Remove%20Duplicates%20from%20Sorted%20Array.md)
### 代码
```c
int removeElement(int *nums, int numsSize,int val){
  int index=0;	//用于记录有多少重复
  for(int i=0;i<numsSize;i++){
    if(nums[i]==val)
      index++;
    else
      nums[i-index]=nums[i];	//元素前移
  }
  return numsSize-index;
}
```
