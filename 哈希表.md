# Day 6

## 242 字母异位词

要快速判断一个元素是否出现集合里 —— 考虑哈希法

方法一：定义size=26的数组，记录字符的ASCII相对数值出现频率 ord(i) - ord('a')  ：  字符串s中出现则索引+1，字符串t中出现则索引-1。判断最终是否等于[0] * 26

方法二：from collections import Counter (Counter: a subclass of dict for counting hashable objects)

方法三：from collections import defaultdict (defaultdict: provides a default value for a nonexistent key)

使用数组记录 

拓展题：383

## 349 数组的交集

不适合用数组的情况：存在很大的数值/数值分布很分散，使用数组会浪费存储空间

使用dict{}记录

## 202 快乐数

set和list的区别：set无序 vs list有序；set元素不重复 vs list元素可重复；set.add() vs list.append()

使用set记录

## 1 两数之和

enumerate()函数遍历列表并输出索引和对应的元素 （重复元素也会被枚举，且有自己的索引）

使用map记录 key-value结构

debug: 先判断是否存在两数之和等于target，再更新records里元素，否则重复索引元素会造成影响。因此，返回[index, records[target - value]]而不是[records[value], records[target - value]]，因为此时index还未更新至records中

case：[3,2,4] output [1,2] instead of [0,0]

不适合类似题15使用的双指针法：不能对数组元素进行排序，否则原数组的索引会被改变

# Day 7

## 454 四数相加

使用map记录 key-value结构（key放a+b两数之和，value放a和b两数之和出现的次数）

舍弃空间复杂度以降低时间复杂度

## 15 三数之和

不适合使用哈希表：在去重过程中有很多细节

双指针法：首先对数组元素进行排序； 在for i loop循环中，a = nums[i], b = nums[left], c = nums[right]

a的去重：判断nums[i]与nums[i - 1]是否相同，而不是判断nums[i]与nums[i+1]是否相同，否则会漏掉含有重复元素的三元数组 like [-1,-1,2]

b和c的去重：应该在找到三元数组之后进行去重

拓展题：18 套用两层for循环的双指针法，去重细节与本题类似





