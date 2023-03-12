# Day 10

## 232 用栈实现队列

队列先进先出，栈先进后出

需要两个栈：输入栈stack_in + 输出栈stack_out

stack.append(x): add an item to the top of the stack

stack.pop(x): remove and return the top item from the stack. modify the original data structure.

debug: 在int peek()中，不可直接返回self.pop()，需要额外一步将队列开头元素加入stack_out的开头，否则影响int pop()的输出

## 225 用队列实现栈

队列 from collections import deque

仅需要一个队列：将从一端pop出去的元素append至另一端

栈顶为队列的右端 (que[-1])，即末端

que.append(): adds an element to the right end(back) of the deque

que.appendleft(): adds an element to the left end(front) of the deque

que.pop() and que.popleft()

# Day 11

## 20 有效的括号

对称匹配类题目 适合用栈解决

不能仅考虑True的情况，有时候需要从False的情况入手

debug：当存在右括号不匹配时，在循环过程中栈会为空，return False

拓展题：1047

## 150 逆波兰表达式求值

debug：the difference between int(a/b) and a//b （ int(-1/2) = 0 , -1 // 2 = -1 )

思路：遇到数字则入栈；遇到运算符则取出栈顶两个数字进行计算，并将结果压入栈中

使用内置operator简化操作

# Day 13

## 239 滑动窗口最大值 （hard mode）

暴力解法： O(n * k)算法 超出时间限制

单调队列 维护大数值

设计单调队列的规则： pop() 如果窗口移除的元素value等于单调队列出口的元素，则弹出出口元素，否则不进行任何操作

push() 如果push的元素value大于单调队列入口的元素，那么将队列入口的元素弹出，直到push元素的数值小于等于队列入口元素的数值为止

front() 返回当前窗口出口元素

## 347 前K个高频元素

优先级队列（使用小顶堆）

import heapq —— provides an implementation of the priority queue algorithm

heapq.heappush(pri_que, (freq, key)); heapq.heappop(pri_que)




