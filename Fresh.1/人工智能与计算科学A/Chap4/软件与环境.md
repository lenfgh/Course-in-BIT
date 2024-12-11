<style>
    body {
        font-size: 13.5px;
        font-family: "Microsoft YaHei", "微软雅黑";
        line-height: 1.6;
    }
</style>
# 四、软件与环境

## 1. 程序设计

### 1.1 面向过程编程设计特点

结构化程序设计方法是面向过程编程应遵循的基本方法和原则。主要包括：

1. 只采用三种基本的程序控制结构（顺序、选择、循环）来编制程序，从而使程序具有良好的结构；
2. 程序设计自顶而下；
3. 用结构化程序设计流程图表示算法。

## 1.2 计算机语言处理系统

![alt text](image.png)

![alt text](image-1.png)

## 2. 算法基础

### 2.1 图灵机与可计算

#### 2.1.1 图灵机

图灵机包括以下四个部分：

1. 一条**无限长的纸带**，用于使用二进制符号来表达计算所用的数据和控制规则；

2. 一个**读写头**，用于获取或者改写纸带当前位置上的符号；

3. 一个**状态寄存器**，用于保存图灵机当前所处的状态（包括停机状态）；

4. 一套**控制规则**，它根据当前机器所处的状态以及当前读写头所获取的符号，来确定读写头下一步的动作，并改变状态寄存器的值，令机器进入一个新的状态。

#### 2.1.2 可计算

可计算性是指对于给定的问题，是否存在一种算法可以解决它。

![alt text](image-2.png)

![alt text](image-3.png)

### 2.2 算法复杂度

#### 2.2.1 时间复杂度

计算所需的步数或指令条数.

![alt text](image-4.png)

#### 2.2.2 空间复杂度

计算所需的存储空间大小。

### 2.3 算法的特点

算法具有以下基本特征：

- 有穷性：一个算法必须在执行有限个操作步骤后终止

- 确定性：算法中每一步的含义必须是确切的，不可出现任何二义性

- 有效性：算法中的每一步操作都应该能有效执行，一个不可执行的操作是无效的

- 有零个或多个输入：这里的输入是指在算法开始之前所需要的初始数据，输入的多少取决于特定的问题

- 有一个或多个输出：所谓输出是指与输入有某种特定关系的量，在一个完整的算法中至少会有一个输出。

算法的两大分类：

- 数值运算：对问题进行数值解

- 非数值运算：包括非常广泛的领域

### 2.4 流程图表示算法

![alt text](image-5.png)

![alt text](image-6.png)

```mermaid
graph LR
    A([Start]) --> B[/Input n/]
    B --> C[Initialize i = 1]
    C --> D{Is i <= n?}
    D -- Yes --> E[Output i asterisks]
    E --> F[Increment i, i = i + 1]
    F --> D
    D -- No --> G([End])
```
![alt text](image-7.png)

**冒泡排序**

```mermaid
graph LR
    A(Start) --> B[Input 30 students' scores]
    B --> C[Initialize i = 0]
    C --> D{Is i < 29?}
    D -- Yes --> E[Initialize j = 0]
    E --> F{Is j < 30 - i - 1?}
    F -- Yes --> G{Is score~j > score~j+1?}
    G -- Yes --> H[Swap score~j and score~j+1]
    G -- No --> I[Continue next comparison]
    H --> I
    I --> J[Increment j, j = j + 1]
    J --> F
    F -- No --> K[Increment i, i = i + 1]
    K --> D
    D -- No --> L[Sorting complete, output scores]
```

**选择排序**

```mermaid
graph LR
    A([Start]) --> B[/Input 30 students' scores/]
    B --> C[Initialize i = 0]
    C --> D{i < 29?}
    D -- Yes --> E[Initialize minIndex = i]
    E --> F[Initialize j = i + 1]
    F --> G{j < 30?}
    G -- Yes --> H{score~j < score~minIndex?}
    H -- Yes --> I[minIndex = j]
    H -- No --> J[Continue next comparison]
    I --> J
    J --> K[Increment j, j = j + 1]
    K --> G
    G -- No --> L{minIndex != i?}
    L -- Yes --> M[Swap score~i and score~minIndex]
    L -- No --> N[Continue next iteration]
    M --> N
    N --> O[Increment i, i = i + 1]
    O --> D
    D -- No --> P([Sorting complete, output scores])
```

**插入排序**

```mermaid
graph   LR
    A([Start]) --> B[/Input 30 students' scores/]
    B --> C[Initialize i = 1]
    C --> D{i < 30?}
    D -- Yes --> E[Initialize key = score~i]
    E --> F[Initialize j = i - 1]
    F --> G{j >= 0 and score~j > key?}
    G -- Yes --> H[score~j+1 = score~j]
    H --> I[Decrement j, j = j - 1]
    I --> G
    G -- No --> J[score~j+1 = key]
    J --> K[Increment i, i = i + 1]
    K --> D
    D -- No --> L([Sorting complete, output scores])
```

### 2.5 典型算法

#### 2.5.1 递归算法

把问题转化为规模缩小了的同类问题的子问题，对这个子问题用函数来描述，然后递归调用该函数以获得问题的最终解。

三个要求：

- 每次调用在规模上都有所缩小

- 相邻两次重复之间有紧密的联系，前一次要为后一次做准备

- 在问题的规模最小时，必须直接给出解答而不再进行递归调用，因而每次递归调用是有条件的。

关键的两步

- 递归公式

- 边界条件

优点：以有限的方式描述规模任意大的问题的方法，简洁易于理解。

缺点：递归调用会占用大量的系统堆栈，可能导致栈溢出，计算速度慢。

#### 3.5.2 迭代算法

需要三个方面的准备：

- 确定迭代变量

- 建立迭代关系式

- 对迭代过程进行控制

## 3. 系统管理

### 3.1 计算机系统

![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png)

### 3.2 文件系统

操作系统中负责管理和存储文件信息的软件机构称为文件管理系统，简称**文件系统**。

- 文件本质上是一组有意义的信息/数据集合。

- 用户角度：支持建立文件，存入、读出、修改文件，当用户不再使用时删除文件等。

- 计算机角度：对文件存储器空间进行组织和分配，负责文件存储并对存入的文件进行保护和检索。



### 3.3 存储体系

![alt text](image-37.png)

![alt text](image-17.png)

![alt text](image-18.png)

![alt text](image-19.png)

### 3.4 磁盘管理

![alt text](image-12.png)

![alt text](image-13.png)

![alt text](image-14.png)

![alt text](image-15.png)

![alt text](image-16.png)







### 3.5 内存管理

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

## 4. 程序管理与人机交互

![alt text](image-23.png)

![alt text](image-24.png)

### 4.1 人机交互

#### 4.1.1 命令方式（字符显示式用户界面）

![alt text](image-25.png)

#### 4.1.2 图形化用户接口（GUI，Graphics User Interface）

![alt text](image-26.png)

#### 4.1.3 系统调用（system call）

![alt text](image-27.png)

### 4.2 进程、调度

![alt text](image-28.png)

![alt text](image-29.png)

![alt text](image-30.png)

![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)

![alt text](image-34.png)

![alt text](image-35.png)




























