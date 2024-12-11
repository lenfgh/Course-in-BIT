<style>
    body {
        font-size: 13.5px;
        font-family: "Microsoft YaHei", "微软雅黑";
        line-height: 1.6;
    }
</style>


# 二、计算机信息数字化基础

<div style="text-align: right; font-style: italic;">by Len Fu 12.10.2024</div>

## 1. 二进制基础
### 1.1 基本概念
- **数制**：数的表示系统
- **基数**：数制所包含的符号的个数
- **权**/**位值**：由位置决定的值
### 1.2 数制间转换

#### 1.2.1 非十进制数转换十进制

**按权展开法**

二->十：
    $(1001011.1010)_{2}=1*2^{6}+1*2^{3}+1*2^{1}+1*2^{0}+1*2^{-1}+1*2^{-3}=75.625$
    
十六->十：
$(5CA)_{16}=5*16^{2}+12*16^{1}+10*10^{0}$

![alt text](image-23.png)

#### 1.2.2 十进制转换非十进制
**短除短乘法**

![alt text](image-22.png)

## 2. 基本数据表示

### 2.1 整数的计算机表示

- 机器数：数在机器中的编码表示

- 真值：机器数所对应的十进制数值

- 模数：一个计量器的容量 $R^{n}$ R是基数,ns是位数

- **计数器从0**开始计数

- **模数**：计数器所能计的数值的个数即模数

- **模数=最大值+1**

- **模数=$R^{n}$**

![alt text](image-24.png)

### 2.2 原码

**定义**

分别用0和1表示正号和负号，并置于z最高有效位上。绝对值部分置于右边

**表示范围**

$(-2^{n-1}+1,2^{n-1}-1)$

![alt text](image-25.png)

![alt text](image-26.png)

### 2.3 反码

**定义**

正数的反码表示与原码相同，负数的反码表示为其原码的符号位不变，其余各位取反。

**表示范围**

$(-2^{n-1}+1,2^{n-1}-1)$

### 2.4 补码

**定义**

$[X_{补}]=\begin{cases}X,\ for\ X\leq 0 \\ 2^{n}-|X|,\ for\ X<0\end{cases}$

正数的补码表示与原码相同，负数的补码表示为其原码的符号位不变，其余各位取反后加1。

**表示范围**

$(-2^{n-1},2^{n-1}-1)$

![alt text](image-27.png)

![alt text](image-29.png)

**补码运算**

![alt text](image-28.png)

![alt text](image-30.png)


### 2.5 浮点数

**定义**

$M\times R^{E}$

其中M是尾数（数的有效数字），R是基数，E是阶（小数在数中的实际位置）

**规格化**

非零浮点数的尾数最高位必须是1

**格式**

![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)

案例

![alt text](image-34.png)

![alt text](image-35.png)

![alt text](image-36.png)

**有效位**

<div style="color: red; font-weight: bold;">尾数二进制转换为十进制的数字位数</div>

![alt text](image-38.png)

### 2.6 实型变量

![alt text](image-37.png)

![alt text](image-39.png)

### 2.7 逻辑运算

![alt text](image-40.png)

![alt text](image-41.png)

![alt text](image-42.png)

![alt text](image-43.png)

![alt text](image-44.png)

### 2.8 ASCII码

美国标准信息交换码，是目前国际上最为流行的字符信息编码方案。

![alt text](image-45.png)

### 2.9 汉字编码

![alt text](image-46.png)

![alt text](image-47.png)

## 3. 信息编码与信息论

**编码**

![alt text](image-50.png)

![alt text](image-51.png)

### 3.1 模数转化

计算机处理音频信号时，必须将模拟信号转换为数字信息，这个过程由模数转换器ADC (Analog to Digital Converter)完成。

#### 音频信号转化

**每秒种音频信号存储容量大小**

<div style="color: red; font-weight: bold; text-align: center;">采样频率×采样精度×声道数/8 = 字节数</div>



![alt text](image-48.png)

![alt text](image-49.png)

### 3.2 图像

**颜色深度（位数）**

- 二值图像
    黑白双色（0或1）
- 灰度图像
    2的8次方=255种黑白变化色
- 彩色图像
    采用RGB彩色空间（R,G,B）
    一般写成（0~255, 0~255 ，0~255）

**图像大小**

<div style="color : red; text-align : center; font-weight : bold;">分辨率*颜色深度  （bit）

分辨率*颜色深度/8 （Byte）
</div>



![alt text](image-52.png)

![alt text](image-53.png)

![alt text](image-54.png)

![alt text](image-55.png)

![alt text](image-56.png)

### 3.3 图形

![alt text](image-58.png)

**图形与图像的区别**

![alt text](image-57.png)

### 3.4 视频

![alt text](image-59.png)

**数字画公式**

![alt text](image-60.png)

### 3.5 特征编码

![alt text](image-63.png)

![alt text](image-62.png)

![alt text](image-61.png)




