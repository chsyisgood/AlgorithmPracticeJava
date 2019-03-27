# Linked List  链表
*“男人最重要的是持久。”*

--------------------------------------------------------
#### 总述
链表的题目比较少，大致因为题目类型比较单一而且题目相对简单。链表的题目可能唯一的trick就是使用【**双指针**】，并且大多数题目用 **recursion** 的方式可以轻松解决。唯一要注意的陷阱是**指针指向**有些情况下必须**重置**（当然部分tree的题目也会涉及！）。这里的链表通常指的是最简单的**只含有头部**的**单向链表**，双向链表和包含尾部的链表这里很少涉及，但是在某些题目例如设计一些数据结构时可以用到，可以减少遍历的复杂度！
- 基础代码
``` java
public class ListNode {
     int val;
     ListNode next;
     ListNode(int x) { val = x; }
}
```

--------------------------------------------------------
#### 1. 双指针  two pointers
所谓双指针，一般情况下有以下几种不同的理解：
- 定义 slow 和 fast 两种不同**速度**的指针，每次循环他们移动的次数有差别
- 定义指针 p 和 q，一个指针总是在另一个指针的 k 距离后面
- 定义指针 left 和 right（类似BS），用来遍历（但在链表中不常用，是一种思路）

##### 1.1 [slow n fast](https://github.com/chsyisgood/AlgorithmPracticeJava/blob/master/05List/slownfast.md)
slow 和 fast 是两个不同速度的指针，这种设计可以方便我们在 one pass 的情况下找到链表中的“特殊点”：比如中点（1/2处）或者任意比例的点（1/3 处）。
而且，通过合理设计代码的先后，可以选择到底是“小中点”还是“大中点”，有道题挺蛋疼的就是有这样的细致要求。

题目：

##### 1.2 [k dist](https://github.com/chsyisgood/AlgorithmPracticeJava/blob/master/05List/kdist.md) 
这类没啥好说的，就是一开始指针q在p的后面，这样如果q到达终点后，p必然指向距离终点前k距离的结点上。部分题目需要 one pass可以用到，很局限。

题目：

##### 1.3 left n right
left 和 right 作为左右指针最常见在于“分治法”。而分治法中一个典型就是Binary Search。当然我印象中 3 sum 也是使用这种【思路】的题目。总之需要心中有数，这类可以方便我们从两头缩小范围

--------------------------------------------------------
#### 2. [递归  recursion](https://github.com/chsyisgood/AlgorithmPracticeJava/blob/master/05List/recursion.md)
其实怎么说，递归只是一种coding的方式，在链表题目中可以让代码更加的简洁、漂亮。这算是递归的最简单的练习吧。

