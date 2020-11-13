# LeetCode刷题方法

##  编程方式

自顶向下的编程方式

- 可读性很强
- 性能可以会有损失

[125. 验证回文串](https://leetcode-cn.com/problems/valid-palindrome/)

```Java
public class Solution {
    public boolean isPalindrome(String s) {
        //高层次(主干)逻辑。
        //1.filter out number & char
        //2.reverse and
        String filteredS = _filterNonNumberAndChar(s);
        String reversedS = _reverseString(filteredS);
        return reversedS.equalsIgnoreCase(filteredS);
    }

    private String _reverseString(String filteredS) {
        return new StringBuilder(filteredS).reverse().toString();
    }
    
    private String _filterNonNumberAndChar(String s){

        return s.replaceAll("[个A-Za-z0-9] ","")
    }
}

```

## 切题四件套

1. Clarification：理清题目
2. Possible solutions：想到所有可能的解法，比较不同的方法
   1. compare (time/space)
   2. optimal（加强）
3. Coding：编写程序
4. Test cases

## 五步刷题法

### 刷题第一遍

1. 5分钟：读题 + 思考
2. 直接看解法：注意！
   - 多解法，比较解法优劣
3. 背诵、默写好的解法

### 刷题第二遍

- 马上自己写 —> LeetCode 提交
- 多种解法比较、体会 —> 优化！

### 刷题第三遍

- 过了一天后，再重复做题
- 不同解法的熟练程度 —> 专项练习

#### 刷题第四遍

- 过了一周：反复回来练习相同题目

### 刷题第五遍

- 面试前一周恢复性训练

## 数据结构

[数据结构脑图](https://naotu.baidu.com/file/b832f043e2ead159d584cca4efb19703?token=7a6a56eb2630548c)

![数据结构](https://aliyun-typora-img.oss-cn-beijing.aliyuncs.com/imgs/20201026164602.png)

### 一维：

- 基础：数组 array (string), 链表 linked list
- 高级：栈 stack, 队列 queue, 双端队列 deque, 集合 set, 映射 map (hash or map), etc

### 二维

- 基础：树 tree, 图 graph
- 高级：二叉搜索树 binary search tree (red-black tree, AVL), 堆 heap, 并查集 disjoint set, 字典树 Trie, etc

###  特殊

- 位运算 Bitwise, 布隆过滤器 BloomFilter
- LRU Cache

## 算法

[算法脑图](https://naotu.baidu.com/file/0a53d3a5343bd86375f348b2831d3610?token=5ab1de1c90d5f3ec)

![算法](https://aliyun-typora-img.oss-cn-beijing.aliyuncs.com/imgs/20201026164323.png)

### If-else, switch 

If-else, switch—> branch

### for, while loop

 for, while loop—> Iteration

### 递归 Recursion 

- Divide & Conquer
- Backtrace

### 搜索 Search

- 深度优先搜索 Depth first search
-  广度优先搜索 Breadth first search
-  A*, etc

### 动态规划 Dynamic Programming

###  二分查找 Binary Search

### 贪心 Greedy

### 数学 Math 

### 几何 Geometry



## 时间复杂度、空间复杂度

### Big O notation

- O(1): Constant Complexity 常数复杂度

  - ```java
    int n = 1000;
    System.out.println("Hey - your input is: " + n);
    ```

    

  - ```java
    int n = 1000;
    System.out.println("Hey - your input is: " + n);
    System.out.println("Hmm.. I'm doing more stuff with: " + n);
    System.out.println("And more: " + n);
    ```

- O($log n$): Logarithmic Complexity 对数复杂度

  - ```java
    for (int i = 1; i < n; i = i * 2) {
    	System.out.println("Hey - I'm busy looking at: " + i);
    }
    ```

- O($n$): Linear Complexity 线性时间复杂度

  - ```java
    for (int i = 1; i <= n; i++) {
    	System.out.println("Hey - I'm busy looking at: " + i);
    }
    ```

- O($n^2$): N square Complexity 平方

  - ```java
    for (int i = 1; i <= n; i++) {
    	for (int j = 1; j <=n; j++) {
    		System.out.println("Hey - I'm busy looking at: " + i + " and " +j);
    	}
    }
    ```

- O($n^3$): N square Complexity 立方

- O($2^n$): Exponential Growth 指数

  - ```java
    int fib(int n) {
    	if (n <= 2) return n;
            return fib(n - 1) + fib(n - 2);
    }
    ```

- O($n!$): Factorial 阶乘



