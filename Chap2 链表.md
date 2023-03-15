# Day 3

## 203 移除链表元素

设置虚拟头结点：dummy_head = ListNode(next = head)

## 707 设计链表

链表初始化

注意点1：连接插入节点和原链表的顺序；获取第n个节点的数值 return cur.val

注意点2: 调用class内函数不是addAtTail(self, val)，而是self.addAtTail(val)

## 206 翻转链表

双指针法：pre指针和cur指针

debug:反转cur.next = pre后，不需要使pre.next与tmp连接！再更新pre和cur指针即可

# Day 4

## 24 两两交换

一定要画图以明晰操作多个指针的先后顺序！按照新链表从前至后/从后至前的顺序进行交换步骤

debug: 对过程中所有动态变化的量以临时节点进行记录，以便更新

## 19 删除倒数第n个结点

双指针的经典应用：如果要删除倒数第n个节点，让fast先移动n步，然后让fast和slow同时移动，直到fast指向链表末尾；删掉slow所指向的节点

## 02.07 链表相交

频繁出现的错误：'NoneType' object has no attribute 'next'

双指针移动：让fast先移动abs(sizeA-sizeB)步，再同步移动 （类似于19）

## 142 环形链表

考查知识点1：如果fast指针（每次移动两个节点）和slow指针（每次移动一个节点）在途中相遇 ，说明这个链表有环。

考查知识点2: 从head结点出发一个指针，从相遇节点也出发一个指针，这两个指针每次只走一个节点,那么当这两个指针相遇的时候就是环形入口的节点。


