<style>
    body {
        font-size: 13.5px;
        font-family: "Microsoft YaHei", "微软雅黑";
        line-height: 1.6;
    }
</style>

# 五、符号智能

<div style="text-align: right; font-style: italic;">by Len Fu 12.10.2024</div>

## 1. 搜索与问题求解

### 1.1 概念

**搜索**

搜索是人工智能技术中进行问题求解的基本技术，不管是符号智能还是计算智能以及统计智能和交互智能，不管是解决具 体应用问题，还是智能行为本身，最终往往都归结为某种搜索，都要用某种搜索算法来实现。

**解**

问题的解：就是从初始状态到目标状态的一组行动序列。

最优解：所有解里面代价最小的解即为最优解。

**搜索过程中要考虑的问题**

1. 搜索过程是否一定能找到一个解。

2. 当搜索过程找到一个解时，如何判断这个解是最优解。

3. 搜索过程的时间与空间复杂性如何。

4. 搜索过程是否会终止运行或是否会陷入死循环。

**搜索过程的5部分**

![alt text](image.png)

### 1.2 状态空间

让计算机知道问题是什么：

**状态空间表示法：状态、操作、状态空间**

#### 1.2.1 状态

![alt text](image-1.png)

#### 1.2.2 操作（算符）

![alt text](image-2.png)

#### 1.2.3 状态空间

![alt text](image-3.png)

**示例**

![alt text](image-4.png)

![alt text](image-5.png)

![alt text](image-6.png)

### 1.3 搜索策略（盲目式）

**回溯搜索**

![alt text](image-7.png)


**图搜索算法的思想**

![alt text](image-8.png)

#### 1.3.1 广度优先搜索

**高价**

**若存在，必有解**

**每次都从最浅的开始**

![alt text](image-9.png)

#### 1.3.2 深度优先搜索

**首先拓展新节点**

![alt text](image-10.png)

##### 注意事项

- 在深度优先搜索中，当搜索到某一个状态时，它所有的子状态以及子状态的后裔状态都必须先于该状态的兄弟状态被搜索。

- 为了保证找到解，应选择合适的深度限制值，或采取不断加大深度限制值的办法，反复搜索，直到找到解。

- 深度优先搜索并不能保证第一次搜索到的某个状态时的路径是到这个状态的最短路径。

- 对任何状态而言，以后的搜索有可能找到另一条通向它的路径。如果路径的长度对解题很关键的话，当算法多次搜索到同一个状态时，它应该保留最短路径。

## 2. 知识表示与推理

**知识表示**

知识表示就是把人类知识符号化或模型化，转换为机器内部的一种数据结构，使得计算机能够方便地存储、处理和利用。

知识表示方法：
- 一阶谓词逻辑表示法

- 产生式表示方法

- 语义网络表示方法

- 框架表示方法

### 2.1 一阶谓词逻辑表示法

一阶谓词逻辑是使用于数学、哲学、语言学及计算机科学中的一种形式系统。

![alt text](image-11.png)

![alt text](image-12.png)

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

### 2.2 其它表示方法

![alt text](image-18.png)

### 2.3 知识推理

推理是求解的一种基本方法，是从已知事实出发，运用已掌握的知识，推导出其中蕴含的事实性结论，或归纳出某些新的结论的过程。

#### 2.3.1 确定性推理

![alt text](image-19.png)

![alt text](image-20.png)

#### 2.3.2 不确定性推理

![alt text](image-21.png)

![alt text](image-22.png)

## 3. 自然语言处理

### 3.1 主要研究内容

![alt text](image-24.png)

![alt text](image-23.png)

### 3.2 研究困难

![alt text](image-25.png)

![alt text](image-42.png)

![alt text](image-43.png)

![alt text](image-44.png)

![alt text](image-41.png)

![alt text](image-40.png)

![alt text](image-39.png)

![alt text](image-38.png)

### 3.3 研究技术

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)

![alt text](image-34.png)

![alt text](image-35.png)

![alt text](image-36.png)












